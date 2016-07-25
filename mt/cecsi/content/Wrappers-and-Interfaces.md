---
title: "Wrapper und Schnittstellen"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 27fc9b72-9f21-4728-abcb-5c015f28a6ab
caps.latest.revision: 12
caps.handback.revision: 11
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
# Wrapper und Schnittstellen
  [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] unterstützt Schnittstellen, mit denen Sie einen Proxy einer Klasse erstellen können, sowie Wrapper, die Ihnen über eine Proxyschnittstelle den Zugriff auf Erweiterungen der für [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] spezifischen JDBC\-API ermöglichen.  
  
## Wrapper  
 [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] unterstützt die java.sql.Wrapper\-Schnittstelle. Diese Schnittstelle bietet einen Mechanismus für den Zugriff auf Erweiterungen der für [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] spezifischen JDBC\-API über eine Proxyschnittstelle.  
  
 In der java.sql.Wrapper\-Schnittstelle sind zwei Methoden definiert: **isWrapperFor** und **unwrap**. Mit der **isWrapperFor**\-Methode wird überprüft, ob das angegebene Eingabeobjekt diese Schnittstelle implementiert. Die **unwrap**\-Methode gibt ein Objekt zurück, das diese Schnittstelle implementiert, um den Zugriff auf die für [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] spezifischen Methoden zu ermöglichen.  
  
 **isWrapperFor** und **unwrap**\-Methoden werden folgendermaßen verfügbar gemacht.  
  
-   [isWrapperFor-Methode &#40;SQLServerCallableStatement&#41;](../content/isWrapperFor-Method--SQLServerCallableStatement-.md)  
  
-   [unwrap-Methode &#40;SQLServerCallableStatement&#41;](../content/unwrap-Method--SQLServerCallableStatement-.md)  
  
-   [isWrapperFor-Methode &#40;SQLServerConnectionPoolDataSource&#41;](../content/isWrapperFor-Method--SQLServerConnectionPoolDataSource-.md)  
  
-   [unwrap-Methode &#40;SQLServerConnectionPoolDataSource&#41;](../content/unwrap-Method--SQLServerConnectionPoolDataSource-.md)  
  
-   [isWrapperFor-Methode &#40;SQLServerDataSource&#41;](../content/isWrapperFor-Method--SQLServerDataSource-.md)  
  
-   [unwrap-Methode &#40;SQLServerDataSource&#41;](../content/unwrap-Method--SQLServerDataSource-.md)  
  
-   [isWrapperFor-Methode &#40;SQLServerPreparedStatement&#41;](../content/isWrapperFor-Method--SQLServerPreparedStatement-.md)  
  
-   [unwrap-Methode &#40;SQLServerPreparedStatement&#41;](../content/unwrap-Method--SQLServerPreparedStatement-.md)  
  
-   [isWrapperFor-Methode &#40;SQLServerStatement&#41;](../content/isWrapperFor-Method--SQLServerStatement-.md)  
  
-   [unwrap-Methode &#40;SQLServerStatement&#41;](../content/unwrap-Method--SQLServerStatement-.md)  
  
-   [isWrapperFor-Methode &#40;SQLServerXADataSource&#41;](../content/isWrapperFor-Method--SQLServerXADataSource-.md)  
  
-   [unwrap-Methode &#40;SQLServerXADataSource&#41;](../content/unwrap-Method--SQLServerXADataSource-.md)  
  
## Schnittstellen  
 In [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] JDBC Driver 3.0 beginnend, stehen die Schnittstelle einem Anwendungsserver für den Zugriff auf eine treiberspezifische Methode über die zugehörige Klasse zur Verfügung. Der Anwendungsserver kann die Klasse durch Erstellen eines Proxy umschließen, wodurch die [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifische Funktionen über eine Schnittstelle verfügbar gemacht werden.[!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] unterstützt Schnittstellen, die über die [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifischen Methoden und Konstanten verfügen, sodass ein Anwendungsserver einen Proxy der Klasse erstellen kann.  
  
 Die Schnittstellen sind von Java\-Standardschnittstellen abgeleitet, damit Sie nach dem Entpacken dasselbe Objekt für den Zugriff auf die treiberspezifischen Funktionen oder die generischen [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-Funktionen verwenden können.  
  
 Die folgenden Schnittstellen wurden hinzugefügt:  
  
-   [ISQLServerCallableStatement](../content/ISQLServerCallableStatement-Interface.md)  
  
-   [ISQLServerConnection](../content/ISQLServerConnection-Interface.md)  
  
-   [ISQLServerDataSource](../content/ISQLServerDataSource-Interface.md)  
  
-   [ISQLServerPreparedStatement](../content/ISQLServerPreparedStatement-Interface.md)  
  
-   [ISQLServerResultSet](../content/ISQLServerResultSet-Interface.md)  
  
-   [ISQLServerStatement](../content/ISQLServerStatement-Interface.md)  
  
## Beispiel  
  
### Beschreibung  
 In diesem Beispiel wird veranschaulicht, wie der Zugriff auf eine [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]\-spezifische Funktion über ein DataSource\-Objekt erfolgt. Diese DataSource\-Klasse wurde möglicherweise von einem Anwendungsserver umschlossen. Für den Zugriff auf die JDBC\-Treiber\-spezifische Funktion oder Konstante können Sie die Datenquelle in eine ISQLServerDataSource\-Schnittstelle entpacken und die darin deklarierten Funktionen verwenden.  
  
### Code  
  
```  
import javax.sql.*;  
import java.sql.*;  
import com.microsoft.sqlserver.jdbc.*;  
  
public class UnWrapTest {  
   public static void main(String[] args) {  
      // This is a test.  This DataSource object could be something from an appserver   
      // which has wrapped the real SQLServerDataSource with its own wrapper  
      SQLServerDataSource ds = new SQLServerDataSource();  
      checkSendStringParametersAsUnicode(ds);  
   }  
  
   // Unwrap to the ISQLServerDataSource interface to access the getSendStringParametersAsUnicode function  
   static void checkSendStringParametersAsUnicode(DataSource ds) {  
      try {  
         final ISQLServerDataSource sqlServerDataSource = ds.unwrap(ISQLServerDataSource.class);  
         boolean sendStringParametersAsUnicode = sqlServerDataSource.getSendStringParametersAsUnicode();  
  
         System.out.println("Send string as parameter value is:-" + sendStringParametersAsUnicode);  
  
      } catch (SQLException sqlE) {  
         System.out.println("Exception:-" + sqlE);  
      }  
   }  
}  
```  
  
## Siehe auch  
 [Grundlegendes zu den Datentypen in JDBC Driver](../content/Understanding-the-JDBC-Driver-Data-Types.md)  
  
  