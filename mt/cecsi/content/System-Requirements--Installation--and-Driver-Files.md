---
title: "Systemanforderungen, Installation und Treiberdateien"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d90fa182-1dab-4d6f-bd85-a04dd1479986
caps.latest.revision: 24
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
  - zh-cn
  - zh-tw
---
# Systemanforderungen, Installation und Treiberdateien
  Der ODBC Driver 11 for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] unterstützt Verbindungen mit SQL Server 2014, SQL Server 2012 R2, [!INCLUDE[ssKilimanjaro](../content/includes/ssKilimanjaro_md.md)], [!INCLUDE[ssKatmai](../content/includes/ssKatmai_md.md)]und [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)].  
  
 Der ODBC Driver 11 for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] on Windows kann auf einem Computer installiert werden, der auch eine oder mehrere Versionen von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Native Client besitzt.  
  
 Der ODBC Driver 13 \(Preview\) for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] unterstützt zusätzlich zu den oben genannten Servern auch SQL Server 2016 \(Preview\).  
  
 Der Treibername, den Sie in einer Verbindungszeichenfolge angeben, lautet **ODBC Driver 11 for SQL Server** \(oder **ODBC Driver 13 for SQL Server** bei Verwendung von ODBC Driver 13\).  
  
## Unterstützte Betriebssysteme  
 Sie können Programme mit dem ODBC-Treiber unter Windows auf den folgenden Windows-Betriebssysteme ausführen:  
  
-   Vista SP2  
  
-   Windows Server 2008 R2  
  
-   Windows Server 2012 R2  
  
-   Windows 7  
  
-   Windows 8  
  
 Wenn Sie Microsoft ODBC Driver 13 \(Preview\) for SQL Server verwenden, werden zusätzlich Windows 10, SQL Server 2014 und SQL Server 2016 \(Preview\) unterstützt.  
  
## Installieren von Microsoft ODBC Driver 13 \(Preview\) for SQL Server  
 Der ODBC Driver 13 \(Preview\) for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] on Windows wird installiert, wenn Sie „msodbcsql.msi“ durch [Herunterladen von Microsoft ODBC Driver 13 \(Preview\) for SQL Server on Windows](https://www.microsoft.com/en-us/download/details.aspx?id=50420) ausführen. Der ODBC-Treiber kann parallel mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Native Client installiert werden.  
  
 Wenn Sie msodbcsql.msi aufrufen, werden nur die Clientkomponenten standardmäßig installiert. Bei den Clientkomponenten handelt es sich um Dateien, die das Ausführen einer mithilfe des ODBC-Treibers entwickelten Anwendung unterstützen. Um die SDK-Komponenten zu installieren, geben Sie ADDLOCAL\=All in der Befehlszeile an. Beispiel:  
  
```  
msiexec /i msodbcsql.msi ADDLOCAL=ALL  
```  
  
 Standardmäßig installiert der ODBC-Treiber-Installer nur die Clientkomponenten. Um alle Komponenten \(Client- und SDK-Komponenten\) zu installieren, geben Sie in der Befehlszeile `ADDLOCAL=All` an. Beispiel:  
  
```  
msiexec /i msodbcsql.msi ADDLOCAL=ALL  
```  
  
 Geben Sie **IACCEPTMSODBCSQLLICENSETERMS\=YES** an, um den Bedingungen der Endbenutzerlizenz zuzustimmen, wenn Sie für die Installation eine der Optionen **\/passive**, **\/qn**, **\/qb** oder **\/qr** verwenden. Diese Option muss vollständig in Großbuchstaben angegeben werden. Zum Beispiel:  
  
```  
msiexec /quiet /passive /qn /i msodbcsql.msi IACCEPTMSODBCSQLLICENSETERMS=YES ADDLOCAL=ALL  
```  
  
 So führen Sie eine unbeaufsichtigte Deinstallation aus:  
  
```  
msiexec /quiet /passive /qn /uninstall msodbcsql.msi  
```  
  
 Wenn eine Anwendung den ODBC-Treiber verwendet, sollte die Anwendung angeben, dass sie vom Treiber über die Installationsoption APPGUID abhängig ist. Dies ermöglicht dem ODBC-Treiber-Installer, abhängige Anwendungen vor der Deinstallation zu melden. Um eine Abhängigkeit auf dem ODBC-Treiber anzugeben, legen Sie den APPGUID\-Befehlszeilenparameter auf Ihren Produktcode fest, wenn Sie den ODBC-Treiber unbeaufsichtigt installieren. \(Der Produktcode muss beim Packen des Setupprogramms für die Anwendung mit Microsoft Installer erstellt werden.\) Beispiel:  
  
```  
msiexec /i msodbcsql.msi APPGUID={ to be determined }  
```  
  
## Installieren von Microsoft ODBC Driver 11 for SQL Server  
 Der ODBC Driver 11 for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] on Windows wird installiert, wenn Sie msodbcsql.msi durch [Herunterladen von Microsoft ODBC Driver 11 for SQL Server on Windows](http://www.microsoft.com/download/details.aspx?id=36434)ausführen. Der ODBC-Treiber kann parallel mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Native Client installiert werden.  
  
 Wenn Sie msodbcsql.msi aufrufen, werden nur die Clientkomponenten standardmäßig installiert. Bei den Clientkomponenten handelt es sich um Dateien, die das Ausführen einer mithilfe des ODBC-Treibers entwickelten Anwendung unterstützen. Um die SDK-Komponenten zu installieren, geben Sie ADDLOCAL\=All in der Befehlszeile an. Beispiel:  
  
```  
msiexec /i msodbcsql.msi ADDLOCAL=ALL  
```  
  
 Standardmäßig installiert der ODBC-Treiber-Installer nur die Clientkomponenten. Um alle Komponenten \(Client- und SDK-Komponenten\) zu installieren, geben Sie in der Befehlszeile `ADDLOCAL=All` an. Beispiel:  
  
```  
msiexec /i msodbcsql.msi ADDLOCAL=ALL  
```  
  
 Geben Sie **IACCEPTMSODBCSQLLICENSETERMS\=YES** an, um den Bedingungen der Endbenutzerlizenz zuzustimmen, wenn Sie für die Installation eine der Optionen **\/passive**, **\/qn**, **\/qb** oder **\/qr** verwenden. Diese Option muss vollständig in Großbuchstaben angegeben werden. Zum Beispiel:  
  
```  
msiexec /quiet /passive /qn /i msodbcsql.msi IACCEPTMSODBCSQLLICENSETERMS=YES ADDLOCAL=ALL  
```  
  
 So führen Sie eine unbeaufsichtigte Deinstallation aus:  
  
```  
msiexec /quiet /passive /qn /uninstall msodbcsql.msi  
```  
  
 Wenn eine Anwendung den ODBC-Treiber verwendet, sollte die Anwendung angeben, dass sie vom Treiber über die Installationsoption APPGUID abhängig ist. Dies ermöglicht dem ODBC-Treiber-Installer, abhängige Anwendungen vor der Deinstallation zu melden. Um eine Abhängigkeit auf dem ODBC-Treiber anzugeben, legen Sie den APPGUID\-Befehlszeilenparameter auf Ihren Produktcode fest, wenn Sie den ODBC-Treiber unbeaufsichtigt installieren. \(Der Produktcode muss beim Packen des Setupprogramms für die Anwendung mit Microsoft Installer erstellt werden.\) Beispiel:  
  
```  
msiexec /i msodbcsql.msi APPGUID={0CC618CE-F36A-415E-84B4-FB1BFF6967E1}  
```  
  
## Befehlszeilentools: sqlcmd.exe und bcp.exe  
 Die Tools „bcp.exe“ und „sqlcmd.exe“ für die Verwendung mit Microsoft ODBC Driver 11 for SQL Server on Windows können unter [Herunterladen von bcp und sqlcmd für Microsoft ODBC Driver 11 for SQL Server on Windows](http://www.microsoft.com/download/details.aspx?id=36433)heruntergeladen werden. Der ODBC-Treiber ist Voraussetzung für die Installation von „Sqlcmd.exe“ und „Bcp.exe“.  
  
 „Bcp.exe“ und „sqlcmd.exe“ werden in „%PROGRAMFILES%\\Microsoft SQL Server\\Client SDK\\ODBC\\110\\Tools“ installiert.  
  
 Eine Anwendung, die BCP-Funktionen verwendet, muss den Treiber mit derselben Version angeben, der mit der für die Anwendungskompilierung verwendeten Headerdatei und Bibliothek ausgeliefert wurde.  
  
 Verwenden Sie z. B. beim Kompilieren einer ODBC-Treiber-Anwendung mit „msodbcsql11.lib“ und „msodbcsql.h“, „DRIVER\={ODBC Driver 11 für SQL Server}“ in der Verbindungszeichenfolge.  
  
## Komponenten von Microsoft ODBC Driver 13 \(Preview\) for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] on Windows  
 Der ODBC-Treiber für Windows enthält die folgenden Komponenten:  
  
|Komponente|Beschreibung|  
|---------------|-----------------|  
|msodbcsql13.dll|Die DLL\-Datei \(Dynamic-Link Library, DLL\), die die gesamte Funktionalität des Treibers enthält „msodbcsql13.dll“ wird in „%SYSTEMROOT%\\System32“ installiert.|  
|msodbcsqlr13.rll|Die begleitende Ressourcendatei für die Treiberbibliothek. „msodbcsqlr13.rll“ wird in „%SYSTEMROOT%\\System32\\1033“ installiert.|  
|s13ch\_msodbcsql.chm|Die Hilfedatei des Datenquellen-Assistenten-, die dokumentiert, wie eine Datenquelle aus dem ODBCDriver for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]erstellt werden kann. „s13chmsodbcsql\_msodbcsql.chm“ wird in „%SYSTEMROOT%\\System32\\1033“ installiert.|  
|msodbcsql.h|Die Header-Datei, die alle erforderlichen neuen Definitionen erhält, die für die Verwendung des ODBC Driver for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] on Windows benötigt werden.<br /><br /> **Hinweis:** Sie können nicht auf „msodbcsql.h“ und „odbcss.h“ im selben Programm verweisen.<br /><br /> „msodbcsql.h“ wird in „%PROGRAMFILES%\\Microsoft SQL Server\\Client SDK\\ODBC\\110\\SDK“ installiert.|  
|msodbcsql13.lib|Die Bibliotheksdatei, die für den Aufruf der **bcp**-Hilfsprogrammfunktionen benötigt wird. Diese Funktionen werden als Teil des ODBC Driver for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] on Windows bereitgestellt.<br /><br /> **Hinweis:** Wenn Sie in Ihrem Programm auf „msodbcsql13.lib“ verweisen, stellen Sie sicher, dass „msodbcsql13.dll“ in Ihrem Systempfad sowie im Systempfad der Dateien, die die Anwendungen verwenden, vorhanden ist.<br /><br /> „msodbcsql13.lib“ wird in „%PROGRAMFILES%\\Microsoft SQL Server\\Client SDK\\ODBC\\110\\SDK“ installiert.|  
  
## Komponenten von Microsoft ODBC Driver 11 for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] on Windows  
 Der ODBC-Treiber für Windows enthält die folgenden Komponenten:  
  
|Komponente|Beschreibung|  
|---------------|-----------------|  
|msodbcsql11.dll|Die DLL\-Datei \(Dynamic-Link Library, DLL\), die die gesamte Funktionalität des Treibers enthält „msodbcsql11.dll“ wird in „%SYSTEMROOT%\\System32“ installiert.|  
|msodbcsqlr11.rll|Die begleitende Ressourcendatei für die Treiberbibliothek. „msodbcsqlr11.rll“ wird in „%SYSTEMROOT%\\System32\\1033“ installiert.|  
|s11ch\_msodbcsql.chm|Die Hilfedatei des Datenquellen-Assistenten-, die dokumentiert, wie eine Datenquelle aus dem ODBCDriver for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]erstellt werden kann. „s11ch\_msodbcsql.chm“ wird in „%SYSTEMROOT%\\System32\\1033“ installiert.|  
|msodbcsql.h|Die Header-Datei, die alle erforderlichen neuen Definitionen erhält, die für die Verwendung des ODBC Driver for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] on Windows benötigt werden.<br /><br /> **Hinweis:** Sie können nicht auf „msodbcsql.h“ und „odbcss.h“ im selben Programm verweisen.<br /><br /> „msodbcsql.h“ wird in „%PROGRAMFILES%\\Microsoft SQL Server\\Client SDK\\ODBC\\110\\SDK“ installiert.|  
|msodbcsql11.lib|Die Bibliotheksdatei, die für den Aufruf der **bcp**-Hilfsprogrammfunktionen benötigt wird. Diese Funktionen werden als Teil des ODBC Driver for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] on Windows bereitgestellt.<br /><br /> **Hinweis:** Wenn Sie in Ihrem Programm auf „msodbcsql11.lib“ verweisen, stellen Sie sicher, dass „msodbcsql11.dll“ in Ihrem Systempfad sowie im Systempfad der Dateien, die die Anwendungen verwenden, vorhanden ist.<br /><br /> „msodbcsql11.lib“ wird in „%PROGRAMFILES%\\Microsoft SQL Server\\Client SDK\\ODBC\\110\\SDK“ installiert.|  
  
## Siehe auch  
 [Microsoft ODBC Driver for SQL Server on Windows](../content/Microsoft-ODBC-Driver-for-SQL-Server-on-Windows.md)  
  
  