---
title: "Grundlegendes zu Isolationsstufen"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2c41e23a-da6c-4650-b5fc-b5fe53ba65c3
caps.latest.revision: 17
caps.handback.revision: 16
manager: jhubbard
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pt-br
  - ru-ru
  - sv-se
  - zh-cn
  - zh-tw
---
# Grundlegendes zu Isolationsstufen
  Transaktionen geben eine Isolationsstufe an, mit der definiert wird, bis zu welchem Ausmaß eine Transaktion von Ressourcen\- oder Datenänderungen isoliert sein muss, die von anderen Transaktionen durchgeführt werden. Die einzelnen Isolationsstufen werden dahin gehend beschrieben, welche Parallelitätsnebeneffekte \(wie z. B. Dirty Reads oder Phantomlesezugriffe\) zulässig sind.  
  
 Transaktionsisolationsstufen steuern Folgendes:  
  
-   Ob beim Lesen von Daten Sperren aktiviert werden können, und welcher Sperrentyp angefordert wird.  
  
-   Wie lange die Lesesperren aufrechterhalten werden.  
  
-   Ob ein Lesevorgang, der auf Zeilen verweist, die durch eine andere Transaktion geändert wurden:  
  
    -   blockiert wird, bis die exklusive Sperre für die Zeile aufgehoben wird.  
  
    -   die durch einen Commit bestätigte Version der Zeile abruft, die zum Zeitpunkt des Anweisungs\- oder Transaktionsstarts vorhanden war.  
  
    -   die Datenänderung liest, für die noch kein Commit ausgeführt wurde.  
  
 Das Auswählen einer Transaktionsisolationsstufe hat keine Auswirkungen auf die Sperren, die zum Schutz von Datenänderungen eingerichtet werden. Eine Transaktion erhält immer eine exklusive Sperre für alle von ihr geänderten Daten und hält diese Sperre bis zum Abschluss der Transaktion aufrecht, und zwar unabhängig davon, welche Isolationsstufe für diese Transaktion festgelegt wurde. Für Lesevorgänge wird durch die Transaktionsisolationsstufen in erster Linie der Grad des Schutzes vor den Auswirkungen der Änderungen definiert, die durch andere Transaktionen vorgenommen werden.  
  
 Eine niedrigere Isolationsstufe erhöht einerseits die Möglichkeit, dass viele Benutzer gleichzeitig auf Daten zugreifen können, führt aber auch dazu, dass die Benutzer mit einem Anstieg der Parallelitätseffekte \(Dirty Reads oder verlorene Updates\) rechnen müssen. Umgekehrt schränkt eine höhere Isolationsstufe zwar die Typen der Parallelitätseffekte ein, mit denen Benutzer rechnen müssen, gleichzeitig werden dafür aber mehr Systemressourcen beansprucht, und die Wahrscheinlichkeit steigt, dass sich die Transaktionen gegenseitig blockieren. So muss bei jeder Auswahl der geeigneten Isolationsstufe eine Abwägung zwischen den Datenintegritätsanforderungen der Anwendungen einerseits und dem mit jeder Isolationsstufe verbundenen Aufwand andererseits erfolgen. Die höchste Isolationsstufe \(Serializable\) garantiert, dass eine Transaktion jedes Mal, wenn sie einen Lesevorgang wiederholt, genau dieselben Daten liest. Dies wird jedoch durch ein Ausmaß an Sperren erreicht, das in Systemen mit mehreren Benutzern wahrscheinlich zu negativen Auswirkungen für andere Benutzer führt. Mit der niedrigsten Isolationsstufe \(Read Uncommitted\) können Daten abgerufen werden, die von anderen Transaktionen geändert wurden, für die jedoch noch kein Commit ausgeführt wurde. In der Isolationsstufe „Read Uncommitted“ können sämtliche denkbaren Parallelitätsnebeneffekte auftreten, dagegen werden keine Lesesperren und keine Versionsverwaltung verwendet, wodurch der Aufwand minimiert wird.  
  
## Hinweise  
 Die folgende Tabelle veranschaulicht, welche Parallelitätsnebeneffekte in den einzelnen Isolationsstufen zulässig sind.  
  
|Isolationsebene|Dirty Read|Non Repeatable Read|Phantom|  
|---------------------|----------------|-------------------------|-------------|  
|Read Uncommitted|Ja|Ja|Ja|  
|Read Committed|Nein|Ja|Ja|  
|Repeatable Read|Nein|Nein|Ja|  
|Momentaufnahme|Nein|Nein|Nein|  
|Serializable|Nein|Nein|Nein|  
  
 Transaktionen müssen mindestens auf der Isolationsstufe „Repeatable Read“ ausgeführt werden, um den Verlust von Updates zu verhindern. Dies kann auftreten, wenn zwei Transaktionen jeweils die gleiche Zeile abrufen und sie später auf Grundlage der zunächst abgerufenen Werte aktualisieren. Wenn die beiden Transaktionen Zeilen mit einer einzigen UPDATE\-Anweisung aktualisieren und die Aktualisierung nicht auf Grundlage der zuvor abgerufenen Werte erfolgt, können bei der Standardisolationsstufe „Read Committed“ keine verlorenen Aktualisierungen auftreten.  
  
 Zum Festlegen der Isolationsstufe für eine Transaktion können Sie die [setTransactionIsolation](../content/setTransactionIsolation-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse verwenden. Diese Methode nimmt einen **int**\-Wert als Argument an. Dieser basiert auf den Verbindungskonstanten, wie im Folgenden dargestellt:  
  
```  
con.setTransactionIsolation(Connection.TRANSACTION_READ_COMMITTED);  
```  
  
 Zum Verwenden der neuen Snapshotisolationsstufe von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] können Sie eine der SQLServerConnection\-Konstanten wie folgt verwenden:  
  
```  
con.setTransactionIsolation(SQLServerConnection.TRANSACTION_SNAPSHOT);  
```  
  
 Sie können auch Folgendes verwenden:  
  
```  
con.setTransactionIsolation(Connection.TRANSACTION_READ_COMMITTED + 4094);  
```  
  
 Weitere Informationen zu [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Isolationsstufen finden Sie unter "Isolationsstufen in [!INCLUDE[ssDE](../content/includes/ssDE_md.md)]" in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation.  
  
## Siehe auch  
 [Ausführen von Transaktionen mit dem JDBC-Treiber](../content/Performing-Transactions-with-the-JDBC-Driver.md)  
  
  