---
title: "Verwenden von gespeicherten Prozeduren ohne Parameter"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e9470a6d-a758-4c56-96ec-7b37139e36a7
caps.latest.revision: 18
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
# Verwenden von gespeicherten Prozeduren ohne Parameter
  Die einfachste Art einer gespeicherten [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Prozedur, die aufgerufen werden kann, enthält keine Parameter und gibt ein einziges Resultset zurück. [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] enthält die [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Klasse, mit der Sie diese Art von gespeicherter Prozedur aufrufen und die zurückgegebenen Daten verarbeiten können.  
  
 Wenn Sie mit dem JDBC\-Treiber eine gespeicherte Prozedur ohne Parameter aufrufen möchten, müssen Sie die `call` \-SQL\-Escapesequenz verwenden. Die Syntax für die `call` \-Escapesequenz ohne Parameter lautet wie folgt:  
  
 `{call procedure-name}`  
  
> [!NOTE]  
>  Weitere Informationen zu SQL\-Escapesequenzen finden Sie unter [Verwenden von SQL-Escapesequenzen](../content/Using-SQL-Escape-Sequences.md).  
  
 Erstellen Sie als Beispiel die folgende Prozedur in der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank:  
  
```  
CREATE PROCEDURE GetContactFormalNames   
AS  
BEGIN  
   SELECT TOP 10 Title + ' ' + FirstName + ' ' + LastName AS FormalName   
   FROM Person.Contact  
END  
```  
  
 Diese gespeicherte Prozedur gibt ein einzelnes Resultset zurück, das eine Datenspalte enthält, bei der es sich um eine Kombination aus Titel, Vorname und Nachname der ersten zehn Kontakte in der Tabelle "Person.Contact" handelt.  
  
 Im folgenden Beispiel werden eine offene Verbindung zur [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank an die Funktion übergeben und die gespeicherte Prozedur "GetContactFormalNames" mit der [executeQuery](../content/executeQuery-Method--SQLServerStatement-.md)\-Methode aufgerufen.  
  
```  
public static void executeSprocNoParams(Connection con) {  
   try {  
      Statement stmt = con.createStatement();  
      ResultSet rs = stmt.executeQuery("{call dbo.GetContactFormalNames}");  
  
      while (rs.next()) {  
         System.out.println(rs.getString("FormalName"));  
      }  
      rs.close();  
      stmt.close();  
   }  
   catch (Exception e) {  
      e.printStackTrace();  
   }  
}  
```  
  
## Siehe auch  
 [Verwenden von Anweisungen mit gespeicherten Prozeduren](../content/Using-Statements-with-Stored-Procedures.md)  
  
  