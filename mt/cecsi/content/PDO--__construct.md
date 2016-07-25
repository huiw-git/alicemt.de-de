---
title: "PDO::__construct"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3ee53aff-6fe4-44cd-a15b-51770c98c712
caps.latest.revision: 18
caps.handback.revision: 17
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
  - zh-cn
  - zh-tw
---
# PDO::__construct
Stellt eine Verbindung mit einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Datenbank her.  
  
## Syntax  
  
```  
  
PDO::__construct($dsn [,$username [,$password [,$driver_options ]]] )  
```  
  
#### Parameter  
*$dsn*: Eine Zeichenfolge mit dem Präfixnamen \(immer`sqlsrv`\), einem Doppelpunkt und dem Server-Schlüsselwort. Beispiel: `"sqlsrv:server=(local)"`. Sie können optional auch andere Schlüsselwörter angeben. Unter [Connection Options](../content/Connection-Options.md) finden Sie eine Beschreibung des Server-Schlüsselworts und anderer Verbindungsschlüsselwörter. Die gesamte *$dsn* wird in Anführungszeichen gesetzt, daher sollten die einzelnen Verbindungsschlüsselwörter nicht in separate Anführungszeichen gesetzt werden.  
  
*$username*: Optional. Eine Zeichenfolge, die den Namen des Benutzers enthält. Um eine Verbindung mithilfe der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Authentifizierung herzustellen, geben Sie die Anmelde-ID an. Um eine Verbindung mithilfe der Windows-Authentifizierung herzustellen, geben Sie `""`an.  
  
*$password*: Optional. Eine Zeichenfolge, die das Kennwort des Benutzers enthält. Um eine Verbindung mithilfe der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Authentifizierung herzustellen, geben Sie das Kennwort an. Um eine Verbindung mithilfe der Windows-Authentifizierung herzustellen, geben Sie `""`an.  
  
*$driver\_options*: optional. Sie können PDO-Treiber-Manager-Attribute und bestimmte [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]-Treiber-Attribute angeben – \-\-PDO::SQLSRV\_ATTR\_ENCODING, PDO::SQLSRV\_ATTR\_DIRECT\_QUERY. Ein ungültiges Attribut generiert keine Ausnahme. Ungültige Attribute generieren Ausnahmen, wenn sie mit [PDO::setAttribute](../Topic/PDO::setAttribute.md)spezifiziert werden.  
  
## Rückgabewert  
Gibt ein PDO-Objekt zurück. Wenn der Fehler auftritt, wird ein PDOException-Objekt zurückgegeben.  
  
## Ausnahmen  
PDOException  
  
## Hinweise  
Sie können ein Verbindungsobjekt schließen, indem Sie die Instanz auf NULL setzen.  
  
Nachdem eine Verbindung hergestellt wurde, wird PDO::errorCode 01000 anstelle von 00000 angezeigt.  
  
Wenn PDO::\_\_construct aus irgendeinem Grund fehlschlägt, wird eine Ausnahme ausgelöst, selbst wenn PDO::ATTR\_ERRMODE auf PDO::ERRMODE\_SILENT festgelegt ist.  
  
Unterstützung für PDO wurde in Version 2.0 von [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)]hinzugefügt.  
  
## Beispiel  
Dieses Beispiel zeigt, wie Sie eine Verbindung mit einem Server mithilfe der Windows-Authentifizierung herstellen und eine Datenbank angeben.  
  
```  
<?php  
   $c = new PDO( "sqlsrv:Server=(local) ; Database = AdventureWorks ", "", "", array(PDO::SQLSRV_ATTR_DIRECT_QUERY => true));   
  
   $query = 'SELECT * FROM Person.ContactType';   
   $stmt = $c->query( $query );   
   while ( $row = $stmt->fetch( PDO::FETCH_ASSOC ) ) {   
      print_r( $row );   
   }  
   $c = null;   
?>  
```  
  
## Beispiel  
Dieses Beispiel zeigt, wie Sie eine Verbindung mit einem Server herstellen und später die Datenbank festlegen.  
  
```  
<?php  
   $c = new PDO( "sqlsrv:server=(local)");  
  
   $c->exec( "USE AdventureWorks");  
   $query = 'SELECT * FROM Person.ContactType';  
   $stmt = $c->query( $query );  
   while ( $row = $stmt->fetch( PDO::FETCH_ASSOC ) ){  
      print_r( $row );  
   }  
   $c = null;  
?>  
```  
  
## Siehe auch  
[PDO-Klasse](../content/PDO-Class.md)  
[PDO](http://go.microsoft.com/fwlink/?LinkID=187441)  
  
