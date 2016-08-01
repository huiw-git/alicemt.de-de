---
title: "setEncrypt-Methode (SQLServerDataSource)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - setEncrypt Method (SQLServerDataSource)
apilocation: 
  - setEncrypt Method (SQLServerDataSource)
apitype: Assembly
ms.assetid: 0c85a9c1-f27c-457e-8461-403cc03e2d17
caps.latest.revision: 22
caps.handback.revision: 21
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
# setEncrypt-Methode (SQLServerDataSource)
  Legt einen Wert vom Typ **Boolean** fest, mit dem angegeben wird, ob die encrypt\-Eigenschaft aktiviert ist.  
  
## Syntax  
  
```  
  
public void setEncypt(boolean encrypt)  
```  
  
#### Parameter  
 *encrypt*  
  
 **true**, wenn zwischen Client und [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] die Secure Sockets Layer \(SSL\)\-Verschlüsselung aktiviert ist. Andernfalls wird **false** verwendet.  
  
## Hinweise  
 Ist die encrypt\-Eigenschaft auf **true** festgelegt, wird von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] sichergestellt, dass [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] für alle zwischen Client und Server versendeten Daten die Secure Sockets Layer \(SSL\)\-Verschlüsselung verwendet, sofern auf dem Server ein Zertifikat installiert ist. Der Standardwert ist **false**.  
  
 Bei der Initiierung eines SSL\-Handshakes wird vom JDBC\-Treiber die Java Virtual Machine \(JVM\) erkannt, auf der er ausgeführt wird.  
  
 Wenn die encrypt\-Eigenschaft auf **true** festgelegt ist, verwendet [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] den JSSE\-Standardsicherheitsanbieter der JVM, um die SSL\-Verschlüsselung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] auszuhandeln. Der Standardsicherheitsanbieter unterstützt möglicherweise nicht alle erforderlichen Funktionen zum erfolgreichen Aushandeln der SSL\-Verschlüsselung. So ist es beispielsweise möglich, dass die im SSL\-Zertifikat für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwendete Größe des öffentlichen RSA\-Schlüssels vom Standardsicherheitsanbieter nicht unterstützt wird. In diesem Fall löst der Standardsicherheitsanbieter möglicherweise einen Fehler aus, wodurch der JDBC\-Treiber die Verbindung trennt. Führen Sie zum Beheben dieses Problems eine der folgenden Aktionen aus:  
  
-   Konfigurieren Sie [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] mit einem Serverzertifikat mit einem kleineren öffentlichen RSA\-Schlüssel.  
  
-   Konfigurieren Sie die JVM für die Verwendung eines anderen JSSE\-Sicherheitsanbieters in der Sicherheitseigenschaftendatei "\<java\-home\>\/lib\/security\/java.security".  
  
-   Verwenden Sie eine andere JVM.  
  
 Ist die encrypt\-Eigenschaft nicht angegeben oder auf **false** festgelegt, wird vom Treiber die Unterstützung der SSL\-Verschlüsselung durch [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] nicht erzwungen. Wenn die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz nicht für das Erzwingen der SSL\-Verschlüsselung konfiguriert ist, wird eine Verbindung ohne jegliche Verschlüsselung hergestellt. Wenn die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz für das Erzwingen der SSL\-Verschlüsselung konfiguriert ist, aktiviert [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] bei Ausführung auf einer ordnungsgemäß konfigurierten Java Virtual Machine \(JVM\) automatisch die SSL\-Verschlüsselung. Andernfalls wird die Verbindung getrennt, und der Treiber löst einen Fehler aus.  
  
## Siehe auch  
 [SQLServerDataSource-Elemente](../content/SQLServerDataSource-Members.md)   
 [SQLServerDataSource-Klasse](../content/SQLServerDataSource-Class.md)  
  
  