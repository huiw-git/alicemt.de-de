---
title: "Installieren des Treiber-Managers"
ms.custom: na
ms.date: 06/09/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7c4b6fb4-f45a-4973-adb9-a4d83f0a2a7a
caps.latest.revision: 58
caps.handback.revision: 57
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
# Installieren des Treiber-Managers
Dieses Thema enthält Anweisungen zur Installation des unixODBC\-Treiber\-Managers für die Verwendung mit Microsoft ODBC Driver 13 \(Vorschau\) und 11 für SQL Server unter Linux.  
  
> [!IMPORTANT]  
> Löschen Sie alle Treiber\-Manager\-Pakete, die auf Ihrem Computer installiert sind, bevor Sie den unixODBC Treiber\-Manager installieren. Die Installation des unixODBC Treiber\-Managers kann einen Fehler eines vorhandenen Treiber\-Managers verursachen.  
  
## Installieren des Treiber\-Managers für Microsoft ODBC\-Treiber 13 \(Vorschau\) für SQL Server.  
  
**Verwenden des Installationsskripts**  
  
> [!IMPORTANT]  
> Stellen Sie sicher, dass Sie das richtige Paket von einem der folgenden Speicherorte heruntergeladen und die Version 13 ausgewählt haben.  
>   
> -   **Red Hat Enterprise Linux 7**\-Download: [Microsoft ODBC Driver 13 \(Preview\) and 11 for SQL Server \- Red Hat Linux](http://go.microsoft.com/fwlink/?LinkId=267321)  
> -   **SUSE Linux Enterprise 12** \-Download: [Microsoft ODBC Driver 13 and 11 Previews for SQL Server \- SUSE Linux](http://go.microsoft.com/fwlink/?LinkId=264916)  
> -   **Ubuntu 15.04** – Download: [Microsoft ODBC Driver 13 \(Preview\) for SQL Server – Ubuntu Linux](http://go.microsoft.com/fwlink/?LinkId=723136)  
  
Installieren des Treiber\-Managers:  
  
1.  Stellen Sie sicher, dass Sie die Root\-Berechtigung besitzen  
  
2.  Wechseln Sie zu dem Verzeichnis, in dem die [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ODBC\-Treiber\-Download die Datei mit dem Namen msodbcsql\-13.0.0.0.tar.gz platziert hat. Stellen Sie sicher, dass Sie die zu Ihrer Linux\-Version passende Datei „\*.tar.g“ besitzen. Führen Sie den folgenden Befehl aus, um die Dateien zu extrahieren: **tar xvzf msodbcsql\-13.0.0.0.tar.gz**  
  
3.  Wechseln Sie zum Verzeichnis „msodbcsql\-13.0.0.0.tar.gz“, und es wird eine Datei namens „build\_dm.sh“ angezeigt. Sie können build\_dm.sh ausführen, um den unixODBC Treiber\-Manager zu installieren.  
  
4.  Um eine Liste der verfügbaren Optionen anzuzeigen, führen Sie den folgenden Befehl aus: **.\/build\_dm.sh \-\-help**  
  
5.  Wenn Sie zur Installation bereit sind und Ihr Computer auf eine externe Website über FTP zugreifen kann, führen Sie den folgenden Befehl aus: **.\/build\_dm.sh**  
  
    Wenn Ihr Computer auf keine externe Website über FTP zugreifen kann, laden Sie unixODBC\-2.3.1.tar.gz herunter Sie können unixODBC\-2.3.1.tar.gz direkt unter dem folgenden Link herunterladen: **http:\/\/www.unixodbc.org\/pub\/unixODBC\/unixODBC\-2.3.1.tar.gz**. UnixODBC\-2.3.2\+ werden von dieser Version des [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] ODBC\-Treibers 13 für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] nicht unterstützt. Führen Sie den folgenden Befehl aus, um die Installation des unixODBC Treiber\-Managers zu starten: **.\/build\_dm.sh \-\-download\-url\=file:\/\/unixODBC\-2.3.1.tar.gz**  
  
6.  Geben Sie **YES** ein, um mit dem Entpacken der Dateien fortzufahren. Dieser Teil des Prozesses kann bis zu 5 Minuten in Anspruch nehmen.  
  
7.  Nachdem das Skript beendet wird, befolgen Sie die Anweisungen auf dem Bildschirm, um den unixODBC Treiber\-Manager zu installieren.  
  
Sie können nun den Treiber installieren. Weitere Informationen finden Sie unter [Den Microsoft ODBC Driver for SQL Server on Linux installieren](../content/Installing-the-Microsoft-ODBC-Driver-for-SQL-Server-on-Linux.md).  
  
**Manuelle Installation**  
  
Wenn das Skript für die Installation nicht abgeschlossen werden konnte, konfigurieren und erstellen Sie selbst den richtigen Treiber\-Manager.  
  
1.  Entfernen Sie alle älteren installierten Version von unixODBC \(z. B. unixODBC 2.2.13\). Führen Sie den folgenden Befehl auf Red Hat Enterprise Linux 6 aus: **yum remove unixODBC**. Auf SUSE Linux Enterprise: **zypper remove unixODBC**. Auf Ubuntu: **apt remove unixodbc**  
  
2.  Laden Sie den unixODBC\-2.3.1\-Treiber\-Manager unter dem folgenden Link herunter: **http:\/\/www.unixodbc.org\/pub\/unixODBC\/unixODBC\-2.3.1.tar.gz**. UnixODBC\-2.3.2\+ werden von dieser Version des [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] ODBC\-Treibers 13 für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] nicht unterstützt.  
  
3.  Führen Sie den folgenden Befehl auf Ihrem Linux\-Computer aus: **tar xvzf unixODBC\-2.3.1.tar.gz**.  
  
4.  Wechseln Sie zum Verzeichnis unixODBC\-2.3.1.  
  
5.  Bei einer Eingabeaufforderung führen Sie den Befehl **CPPFLAGS\="\-DSIZEOF\_LONG\_INT\=8"** aus.  
  
6.  Bei einer Eingabeaufforderung führen Sie den Befehl **export CPPFLAGS** aus.  
  
7.  Bei einer Eingabeaufforderung führen Sie den Befehl **".\/configure \-\-prefix\=\/usr \-\-libdir\=\/usr\/lib64 \-\-sysconfdir\=\/etc \-\-enable\-gui\=no \-\-enable\-drivers\=no \-\-enable\-iconv \-\-with\-iconv\-char\-enc\=UTF8 \-\-with\-iconv\-ucode\-enc\=UTF16LE"** aus.  
  
8.  Bei einer Eingabeaufforderung \(angemeldet als Root\-Benutzer\) führen Sie den Befehl **make** aus.  
  
9. Bei einer Eingabeaufforderung \(angemeldet als Root\-Benutzer\) führen Sie den Befehl **make install** aus.  
  
Sie können nun den Treiber installieren. Weitere Informationen finden Sie unter [Den Microsoft ODBC Driver for SQL Server on Linux installieren](../content/Installing-the-Microsoft-ODBC-Driver-for-SQL-Server-on-Linux.md).  
  
## Installieren des Treiber\-Managers für Microsoft ODBC Driver 11 \(Preview\) for SQL Server.  
  
**Verwenden des Installationsskripts**  
  
> [!IMPORTANT]  
> Diese Anleitungen beziehen sich auf „msodbcsql\-11.0.2270.0.tar.gz“, die Installationsdatei für Red Hat Linux. Wenn Sie die Preview für SUSE Linux installieren, ist der Dateiname msodbcsql 11.0.2260.0.tar.gz.  
  
Installieren des Treiber\-Managers:  
  
1.  Stellen Sie sicher, dass Sie die Root\-Berechtigung besitzen  
  
2.  Wechseln Sie zu dem Verzeichnis, in dem die [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ODBC\-Treiber\-Download die Datei mit dem Namen msodbcsql\-11.0.2270.0.tar.gz platziert hat. Stellen Sie sicher, dass Sie die zu Ihrer Linux\-Version passende Datei „\*.tar.g“ besitzen. Führen Sie den folgenden Befehl aus, um die Dateien zu extrahieren: **tar xvzf msodbcsql\-11.0.2270.0.tar.gz**  
  
3.  Wechseln Sie zum Verzeichnis msodbcsql\-11.0.2270.0.tar.gz und es wird eine Datei namens build\_dm.sh angezeigt. Sie können build\_dm.sh zum Installieren des unixODBC Treiber\-Managers ausführen.  
  
4.  Um eine Liste der verfügbaren Optionen anzuzeigen, geben Sie den folgenden Befehl ein: **.\/build\_dm.sh \-\-help**.  
  
5.  Wenn Sie zur Installation bereit sind und Ihr Computer auf eine externe Website über FTP zugreifen kann, führen Sie den folgenden Befehl aus: **.\/build\_dm.sh**.  
  
    Wenn Ihr Computer auf keine externe Website über FTP zugreifen kann, laden Sie unixODBC\-2.3.0.tar.gz herunter. Sie erhalten unixODBC\-2.3.0.tar.gz von [http:\/\/www.unixodbc.org](http://www.unixodbc.org/). Klicken Sie auf den Link **Herunterladen** auf der linken Seite der Seite, um zur Downloadseite zu wechseln. Klicken Sie dann auf den entsprechenden Link, um unixODBC\-2.3.0 \(nicht unixODBC\-2.3.1\) herunterzuladen. UnixODBC\-2.3.1 wird von dieser Version des [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] ODBC Driver 11 for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] nicht unterstützt. Führen Sie den folgenden Befehl aus, um die Installation des unixODBC Treiber\-Managers zu starten: **.\/build\_dm.sh \-\-download\-url\=file:\/\/unixODBC\-2.3.0.tar.gz**  
  
6.  Geben Sie **YES** ein, um mit dem Entpacken der Dateien fortzufahren. Dieser Teil des Prozesses kann bis zu 5 Minuten in Anspruch nehmen.  
  
7.  Nachdem das Skript beendet ist, befolgen Sie die Anweisungen auf dem Bildschirm, um den unixODBC Treiber\-Manager zu installieren.  
  
Sie können nun den Treiber installieren. Weitere Informationen finden Sie unter [Den Microsoft ODBC Driver for SQL Server on Linux installieren](../content/Installing-the-Microsoft-ODBC-Driver-for-SQL-Server-on-Linux.md).  
  
**Manuelle Installation**  
  
Wenn das Skript für die Installation nicht abgeschlossen werden konnte, konfigurieren und erstellen Sie selbst den richtigen Treiber\-Manager.  
  
1.  Entfernen Sie alle älteren installierten Versionen von unixODBC \(z. B. unixODBC 2.2.11\). Führen Sie den folgenden Befehl auf Red Hat Enterprise Linux 5 oder 6 aus: **yum remove unixODBC**. Auf SUSE Linux Enterprise: **zypper remove unixODBC**.  
  
2.  Wechseln Sie zu [http:\/\/www.unixodbc.org](http://www.unixodbc.org/). Klicken Sie auf den Link **Herunterladen** auf der linken Seite der Seite, um zur Downloadseite zu wechseln. Klicken Sie dann auf den entsprechenden Link, um die Datei „unixodbc\-2.3.0.tar.gz“ auf Ihrem Computer zu speichern. UnixODBC\-2.3.1 wird von dieser Version des [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] ODBC Driver 11 for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] nicht unterstützt.  
  
3.  Führen Sie den folgenden Befehl auf Ihrem Linux\-Computer aus: **tar xvzf unixODBC\-2.3.0.tar.gz**.  
  
4.  Wechseln Sie zum Verzeichnis „unixODBC\-2.3.0“.  
  
5.  Bei einer Eingabeaufforderung führen Sie den Befehl **CPPFLAGS\="\-DSIZEOF\_LONG\_INT\=8"** aus.  
  
6.  Bei einer Eingabeaufforderung führen Sie den Befehl **export CPPFLAGS** aus.  
  
7.  Bei einer Eingabeaufforderung führen Sie den Befehl **".\/configure \-\-prefix\=\/usr \-\-libdir\=\/usr\/lib64 \-\-sysconfdir\=\/etc \-\-enable\-gui\=no \-\-enable\-drivers\=no \-\-enable\-iconv \-\-with\-iconv\-char\-enc\=UTF8 \-\-with\-iconv\-ucode\-enc\=UTF16LE"** aus.  
  
8.  Bei einer Eingabeaufforderung \(angemeldet als Root\-Benutzer\) führen Sie den Befehl **make** aus.  
  
9. Bei einer Eingabeaufforderung \(angemeldet als Root\-Benutzer\) führen Sie den Befehl **make install** aus.  
  
Sie können nun den Treiber installieren. Weitere Informationen finden Sie unter [Den Microsoft ODBC Driver for SQL Server on Linux installieren](../content/Installing-the-Microsoft-ODBC-Driver-for-SQL-Server-on-Linux.md).  
  
## Siehe auch  
[Microsoft ODBC Driver for SQL Server on Linux](../content/Microsoft-ODBC-Driver-for-SQL-Server-on-Linux.md)  
  
