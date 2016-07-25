---
title: "&#196;ndern von Daten mit SQL-Anweisungen"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4704199b-c0ae-4c77-8a2e-6963715b4ffb
caps.latest.revision: 17
caps.handback.revision: 15
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
# &#196;ndern von Daten mit SQL-Anweisungen
    
## Ändern von Daten mit SQL\-Anweisungen  
 Mit der [executeUpdate](../content/executeUpdate-Method--SQLServerStatement-.md)\-Methode der [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse können Sie die in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank enthaltenen Daten über eine SQL\-Anweisung ändern. Die executeUpdate\-Methode übergibt die SQL\-Anweisung zur Verarbeitung an die Datenbank und gibt anschließend einen Wert zurück, der die Anzahl der betroffenen Zeilen angibt.  
  
 Sie müssen dazu zuerst mit der [createStatement](../content/createStatement-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse ein SQLServerStatement\-Objekt erstellen.  
  
 Im folgenden Beispiel werden eine offene Verbindung zur [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)][!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank an die Funktion übergeben, eine SQL\-Anweisung erstellt, die neue Daten zu der Tabelle hinzufügt, die Anweisung anschließend ausgeführt und der Rückgabewert angezeigt.  
  
 [!CODE [JDBC#UsingSQLToModifyData1](../CodeSnippet/SQLDrivers/jdbc#usingsqltomodifydata1)]  
  
> [!NOTE]  
>  Wenn Sie eine SQL\-Anweisung verwenden müssen, um die Daten in einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Datenbank zu ändern, müssen Sie die [executeUpdate](../content/executeUpdate-Method--SQLServerPreparedStatement-.md)\-Methode der [SQLServerPreparedStatement](../content/SQLServerPreparedStatement-Class.md)\-Klasse verwenden.  
>   
>  Wenn die Spalte, in die Daten eingefügt werden sollen, Sonderzeichen wie Leerzeichen enthält, müssen Sie die einzufügenden Werte angeben, auch wenn es sich um die Standardwerte handelt. Andernfalls schlägt die Einfügeoperation fehl.  
>   
>  Wenn der JDBC\-Treiber alle Updatezählungen zurückgeben soll, einschließlich der Updatezählungen, die von eventuell ausgelösten Triggern zurückgegeben werden, müssen Sie die lastUpdateCount\-Verbindungseigenschaft auf "false" setzen. Weitere Informationen zur lastUpdateCount\-Eigenschaft finden Sie unter [Einstellen der Verbindungseigenschaften](../content/Setting-the-Connection-Properties.md).  
  
## Siehe auch  
 [Verwenden von Anweisungen mit SQL](../content/Using-Statements-with-SQL.md)  
  
  