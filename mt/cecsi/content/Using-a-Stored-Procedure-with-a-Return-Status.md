---
title: "Verwenden von gespeicherten Prozeduren mit einem R&#252;ckgabestatus"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4b126e95-8458-41d6-af37-fc6662859f19
caps.latest.revision: 22
caps.handback.revision: 19
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
# Verwenden von gespeicherten Prozeduren mit einem R&#252;ckgabestatus
  Bei einer aufrufbaren gespeicherten [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Prozedur handelt es sich um eine Prozedur, die einen Status\- oder Ergebnisparameter zurückgibt. Damit wird normalerweise ermittelt, ob die gespeicherte Prozedur erfolgreich ausgeführt wurde oder fehlgeschlagen ist. [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] enthält die [SQLServerCallableStatement](../content/SQLServerCallableStatement-Class.md)\-Klasse, mit der Sie diese Art von gespeicherter Prozedur aufrufen und die zurückgegebenen Daten verarbeiten können.  
  
 Wenn Sie diese Art von gespeicherter Prozedur mit dem JDBC\-Treiber aufrufen, müssen Sie die `call`\-SQL\-Escapesequenz zusammen mit der [prepareCall](../content/prepareCall-Method--SQLServerConnection-.md)\-Methode der [SQLServerConnection](../content/SQLServerConnection-Class.md)\-Klasse verwenden. Die Syntax für die `call`\-Escapesequenz mit einem Rückgabestatusparameter lautet wie folgt:  
  
 `{[?=]call procedure-name[([parameter][,[parameter]]...)]}`  
  
> [!NOTE]  
>  Weitere Informationen zu SQL\-Escapesequenzen finden Sie unter [Verwenden von SQL-Escapesequenzen](../content/Using-SQL-Escape-Sequences.md).  
  
 Geben Sie die Rückgabestatusparameter beim Erstellen der `call` \-Escapesequenz mit dem Fragezeichen \(?\) an. das als Platzhalter für den Parameterwert fungiert, der von der gespeicherten Prozedur zurückgegeben wird. Um einen Wert für einen Rückgabestatusparameter anzugeben, müssen Sie vor dem Ausführen der gespeicherten Prozedur den Datentyp des Parameters mit der [registerOutParameter](../content/registerOutParameter-Method--SQLServerCallableStatement-.md)\-Methode der SQLServerCallableStatement\-Klasse angeben.  
  
> [!NOTE]  
>  Wenn der JDBC\-Treiber mit einer SQL Server\-Datenbank verwendet wird, handelt es sich bei dem Wert, der in der registerOutParameter\-Methode für den Rückgabestatusparameter angegeben wird, immer um einen integer\-Wert. Dies können Sie mit dem Datentyp **java.sql.Types.INTEGER** angeben.  
  
 Wenn Sie an die registerOutParameter\-Methode einen Wert für einen Rückgabestatusparameter übergeben, müssen Sie darüber hinaus nicht nur den Datentyp für den Parameter angeben, sondern auch die ordinale Position des Parameters im Aufruf der gespeicherten Prozedur. Für den Rückgabestatusparameter ist die ordinale Position immer 1, da es sich immer um den ersten Parameter im Aufruf der gespeicherten Prozedur handelt. Obwohl die SQLServerCallableStatement\-Klasse die Verwendung des Namens eines Parameters zum Angeben dieses Parameters unterstützt, können Sie für Rückgabestatusparameter nur die Ordnungspositionsnummer verwenden.  
  
 Erstellen Sie als Beispiel die folgende Prozedur in der [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank:  
  
```  
CREATE PROCEDURE CheckContactCity  
   (@cityName CHAR(50))  
AS  
BEGIN  
   IF ((SELECT COUNT(*)  
   FROM Person.Address  
   WHERE City = @cityName) > 1)  
   RETURN 1  
ELSE  
   RETURN 0  
END  
```  
  
 Diese gespeicherte Prozedur gibt abhängig davon, ob der im cityName\-Parameter angegebene Ort in der Person.Address\-Tabelle gefunden wurde, den Statuswert 1 oder 0 zurück.  
  
 Im folgenden Beispiel werden eine offene Verbindung zur [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)]\-Beispieldatenbank an die Funktion übergeben und die gespeicherte Prozedur "CheckContactCity" mit der [execute](../content/execute-Method--SQLServerStatement-.md)\-Methode aufgerufen:  
  
 [!CODE [JDBC#UsingSprocWithReturnStatus1](../CodeSnippet/SQLDrivers/jdbc#usingsprocwithreturnstatus1)]  
  
## Siehe auch  
 [Verwenden von Anweisungen mit gespeicherten Prozeduren](../content/Using-Statements-with-Stored-Procedures.md)  
  
  