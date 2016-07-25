---
title: "setIntegratedSecurity-Methode (SQLServerDataSource)"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - SQLServerDataSource.setIntegratedSecurity
apilocation: 
  - sqljdbc.jar
apitype: Assembly
ms.assetid: 4c968ee4-b041-424a-bf69-cc2c4a4f51c6
caps.latest.revision: 12
caps.handback.revision: 12
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
# setIntegratedSecurity-Methode (SQLServerDataSource)
  Legt einen Wert vom Typ **Boolean** fest, mit dem angegeben wird, ob die integratedSecurity\-Eigenschaft aktiviert ist.  
  
## Syntax  
  
```  
  
public void setIntegratedSecurity(boolean enable)  
```  
  
#### Parameter  
 *enable*  
  
 **true**, wenn "integratedSecurity" aktiviert ist. Andernfalls wird **false** verwendet.  
  
## Hinweise  
 Legen Sie diese Eigenschaft auf "**true**" fest, wenn der Benutzer der Anwendung von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] anhand der Windows\-Anmeldeinformationen authentifiziert werden soll. Bei "**true**" wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] im Cache für Anmeldeinformationen des lokalen Computers nach Anmeldeinformationen gesucht, die bei der Anmeldung am Computer oder Netzwerk bereits angegeben wurden. Bei "**false**" müssen Benutzername und Kennwort angegeben werden.  
  
> [!NOTE]  
>  Diese Eigenschaft wird nur für [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Windows\-Betriebssysteme unterstützt.  
  
 Weitere Informationen zum Verwenden der integrierten Authentifizierung finden Sie unter [Erstellen der Verbindungs-URL](../content/Building-the-Connection-URL.md).  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  