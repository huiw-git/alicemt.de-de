---
title: "Herstellen einer Verbindung mit sqlcmd"
ms.custom: na
ms.date: 06/09/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 61a2ec0d-1bcb-4231-bea0-cff866c21463
caps.latest.revision: 44
caps.handback.revision: 43
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
# Herstellen einer Verbindung mit sqlcmd
Das [sqlcmd](http://go.microsoft.com/fwlink/?LinkID=154481)\-Hilfsprogramm ist im [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] ODBC Driver for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] on Linux verfügbar.  
  
Die folgenden Befehle demonstrieren zuerst, wie die Windows\-Authentifizierung verwendet wird und dann, wie Sie die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Authentifizierung verwenden.  
  
```  
sqlcmd –E –Sxxx.xxx.xxx.xxx  
sqlcmd –Sxxx.xxx.xxx.xxx –Uxxx -Pxxx  
```  
  
## Verfügbare sqlcmd\-Optionen  
In der aktuellen Version sind die folgenden sqlcmd\-Optionen verfügbar:  
  
\-?  
Zeigen Sie sqlcmd\-Syntax an.  
  
\-a  
Fordern Sie eine Paketgröße an.  
  
\-b  
Beenden Sie den Batchauftrag, wenn ein Fehler auftritt.  
  
\-c *batch\_terminator*  
Geben Sie das Batchabschlusszeichen an.  
  
\-C  
Vertrauen Sie dem Server\-Zertifikat  
  
\-d *database\_name*  
Geben Sie eine USE *database\_name* Anweisung an, wenn Sie sqlcmd starten.  
  
\-D  
Bewirkt, dass der Wert, der an die \-S\-Option von sqlcmd übergeben wird, als Datenquellenname \(DSN\) interpretiert wird. Weitere Informationen finden Sie unter „DSN\-Unterstützung in sqlcmd und bcp“ am Ende dieses Themas.  
  
\-e  
Schreiben Sie Eingabeskripts in das Standardausgabegerät \(stdout\).  
  
\-E  
Verwenden Sie eine vertrauenswürdige Verbindung, integrierte Authentifizierung.  
  
Weitere Informationen zum Vornehmen von vertrauenswürdigen Verbindungen, die eine integrierte Authentifizierung von einem Linux\-Client verwenden:  
  
-   [Systemeigenes LDAP, systemeigene Kerberos und AD\-Dienste für Windows Server 2003 R2 und Schema für plattformübergreifende Identitätsverwaltung](http://www.interopsystems.com/LearningCenter/Native_LDAP_native_Kerberos_and_AD_services.htm)  
  
-   [Authentifizieren von Linux\-Clients mit Active Directory](http://technet.microsoft.com/magazine/2008.12.linux.aspx#id0060048)  
  
-   [Erstellen oder Hinzufügen von neuen Netzwerkalias an eine Netzwerkkarte \(NIC\) unter Linux](http://www.cyberciti.biz/faq/linux-creating-or-adding-new-network-alias-to-a-network-card-nic/)  
  
\-h *number\_of\_rows*  
Geben Sie die Anzahl der Zeilen an, die zwischen den Spaltenüberschriften geschrieben werden sollen.  
  
\-H  
Geben Sie den Namen einer Arbeitsstation an.  
  
\-i *input\_file*\[,*input\_file*\[,...\]\]  
Identifizieren Sie die Datei, die einen Batch mit SQL\-Anweisungen oder gespeicherten Prozeduren enthält.  
  
\-I  
Legen Sie die SET QUOTED\_IDENTIFIER\-Verbindungsoption auf ON fest.  
  
\-k  
Entfernen oder Ersetzen von Zeichen.  
  
**\-K** *application\_intent*  
Deklariert den Arbeitsauslastungstyp der Anwendung beim Herstellen einer Verbindung mit einem Server. Der einzige derzeit unterstützte Wert ist **ReadOnly**. Wenn **\-K** nicht angegeben wird, unterstützt sqlcmd keine Konnektivität mit einem sekundären Replikat in einer AlwaysOn\-Verfügbarkeitsgruppe. Weitere Informationen finden Sie unter [ODBC-Treiber mit der Linux-Unterstützung für hohe Verfügbarkeit, Notfallwiederherstellung](../content/ODBC-Driver-on-Linux-Support-for-High-Availability--Disaster-Recovery.md).  
  
> [!NOTE]  
> **\-K** wird in der CTP\-Version für SUSE Linux nicht unterstützt. Sie können jedoch das Schlüsselwort **ApplicationIntent\=ReadOnly** in einer DSN\-Datei angeben, die an sqlcmd übergeben wird. Weitere Informationen finden Sie unter „DSN\-Unterstützung in sqlcmd und bcp“ am Ende dieses Themas.  
  
\-l  
Geben Sie an, wie viele Sekunden bei der Herstellung einer Verbindung mit einem Server verstreichen dürfen, bevor für eine sqlcmd\-Anmeldung beim ODBC\-Treiber ein Timeout eintritt.  
  
\-m *error\_level*  
Steuern Sie, welche Fehlermeldungen an stdout gesendet werden.  
  
**\-M** *multisubnet\_failover*  
Geben Sie immer **\-M** an, wenn Sie eine Verbindung mit dem Verfügbarkeitsgruppenlistener einer [!INCLUDE[ssSQL11](../content/includes/ssSQL11_md.md)] Verfügbarkeitsgruppe oder einer [!INCLUDE[ssSQL11](../content/includes/ssSQL11_md.md)] Failoverclusterinstanz herstellen.**\-M** gewährleistet eine schnellere Erkennung und Verbindung mit dem \(gerade\) aktiven Server. Wenn **– M** nicht angegeben ist, so ist **\- M** deaktiviert. Weitere Informationen zu [!INCLUDE[ssHADR](../content/includes/ssHADR_md.md)] finden Sie unter [ODBC-Treiber mit der Linux-Unterstützung für hohe Verfügbarkeit, Notfallwiederherstellung](../content/ODBC-Driver-on-Linux-Support-for-High-Availability--Disaster-Recovery.md).  
  
> [!NOTE]  
> **\-M** wird in der CTP\-Version für SUSE Linux nicht unterstützt. Sie können jedoch das Schlüsselwort **MultiSubnetFailover\=Yes** in einer DSN\-Datei angeben, die an sqlcmd übergeben wird. Weitere Informationen finden Sie unter „DSN\-Unterstützung in sqlcmd und bcp“ am Ende dieses Themas.  
  
\-N  
Verschlüsseln Sie die Verbindung.  
  
\-o *output\_file*  
Identifizieren Sie die Datei, in welche die Ausgabe von sqlcmd geschrieben wird.  
  
\-p  
Gibt Leistungsstatistiken für jedes Resultset aus.  
  
\-P  
Geben Sie ein Benutzerkennwort an.  
  
\-q *commandline\_query*  
Führen Sie eine Abfrage aus, wenn sqlcmd startet, diese jedoch sqlcmd nicht beendet, nachdem die Ausführung der Abfrage abgeschlossen ist.  
  
\-Q *commandline\_query*  
Führen Sie eine Abfrage aus, wenn sqlcmd startet. sqlcmd wird beendet, wenn die Abfrage abgeschlossen ist.  
  
\-r  
Leitet die Fehlermeldungen an stderr.  
  
\-R  
Bewirkt, dass der Treiber die regionalen Einstellungen des Clients verwendet, um Währungs\-, Datums\- und Uhrzeitdaten in Zeichendaten zu konvertieren. Derzeit werden nur en\_US\-Formatierungen \(US\-Englisch\) verwendet.  
  
\-s *column\_separator\_char*  
Geben Sie das Spaltentrennzeichen an.  
  
\-S \[*protocol*:\] *server*\[**,** *port*\]  
Geben Sie die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz an, mit der eine Verbindung hergestellt wird. Oder, wenn \-D verwendet wird, einen DSN. Der ODBC\-Treiber unter Linux erfordert \-S. Für den ODBC\-Treiber unter Linux ist **tcp** das einzige gültige Protokoll.  
  
\-t *query\_timeout*  
Gibt an, wie viele Sekunden verstreichen, bevor für einen Befehl \(oder eine SQL\-Anweisung\) ein Timeout eintritt.  
  
\-u  
Geben Sie an, dass output\_file unabhängig vom Format von input\_file im Unicode\-Format gespeichert werden.  
  
\-U *login\_id*  
Geben Sie eine Benutzeranmelde\-ID an.  
  
\-V *error\_severity\_level*  
Steuern Sie den Schweregrad, der zur Festlegung der ERRORLEVEL\-Variable verwendet wird.  
  
\-w *column\_width*  
Geben Sie die Bildschirmbreite für die Ausgabe an.  
  
\-W  
Entfernen Sie nachfolgende Leerzeichen aus einer Spalte.  
  
\-x  
Variablenersetzung deaktivieren.  
  
\-X  
Befehle, Startskripts und Umgebungsvariablen deaktivieren.  
  
\-y *variable\_length\_type\_display\_width*  
Legen Sie die sqlcmd\-Skriptvariable SQLCMDMAXFIXEDTYPEWIDTH fest.  
  
\-Y *fixed\_length\_type\_display\_width*  
Legen Sie die sqlcmd\-Skriptvariable SQLCMDMAXVARTYPEWIDTH fest.  
  
In der aktuellen Version sind die folgenden sqlcmd\-Befehle verfügbar:  
  
-   \[:\]\!\!  
  
-   :Connect  
  
-   :Error  
  
-   \[:\]EXIT  
  
-   GO \[*count*\]  
  
-   :Help  
  
-   :List  
  
-   :Listvar  
  
-   :On Error  
  
-   :Out  
  
-   :Perftrace  
  
-   \[:\]QUIT  
  
-   :r  
  
-   :RESET  
  
-   :setvar  
  
## Nicht verfügbare sqlcmd\-Optionen  
In der aktuellen Version sind die folgenden sqlcmd\-Optionen nicht verfügbar:  
  
\-A  
Melden Sie sich über eine dedizierte Administratorverbindung \(Dedicated Administrator Connection, DAC\) in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] an. Weitere Informationen zur Herstellung einer dedizierten Administratorverbindung \(DAC\) finden Sie unter [Programmierrichtlinien](../content/Programming-Guidelines.md).  
  
\-f *code\_page*  
Geben Sie die Eingabe\- und Ausgabecodepages an.  
  
\-L  
Listen Sie die lokal konfigurierten Servercomputer sowie die Namen der Servercomputer auf, die Broadcastnachrichten über das Netzwerk senden.  
  
\-v  
Erstellen Sie eine sqlcmd\-Skriptvariable, die in einem sqlcmd\-Skript verwendet werden kann.  
  
Sie können die folgende alternative Methode verwenden:  
  
-   Schreiben Sie die Parameter in eine Datei. Diese können Sie dann an eine andere Datei anhängen. Dies hilft Ihnen dabei, eine Parameterdatei zu verwenden, um die Werte zu ersetzen. Erstellen Sie eine Datei namens a.sql \(die Parameterdatei\) mit dem folgenden Inhalt:  
  
    ```  
    :setvar ColumnName object_id  
    :setvar TableName sys.objects  
    ```  
  
-   Erstellen Sie eine Datei namens b.sql mit den Parametern für den Ersatz:  
  
    ```  
    select $(ColumnName) from $(TableName)  
    ```  
  
-   Kombinieren Sie in der Befehlszeile a.sql und b.sql in c.sql mit folgenden Befehle:  
  
    cat a.sql > c.sql  
  
    cat b.sql >> c.sql  
  
-   Ausführen von sqlcmd und c.sql als Eingabedatei:  
  
    slqcmd \-S<…> \-P<..> –U<..> \-I c.sql  
  
\-z *password*  
Kennwort ändern.  
  
\-Z *password*  
Kennwort ändern und beenden.  
  
In der aktuellen Version sind die folgenden sqlcmd\-Befehle nicht verfügbar:  
  
-   :ED  
  
-   :ServerList  
  
-   :XML  
  
## DSN\-Unterstützung in sqlcmd und bcp  
Sie können einen Datenquellennamen \(DSN\) statt eines Servernamens in der **sqlcmd** oder **bcp\-S** Option \(oder **sqlcmd**: Befehl verbinden\) angeben, wenn Sie \-D. angeben  \-D bewirkt, dass die Option \-S den angegebenen DSN abruft.**sqlcmd** oder **bcp** stellt eine Verbindung mit dem Server her, der in der DSN angegeben ist.  
  
System\-DSNs werden in der Datei odbc.ini im ODBC\-SysConfigDir\-Verzeichnis \(\/etc\/odbc.ini auf Standard\-Installationen\) gespeichert. Benutzer\-DSNs werden in odbc.in, im Basisverzeichnis eines Benutzers \(~ \/. odbc.ini\) gespeichert.  
  
Die folgenden Einträge werden in einem DSN unter Linux unterstützt:  
  
-   **ApplicationIntent\=ReadOnly**  
  
-   **Database\=***database\_name*  
  
-   **Driver\=ODBC Driver 11 for SQL Server**  
  
-   **MultiSubnetFailover\=Yes**  
  
-   **Server\=***server\_name\_or\_IP\_address*  
  
-   **Trusted\_Connection\=yes**|**no**  
  
In einem DSN ist nur der Eintrag DRIVER erforderlich. Für die Verbindung mit einem Server benötigt **sqlcmd** oder **bcp** allerdings den Wert im Eintrag SERVER.  
  
Wenn diese Option sowohl in der DSN als auch in der **sqlcmd**\- oder **bcp**\-Befehlszeile angegeben ist, überschreibt die Option **sqlcmd** oder **bcp** den Wert, der im DSN verwendet wird. Wenn der DSN z. B. einen DATABASE\-Eintrag enthält und **sqlcmd** Befehlszeile \-d enthält, wird der an **\-d** übergebene Wert verwendet. Wenn **Trusted\_Connection\=yes** im DSN angegeben ist, werden die Kerberos Authentifizierung sowie der Benutzername \(**–U**\) verwendet und das Kennwort \(**–P**\), falls vorhanden, ignoriert.  
  
Vorhandene Skripts, die **isql** aufrufen, können geändert werden, um **sqlcmd** zu verwenden, indem der folgende Alias definiert wird: **alias isql\="sqlcmd –D"**.  
  
## Siehe auch  
[Microsoft ODBC Driver for SQL Server on Linux](../content/Microsoft-ODBC-Driver-for-SQL-Server-on-Linux.md)  
  
