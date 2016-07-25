---
title: "Systemanforderungen f&#252;r den JDBC-Treiber"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 447792bb-f39b-49b4-9fd0-1ef4154c74ab
caps.latest.revision: 73
caps.handback.revision: 66
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
# Systemanforderungen f&#252;r den JDBC-Treiber
  Für den Datenzugriff von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] oder [!INCLUDE[ssAzure](../content/includes/ssAzure_md.md)] mittels [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] müssen folgende Komponenten auf Ihrem Computer installiert sein:  
  
-   [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)]  
  
     Im [Microsoft Download Center](http://www.microsoft.com/download/details.aspx?id=11774) stehen der Microsoft JDBC\-Treiber 6.0 \(Preview\), 4.2, 4.1 und 4.0 für SQL Server zum Download bereit.  
  
-   Java\-Laufzeitumgebung \(Java Runtime Environment, JRE\)  
  
## Anforderungen der Java\-Laufzeitumgebung  
 Ab Version 4.2 des Microsoft JDBC\-Treibers für SQL Server werden das Sun Java SE Development Kit \(JDK\) 8.0 und die Java\-Laufzeitumgebung \(JRE\) 8.0 unterstützt. Die Unterstützung für die Java Database Connectivity \(JDBC\) Spec\-API wurde nun auf die JDBC 4.1 und 4.2\-API ausgeweitet.  
  
 Ab Version 4.1 des Microsoft JDBC\-Treibers für SQL Server werden Sun Java SE Development Kit \(JDK\) 7.0 und die Java\-Laufzeitumgebung \(JRE\) 7.0 unterstützt.  
  
 Ab [!INCLUDE[jdbc_40](../content/includes/jdbc_40_md.md)] wurde die JDBC\-Treiberunterstützung für Java Database Connectivity \(JDBC\) Spec\-API auf die JDBC 4.0\-API ausgeweitet. Die JDBC 4.0\-API wurde als Teil des Sun Java SE Development Kits \(JDK\) 6.0 und der Java\-Laufzeitumgebung \(JRE\) 6.0 eingeführt. JDBC 4.0 ist eine Obermenge der JDBC 3.0\-API.  
  
 Bei der Bereitstellung von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] unter Windows\- und UNIX\-Betriebssystemen müssen Sie entsprechend eines der folgenden Installationspakete verwenden: *Sqljdbc\_ \< Version \> \_enu.exe* oder*Sqljdbc\_ \< Version \> \_enu.tar.gz*. Weitere Informationen zum Thema JDBC\-Treiberbereitstellung finden Sie im Thema [Bereitstellen des JDBC-Treibers](../content/Deploying-the-JDBC-Driver.md).  
  
 **Microsoft JDBC\-Treiber 6.0 \(Preview\) und 4.2 für SQL Server:**  
  
 Aus Gründen der Abwärtskompatibilität und zur Unterstützung möglicher Upgradeszenarien enthalten sowohl JDBC Driver 6.0 \(Preview\) als auch 4.2 in jedem Installationspaket vier JAR\-Klassenbibliotheken: **sqljdbc.jar**, **sqljdbc4.jar**, **sqljdbc41.jar** und **sqljdbc42.jar**. Hinweis: **sqljdbc.jar** und **sqljdbc4.jar** werden lediglich aus Gründen der Abwärtskompatibilität zur Verfügung gestellt und enthalten keine neuen Funktionen aus den Treiberversionen 6.0, 4.2 und 4.1.  
  
 Der JDBC\-Treiber ist für die Verwendung mit allen sowie die Unterstützung aller wichtigen Sun\-kompatiblen Java Virtual Machines konzipiert. Er wird jedoch nur mit der Sun\-Laufzeitumgebung 5.0, 6.0, 7.0 und 8.0 getestet.  
  
 Im Folgenden wird eine Übersicht über die Unterstützung durch die vier in den Microsoft JDBC\-Treibern 6.0 \(Vorschau\) und 4.2 für SQL Server enthaltenen JAR\-Dateien gegeben:  
  
|JAR|JDBC\-Versionskompatibilität|Empfohlene Java\-Version|Beschreibung|  
|---------|----------------------------------|------------------------------|------------------|  
|sqljdbc.jar|3.0|5|Erfordert die Java\-Laufzeitumgebung\(JRE\) Version 5.0.  Durch JRE 6.0 oder höher mit wird eine Ausnahme ausgelöst, wenn die Verbindung mit einer Datenbank hergestellt wird.<br /><br /> Wird nur aus Gründen der Abwärtskompatibilität bereitgestellt und enthält keine neuen Features aus den Versionen 4.1 und 4.2.|  
|sqljdbc4.jar|4.0|6|Erfordert die Java\-Laufzeitumgebung \(JRE\) Version 6.0 oder 7.0. Die Verwendung von JRE 5.0 löst eine Ausnahme aus.<br /><br /> Wird nur aus Gründen der Abwärtskompatibilität bereitgestellt und enthält keine neuen Features aus den Versionen 4.1 und 4.2.|  
|sqljdbc41.jar|4.1|7|Erfordert die Java\-Laufzeitumgebung\( JRE\) Version 7.0. Die Verwendung von JRE 6.0 löst eine Ausnahme aus.<br /><br /> Neue Funktionen in 6.0\- und 4.2\-Paketen schließen Folgendes mit ein: JDBC 4.1\-Kompatibilität und Massenkopieren<br /><br /> Darüber hinaus schließen im 6.0\-Paket neue Funktionen Folgendes mit ein: immer verschlüsselt und Internationalized Domain Name \(IDN\)|  
|sqljdbc42.jar|4.2|8|Erfordert die Java\-Laufzeitumgebung\(JRE\) Version 8.0. Die Verwendung von JRE 7.0 löst eine Ausnahme aus.<br /><br /> Neue Funktionen in 6.0\- und 4.2\-Paketen schließen Folgendes mit ein: JDBC 4.1 Compliance, JDBC 4.2 Compliance und Massenkopieren<br /><br /> Darüber hinaus schließen im 6.0\-Paket neue Funktionen Folgendes mit ein: immer verschlüsselt und Internationalized Domain Name \(IDN\)|  
  
 **Microsoft JDBC\-Treiber 4.1 für SQL Server:**  
  
 Zur Gewährleistung von Abwärtskompatibilität und möglichen Aktualisierungsszenarien enthalten der JDBC\-Treiber 4.1 drei JAR\-Klassenbibliotheken in jedem Installationspaket: **sqljdbc.jar**, **sqljdbc4.jar** und **sqljdbc41.jar**.  
  
> [!NOTE]  
>  **sqljdbc.jar, sqljdbc4.jar** werden lediglich aus Gründen der Abwärtskompatibilität zur Verfügung gestellt und enthalten keine neuen Funktionen der Version 4.1.  
  
|JAR|Beschreibung|  
|---------|------------------|  
|sqljdbc.jar|**sqljdbc.jar**\-Klassenbibliothek unterstützt JDBC 3.0.<br /><br /> **sqljdbc.jar**\-Klassenbibliothek erfordert die Java\-Laufzeitumgebung \(JRE\) der Version 5.0. Durch die Verwendung von **sqljdbc.jar** JRE 6.0 oder 7.0 mit wird eine Ausnahme ausgelöst, wenn die Verbindung mit einer Datenbank hergestellt wird. **Note:**  Der JDBC\-Treiber unterstützt keine JRE 1.4. Wenn Sie den JDBC\-Treiber verwenden, müssen Sie JRE 1.4 auf JRE 5.0 auf JRE 6.0 oder 7.0 aktualisieren. Es kann unter Umständen erforderlich sein, Ihre Anwendung neu zu kompilieren, weil diese möglicherweise nicht mit JDK 5.0 oder JDK 6.0 kompatibel ist. Weitere Informationen finden Sie in der Dokumentation auf der Website von Sun Microsystems.|  
|sqljdbc4.jar|**sqljdbc4.jar**\-Klassenbibliothek unterstützt die JDBC 4.0\-API. Sie enthält außerdem alle Funktionen von **sqljdbc.jar** sowie die neuen JDBC 4.0\-API\-Methoden.<br /><br /> **sqljdbc4.jar**\-Klassenbibliothek erfordert die Java\-Laufzeitumgebung \(JRE\) der Version 6.0 oder 7.0. Die Verwendung von **sqljdbc4.jar** JRE 5.0 löst eine Ausnahme aus. **Note:**  Verwenden Sie **sqljdbc4.jar**, wenn Ihre Anwendung JRE 6.0 oder 7.0 benötigt, selbst wenn Ihre Anwendung nicht auf JDBC 4.0\-API\-Funktionen zurückgreift.|  
|sqljdbc41.jar|**sqljdbc41.jar**\-Klassenbibliothek unterstützt die JDBC 4.0\-API. Sie enthält außerdem alle Funktionen von **sqljdbc4.jar** sowie die JDBC 4.0\-API\-Methoden. JDBC 4.1 wird nicht unterstützt \(löst eine Ausnahme aus: „SQLFeatureNotSupportedException“\).<br /><br /> **sqljdbc41.jar**\-Klassenbibliothek erfordert die Java\-Laufzeitumgebung \(JRE\) der Version 7.0. Die Verwendung von **sqljdbc41.jar** JRE 6.0 und 5.0 löst eine Ausnahme aus. **Note:**  Bei der Verwendung von **sqljdbc41.jar** muss Ihre Anwendung mit JDK 7.0 kompilieren können.|  
  
 Der JDBC\-Treiber ist für die Verwendung mit allen sowie die Unterstützung durch alle wichtigen Sun\-kompatiblen Java Virtual Machines konzipiert. Er wird jedoch nur mit der Sun\-Laufzeitumgebung 5.0, 6.0 und 7.0 getestet.  
  
 Im Folgenden wird eine Übersicht über die Unterstützung durch die drei in den Microsoft JDBC\-Treibern 6.0 \(Vorschau\) und 4.2 für SQL Server enthaltenen JAR\-Dateien gegeben:  
  
|JAR|JDBC\-Version|JRE \(kann ausgeführt werden\)|JDK \(kann kompiliert werden\)|  
|---------|-------------------|------------------------------------|------------------------------------|  
|sqljdbc.jar|3|5|5|  
|sqljdbc4.jar|4|7 6|6 5|  
|sqljdbc41.jar|4|7|7 6 5|  
  
 **Microsoft JDBC\-Treiber 4.0 für SQL Server:**  
  
 Aus Gründen der Abwärtskompatibilität und zur Unterstützung möglicher Upgradeszenarien enthält JDBC Driver in jedem Installationspaket zwei JAR\-Klassenbibliotheken: **sqljdbc.jar** und **sqljdbc4.jar**.  
  
|JAR|Beschreibung|  
|---------|------------------|  
|sqljdbc.jar|**sqljdbc.jar**\-Klassenbibliothek unterstützt JDBC 3.0.<br /><br /> **sqljdbc.jar**\-Klassenbibliothek erfordert die Java\-Laufzeitumgebung \(JRE\) der Version 5.0. Durch die Verwendung von **sqljdbc.jar** JRE 6.0 oder 7.0 mit wird eine Ausnahme ausgelöst, wenn die Verbindung mit einer Datenbank hergestellt wird. **Note:**  Der JDBC\-Treiber unterstützt keine JRE 1.4. Wenn Sie den JDBC\-Treiber verwenden, müssen Sie JRE 1.4 auf JRE 5.0 auf JRE 6.0 oder 7.0 aktualisieren. Es kann unter Umständen erforderlich sein, Ihre Anwendung neu zu kompilieren, weil diese möglicherweise nicht mit JDK 5.0 oder JDK 6.0 kompatibel ist. Weitere Informationen finden Sie in der Dokumentation auf der Website von Sun Microsystems. [!INCLUDE[jdbc_40](../content/includes/jdbc_40_md.md)] unterstützt JDK 7 nicht.|  
|sqljdbc4.jar|**sqljdbc4.jar**\-Klassenbibliothek unterstützt die JDBC 4.0\-API. Sie enthält außerdem alle Funktionen von **sqljdbc.jar** sowie die neuen JDBC 4.0\-API\-Methoden.<br /><br /> **sqljdbc4.jar**\-Klassenbibliothek erfordert die Java\-Laufzeitumgebung \(JRE\) der Version 6.0 oder 7.0. Die Verwendung von **sqljdbc4.jar** JRE 5.0 löst eine Ausnahme aus. **Note:**  Verwenden Sie **sqljdbc4.jar**, wenn Ihre Anwendung JRE 6.0 oder 7.0 benötigt, selbst wenn Ihre Anwendung nicht auf JDBC 4.0\-API\-Funktionen zurückgreift.|  
  
 Der JDBC\-Treiber ist für die Verwendung mit allen sowie die Unterstützung durch alle wichtigen Sun\-kompatiblen Java Virtual Machines konzipiert. Er wird jedoch nur mit der Sun\-Laufzeitumgebung 5.0, 6.0 und 7.0 getestet.  
  
## SQL Server\-Anforderungen  
 Der JDBC\-Treiber unterstützt Verbindungen mit Azure\-SQL\-Datenbank und SQL Server. Microsoft JDBC Driver 4.2 und 4.1 für SQL Server werden beginnend mit SQL Server 2008 unterstützt. Beim Microsoft JDBC Driver 4.0 für SQL Server ist Unterstützung ab SQL Server 2005 verfügbar.  
  
## Betriebssystemanforderungen  
 Der JDBC\-Treiber ist für die Verwendung mit einem Betriebssystem konzipiert, das die Java Virtual Machine \(JVM\) unterstützt. Offizellen Tests wurden jedoch nur die Betriebssysteme Sun Solaris und Windows unterzogen.  
  
## Unterstützte Sprachen  
 Der JDBC\-Treiber unterstützt alle [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Spaltensortierungen. Weiterführende Informationen zu den vom JDBC\-Treiber unterstützten Sortierungen finden Sie in [Internationale Funktionen des JDBC-Treibers](../content/International-Features-of-the-JDBC-Driver.md).  
  
 Weitere Informationen zu Sortierungen finden Sie unter „Arbeiten mit Sortierungen“ in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Onlinedokumentation.  
  
## Siehe auch  
 [Übersicht über den JDBC-Treiber](../content/Overview-of-the-JDBC-Driver.md)  
  
  