---
title: "Verwenden der adaptiven Pufferung"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 92d4e3be-c3e9-4732-9a60-b57f4d0f7cb7
caps.latest.revision: 52
caps.handback.revision: 51
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
# Verwenden der adaptiven Pufferung
  Mit der adaptiven Pufferung können Daten mit großen Werten ohne den Aufwand von Servercursorn abgerufen werden. In Anwendungen kann die Funktion der adaptiven Pufferung mit allen Versionen von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwendet werden, die vom Treiber unterstützt werden.  
  
 Wenn [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] eine Abfrage ausführt, ruft der Treiber normalerweise alle Ergebnisse vom Server in einen Anwendungsspeicher ab. Obwohl bei diesem Ansatz die Ressourcenauslastung für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] reduziert wird, kann ein OutOfMemoryError in der JDBC\-Anwendung für die Abfragen ausgelöst werden, bei denen sehr große Ergebnisse zurückgegeben werden.  
  
 Damit Anwendungen sehr große Ergebnisse behandeln können, stellt [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] die adaptive Pufferung bereit. Mithilfe der adaptiven Pufferung ruft der Treiber Ergebnisse der Anweisungsausführung erst dann von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ab, wenn sie in der Anwendung benötigt werden, statt alle Ergebnisse auf einmal abzurufen. Der Treiber verwirft außerdem die Ergebnisse, sobald die Anwendung nicht mehr auf sie zugreifen kann. Im Folgenden werden einige Szenarien beschrieben, in denen die Verwendung der adaptiven Pufferung sinnvoll sein kann:  
  
-   **Die Abfrage liefert ein sehr umfangreiches Resultset:** Die Anwendung kann eine SELECT\-Anweisung ausführen, die mehr Zeilen zurückgibt, als im Speicher der Anwendung gespeichert werden können. In vorherigen Versionen musste die Anwendung einen Servercursor verwenden, um einen OutOfMemoryError zu vermeiden. Die adaptive Pufferung stellt die Möglichkeit bereit, ein beliebig großes Resultset mit Vorwärtscursor und schreibgeschützt zu übergeben, ohne dass ein Servercursor erforderlich ist.  
  
-   **Die Abfrage erzeugt sehr umfangreiche**  [SQLServerResultSet](../content/SQLServerResultSet-Class.md) **\-Spalten oder**  [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md) **\-OUT\-Parameterwerte:** Die Anwendung kann einen Wert \(Spalte oder OUT\-Parameter\) abrufen, der zu groß ist, um vollständig im Anwendungsspeicher gespeichert zu werden. Durch die adaptive Pufferung kann die Clientanwendung solche Werte als Datenstrom mithilfe der Methoden getAsciiStream, getBinaryStream, oder getCharacterStream abrufen. Die Anwendung ruft den Wert beim Lesen des Datenstroms von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ab.  
  
> [!NOTE]  
>  Mit adaptiver Pufferung puffert der JDBC\-Treiber nur die benötigte Datenmenge. Der Treiber stellt keine öffentliche Methode zum Steuern oder Beschränken der Puffergröße bereit.  
  
## Festlegen der adaptiven Pufferung  
 Ab Version 2.0 des JDBC\-Treibers ist das Standardverhalten des Treibers "**adaptive**". Dies bedeutet, um das Verhalten der adaptiven Pufferung zu verwenden, muss das Verhalten der adaptiven Pufferung in der Anwendung nicht explizit angefordert werden. In Version 1.2 lautete der Puffermodus jedoch standardmäßig "**full**", und die Anwendung musste den Modus für die adaptive Pufferung explizit anfordern.  
  
 Es gibt drei Möglichkeiten, mit denen eine Anwendung die Verwendung der adaptiven Pufferung für die Anweisungsausführung anfordern kann:  
  
-   Die Anwendung kann die Verbindungseigenschaft **responseBuffering** auf "adaptive" festlegen. Weitere Informationen zum Festlegen der Verbindungseigenschaften finden Sie unter [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md).  
  
-   Die Anwendung kann die [setResponseBuffering](../content/setResponseBuffering-Method--SQLServerDataSource-.md)\-Methode des [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Objekts zum Festlegen des Antwortpufferungsmodus für alle Verbindungen verwenden, die mit diesem [SQLServerDataSource](../content/SQLServerDataSource-Class.md)\-Objekt erstellt wurden.  
  
-   Die Anwendung kann die [setResponseBuffering](../content/setResponseBuffering-Method--SQLServerStatement-.md)\-Methode der [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse verwenden, um den Antwortpuffermodus für ein bestimmtes Anweisungsobjekt festzulegen.  
  
 Bei Verwendung von JDBC Driver, Version 1.2, mussten Anwendungen das Anweisungsobjekt in [SQLServerStatement](../content/SQLServerStatement-Class.md) umwandeln, um die [setResponseBuffering](../content/setResponseBuffering-Method--SQLServerStatement-.md)\-Methode zu verwenden. Diese frühere Verwendungsweise wird in den Codebeispielen in [Beispiel zum Lesen umfangreicher Daten](../content/Reading-Large-Data-Sample.md) und [Beispiel zum Lesen umfangreicher Daten mit gespeicherten Prozeduren](../content/Reading-Large-Data-with-Stored-Procedures-Sample.md) veranschaulicht.  
  
 Mit Version 2.0 des JDBC\-Treibers können Anwendungen jedoch die [isWrapperFor](../content/isWrapperFor-Method--SQLServerStatement-.md)\-Methode und die [unwrap](../content/unwrap-Method--SQLServerStatement-.md)\-Methode verwenden, um auf die herstellerspezifischen Funktionen zuzugreifen, ohne Vermutungen über die Klassenhierarchie der Implementierung anstellen zu müssen. Beispielcode finden Sie im Thema [Beispiel zum Aktualisieren umfangreicher Daten](../content/Updating-Large-Data-Sample.md).  
  
## Abrufen umfangreicher Daten mit adaptiver Pufferung  
 Wenn große Werte einmal mithilfe der get\<Typ\>Stream\-Methoden gelesen werden und auf die ResultSet\-Spalten und die CallableStatement\-OUT\-Parameter in der Reihenfolge zugegriffen wird, in der sie von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] zurückgegeben werden, minimiert die adaptive Pufferung die Anwendungsspeicherauslastung beim Verarbeiten der Ergebnisse. Beim Verwenden der adaptiven Pufferung:  
  
-   Die in der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse und der [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse definierten get\<Type\>Stream\-Methoden geben schreibgeschützte Datenströme zurück, die zurückgesetzt werden können, wenn sie von der Anwendung gekennzeichnet werden. Wenn in der Anwendung `reset` für den Datenstrom ausgeführt werden soll, muss zunächst die `mark`\-Methode für diesen Datenstrom aufgerufen werden.  
  
-   Die in der [SQLServerClob](../content/SQLServerClob-Class.md)\-Klasse und der [SQLServerBlob](../content/SQLServerBlob-Class.md)\-Klasse definierten get\<Type\>Stream\-Methoden geben Datenströme zurück, die immer wieder an der Anfangsposition des Datenstroms positioniert werden können, ohne die `mark`\-Methode aufzurufen.  
  
 Wenn die Anwendung adaptive Pufferung verwendet, können die von den get\<Type\>Stream\-Methoden abgerufenen Werte nur einmal abgerufen werden. Wenn Sie versuchen, eine get\<Type\>\-Methode für die gleiche Spalte oder den gleichen Parameter aufzurufen, nachdem die get\<Type\>Stream\-Methode des gleichen Objekts aufgerufen wurde, wird eine Ausnahme mit der folgenden Meldung ausgelöst: "Auf die Daten wurde zugegriffen; sie sind für diese Spalte oder diesen Parameter nicht verfügbar."  
  
## Richtlinien für die Verwendung der adaptiven Pufferung  
 Entwickler sollten sich an diese wichtigen Richtlinien halten, um die Speicherauslastung durch die Anwendung zu minimieren:  
  
-   Vermeiden Sie die Verwendung der Verbindungszeichenfolgeneigenschaft **selectMethod\=cursor**, damit die Anwendung ein sehr großes Resultset verarbeiten kann. Die adaptive Pufferung ermöglicht Anwendungen, sehr große, schreibgeschützte Vorwärtsresultsets ohne die Verwendung eines Servercursors zu verarbeiten. Beachten Sie, dass das Festlegen von **selectMethod\=cursor** sich auf alle schreibgeschützten Resultset mit Vorwärtscursor auswirken, die über diese Verbindung generiert werden. Das heißt, wenn die Anwendung wiederholt kleine Resultsets mit wenigen Zeilen verarbeitet, werden zum Erstellen, Lesen und Schließen eines Servercursors für jedes Resultset sowohl auf Clientseite als auch auf Serverweite mehr Ressourcen verwendet als bei einer **selectMethod**, die auf einen anderen Wert als **cursor** festgelegt ist.  
  
-   Lesen Sie große Text\- oder Binärwerte als Datenströme mithilfe der Methoden getAsciiStream, getBinaryStream, oder getCharacterStream anstelle der getBlob\-Methode oder der getClob\-Methode. Ab Version 1.2 stellt die [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse neue get\<Type\>Stream\-Methoden hierfür bereit.  
  
-   Stellen Sie sicher, dass Spalten mit potenziell großen Werten in der Liste der Spalten in einer SELECT\-Anweisung am Ende platziert werden und dass die get\<Type\>Stream\-Methoden von [SQLServerResultSet](../content/SQLServerResultSet-Class.md) verwendet werden, um in der Reihenfolge auf die Spalten zuzugreifen, in der sie ausgewählt werden.  
  
-   Stellen Sie sicher, dass OUT\-Parameter mit potenziell großen Werten in der Liste der Parameter im SQL zum Erstellen von [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md) zuletzt deklariert werden. Stellen Sie außerdem sicher, dass die get\<Type\>Stream\-Methoden von [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md) verwendet werden, um auf die OUT\-Parameter in der Reihenfolge zuzugreifen, in der sie deklariert wurden.  
  
-   Vermeiden Sie, gleichzeitig mehrere Anweisungen über die gleiche Verbindung auszuführen. Das Ausführen einer weiteren Anweisung vor dem Verarbeiten der Ergebnisse der vorhergehenden Anweisung kann dazu führen, dass nicht verarbeitete Ergebnisse im Anwendungsspeicher gepuffert werden.  
  
-   In bestimmten Fällen wie den folgenden bietet die Verwendung von **selectMethod\=cursor** gegenüber **responseBuffering\=adaptive** Vorteile:  
  
    -   Wenn die Anwendung ein schreibgeschütztes Resultset mit Vorwärtscursor langsam verarbeitet, z. B. beim Lesen jeder Zeile nach einer Benutzereingabe, wird die Ressourcenverwendung durch **selectMethod\=cursor** anstelle von **responseBuffering\=adaptive**[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] möglicherweise verringert.  
  
    -   Wenn die Anwendung zwei oder mehr schreibgeschützte Resultsets mit Vorwärtscursor gleichzeitig für die gleiche Verbindung verarbeitet, lässt sich der vom Treiber bei der Verarbeitung dieser Resultsets benötigte Speicher durch **selectMethod\=cursor** anstelle von **responseBuffering\=adaptive** möglicherweise verringern.  
  
     In beiden Fällen müssen Sie den zusätzlichen Aufwand des Erstellens, Lesens und Schließens der Servercursor berücksichtigen.  
  
 Darüber hinaus enthält die folgende Liste einige Empfehlungen für scrollfähige Resultsets und aktualisierbare Resultsets mit Vorwärtscursor:  
  
-   Bei scrollfähigen Resultsets liest der Treiber beim Abrufen eines Zeilenblocks immer die von der [getFetchSize](../content/getFetchSize-Method--SQLServerResultSet-.md)\-Methode des [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts angegebene Anzahl von Zeilen in den Speicher ein, auch bei aktivierter adaptiver Pufferung. Wenn das Scrolling einen OutOfMemoryError verursacht, können Sie die Anzahl der abgerufenen Zeilen verringern, indem Sie die [setFetchSize](../content/setFetchSize-Method--SQLServerResultSet-.md)\-Methode des [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts aufrufen, um die Abrufgröße auf eine kleinere Zeilenanzahl festzulegen und ggf. sogar auf eine Zeile verringern. Führt dies immer noch zu einem OutOfMemoryError, vermeiden Sie das Einschließen sehr großer Spalten in scrollfähigen Resultsets.  
  
-   Bei aktualisierbaren Resultsets mit Vorwärtscursor liest der Treiber beim Abrufen eines Zeilenblocks normalerweise die von der [getFetchSize](../content/getFetchSize-Method--SQLServerResultSet-.md)\-Methode des [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts angegebene Anzahl von Zeilen in den Speicher ein, auch wenn die adaptive Pufferung für die Verbindung aktiviert ist. Wenn das Aufrufen der [next](../content/next-Method--SQLServerResultSet-.md)\-Methode des [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts einen OutOfMemoryError verursacht, können Sie die Anzahl der abgerufenen Zeilen verringern, indem Sie die [setFetchSize](../content/setFetchSize-Method--SQLServerResultSet-.md)\-Methode des [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts aufrufen, um die Abrufgröße auf eine kleinere Zeilenanzahl festzulegen und ggf. sogar auf eine Zeile verringern. Sie können auch erzwingen, dass der Treiber keine Zeilen puffert, indem Sie vor dem Ausführen der Anweisung die [setResponseBuffering](../content/setResponseBuffering-Method--SQLServerStatement-.md)\-Methode des [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekts mit dem **adaptive**\-Parameter aufrufen. Da das Resultset nicht scrollfähig ist, verwirft der Treiber einen großen Spaltenwert, auf den die Anwendung mit einer der get\<Type\>Stream\-Methoden zugreift, wie bei schreibgeschützten Resultsets mit Vorwärtscursor, sobald er von der Anwendung gelesen wurde.  
  
## Siehe auch  
 [Verbessern von Leistung und Zuverlässigkeit mit dem JDBC-Treiber](../content/Improving-Performance-and-Reliability-with-the-JDBC-Driver.md)  
  
  