---
title: "Datenzugriffs-Ablaufverfolgung mit dem ODBC-Treiber unter Linux"
ms.custom: na
ms.date: 06/09/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3149173a-588e-47a0-9f50-edb8e9adf5e8
caps.latest.revision: 13
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
  - zh-cn
  - zh-tw
---
# Datenzugriffs-Ablaufverfolgung mit dem ODBC-Treiber unter Linux
Der Treiber unterstützt für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] unter Linux die Ein\- und Ausgangs\-Ablaufverfolgung von ODBC\-API.  
  
Um das Verhalten Ihrer Anwendung zu verfolgen, fügen Sie zuerst die folgende Zeile in die Datei „odbcinst.ini“ ein:  
  
```  
Trace=Yes  
```  
  
Starten Sie dann Ihre Anwendung mit „strace“. Zum Beispiel:  
  
```  
strace -t -f -o trace_out.txt executable  
```  
  
Entfernen Sie nach Abschluss der Ablaufverfolgung Ihrer Anwendung `Trace=Yes` aus der Datei „odbcinst.ini“, um Leistungseinbußen während der Ablaufverfolgung zu vermeiden.  
  
Die Ablaufverfolgung gilt für alle Anwendungen, die den Treiber in der Datei „odbcinst.ini“ verwenden. Um nicht alle Anwendungen zu verfolgen \(um z. B. zu verhindern, dass benutzerbezogene vertrauliche Informationen weitergegeben werden\), können Sie eine einzelne Anwendungsinstanz verfolgen, indem Sie den Speicherort einer privaten „odbcinst.ini“, mit der Umgebungsvariablen ODBCSYSINI bereitstellen. Zum Beispiel:  
  
```  
$ ODBCSYSINI=/home/myappuser myapp  
```  
  
In diesem Fall können Sie **Trace\=Yes** im \[ODBC Driver 11 for SQL Server\]\-Abschnitt „\/home\/myappuser\/odbcinst.ini.“ hinzufügen.  
  
## Bestimmen, welche ODBC.ini Datei der Treiber verwendet.  
Der ODBC\-Treiber für Linux weiß nicht, welche ODBC INI verwendet wird oder welcher Pfad zu der ODBC\-INI\-Datei führt. Daher kann der Treiber die ODBC INI\-Datei nicht verfolgen.  
  
Informationen darüber, welche ODBC.ini Datei verwendet wird, sind dennoch verfügbar, über die unixodbc\-Tools odbc\_config und odbcinst und über die Dokumentation des unixODBC Driver Manager.  
  
Beispielsweise druckt der folgende Befehl \(u. a.\) den Speicherort der System\- und Benutzer\-ODBC INI\-Dateien, die jeweils die System\- und Benutzer\-DSN enthalten.  
  
```  
$ odbcinst -j  
unixODBC 2.3.0  
DRIVERS............: /etc/odbcinst.ini  
SYSTEM DATA SOURCES: /etc/odbc.ini  
FILE DATA SOURCES..: /etc/ODBCDataSources  
USER DATA SOURCES..: /home/odbcuser/.odbc.ini  
SQLULEN Size.......: 8  
SQLLEN Size........: 8  
SQLSETPOSIROW Size.: 8  
```  
  
Die [unixODBC\-Dokumentation](http://www.unixodbc.org/doc/UserManual/) erläutert, wie die DSS Entscheidung des Benutzers im Vergleich zur System\-DSN Entscheidung hergestellt wird. Dies gilt insbesondere in folgenden Fällen:  
  
Benutzer\-DSN Dies sind Ihre persönlichen Datenquellen. Sie können neue hinzufügen, vorhandene entfernen und vorhandene konfigurieren. Benutzer\-DSN\-Informationen werden an einem geheimen Ort gespeichert, auf den nur Sie zugreifen können. Trennen Sie Ihre Benutzer\-DSNs von anderen Benutzer\-DSNs, dies ermöglicht Ihnen viel Flexibilität und Kontrolle über das Erstellen von und Arbeiten mit Datenquellen, die nur für Sie wichtig sind.  
  
System\-DSN Diese werden vom Systemadministrator erstellt. Sie funktionieren ähnlich wie die Benutzer\-DSNs, jedoch mit drei wichtigen Unterschieden:  
  
-   Nur der Systemadministrator kann System\-DSNs hinzufügen, entfernen und konfigurieren.  
  
-   System\-DSNs werden nur verwendet, wenn der DSN nicht als Benutzer\-DSN vorhanden ist. Anders ausgedrückt: Ihr Benutzer\-DSN hat Vorrang gegenüber dem System\-DSN.  
  
-   Alle teilen sich die gleiche Liste von System\-DSNs.  
  
