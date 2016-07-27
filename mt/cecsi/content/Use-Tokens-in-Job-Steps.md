---
title: "Verwenden von Token in Auftragsschritten"
ms.custom: na
ms.date: 07/25/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 105bbb66-0ade-4b46-b8e4-f849e5fc4d43
caps.latest.revision: 4
caps.handback.revision: 3
manager: jhubbard
translation.priority.mt: 
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
# Verwenden von Token in Auftragsschritten
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent können Sie mithilfe von Token in [!INCLUDE[tsql](../content/includes/tsql_md.md)] auftragsschrittskripts. Durch die Verwendung von Token verfügen Sie beim Schreiben von Auftragsschritten über dieselbe Flexibilität, die die Verwendung von Variablen beim Schreiben von Softwareprogrammen bietet. Die von Ihnen in ein Auftragsschrittskript eingefügten Token werden vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent zur Ausführungszeit ersetzt, bevor der Auftragsschritt vom [!INCLUDE[tsql](../content/includes/tsql_md.md)]-Subsystem ausgeführt wird.  
  
> [!IMPORTANT]  
> Mit [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] Service Pack 1 wurde die Syntax der Token für die Arbeitsschritte des [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agents geändert. Damit Auftragsschritte fehlerfrei ausgeführt werden können, müssen alle in Auftragsschritten verwendete Token von einem Escapemakro begleitet werden. Das Verwenden von Escapemakros und das Aktualisieren von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Auftragsschritten, in denen Token verwendet werden, wird in den folgenden Abschnitten "Grundlegendes zum Verwenden von Token", "[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Token und -Makros" und "Aktualisieren von Auftragsschritten für die Verwendung von Makros" beschrieben. Außerdem wurde auch die [!INCLUDE[ssVersion2000](../content/includes/ssVersion2000_md.md)]-Syntax, in der zur Auszeichnung von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Auftragsschritten eckige Klammern verwendet wurden (z.&amp;nbsp;B. "`[DATE]`") geändert. Jetzt müssen Sie Tokennamen in runde Klammern einschließen und ein Dollarzeichen (`$`) an den Anfang der Tokensyntax setzen. Zum Beispiel:  
>   
> `$(ESCAPE_`*Makroname*`(DATE))`  
  
## Grundlegendes zum Verwenden von Token  
  
> [!IMPORTANT]  
> Jeder Windows-Benutzer mit Schreibberechtigungen für das Windows-Ereignisprotokoll kann auf Auftragsschritte zugreifen, die durch [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Warnungen oder WMI-Warnungen aktiviert werden. Zur Vermeidung dieses Sicherheitsrisikos sind [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Tokens, die in von Warnungen aktivierten Aufträgen verwendet werden können, standardmäßig deaktiviert. Diese Token werden: **ein\-DBN**, **ein\-SVR**, **ein\-ERR**, **ein\-Schweregrad**, **ein\-MSG**., und **WMI (***Eigenschaft***)**. Beachten Sie, dass in dieser Version die Verwendung von Token auf alle Warnungen ausgeweitet ist.  
>   
> Wenn Sie diese Token verwenden müssen, stellen Sie zuvor sicher, dass ausschließlich Mitglieder von vertrauenswürdigen Windows-Sicherheitsgruppen, wie der Administratorengruppe, über Schreibberechtigungen für das Ereignisprotokoll des Computers verfügen, auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeführt wird. Klicken Sie dann mit der rechten Maustaste\-Klicken Sie auf **SQL Server-Agent** Wählen Sie im Objekt-Explorer **Eigenschaften**, und klicken Sie auf die **Warnungssystem** Seite **Token für alle Auftragsantworten auf Warnungen ersetzen** zum Aktivieren dieser Token.  
  
[!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent-token-Ersatz ist einfach und effizient: [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent einen genaues Zeichenfolgenliteral-Wert für das Token ersetzt. Alle Token werden Fall\-vertrauliche. Dies muss in den Auftragsschritten berücksichtigt werden, damit die verwendeten Token richtig angegeben werden oder die Ersatzzeichenfolge in den richtigen Datentyp konvertiert wird.  
  
Mit der folgenden Anweisung können Sie z.&amp;nbsp;B. den Namen der Datenbank in einem Auftragsschritt drucken:  
  
`PRINT N'Current database name is $(ESCAPE_SQUOTE(A-DBN))' ;`  
  
In diesem Beispiel die **ESCAPE-\_SQUOTE** Makro eingefügt wird die **ein\-DBN** token. Zur Laufzeit die **ein\-DBN** Token mit den entsprechenden Datenbanknamen ersetzt werden. Das Escapemakro umgeht alle einfachen Anführungszeichen, die möglicherweise unbeabsichtigt in der Zeichenfolge, durch die das Token ersetzt werden soll, übergeben werden. [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent wird ein einfaches Anführungszeichen durch zwei einfache Anführungszeichen in der endgültigen Zeichenfolge ersetzt.  
  
Wenn beispielsweise als Ersatz für das Token die Zeichenfolge `AdventureWorks2012'SELECT @@VERSION --` übergeben wird, wird im [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Auftragsschritt der folgende Befehl ausgeführt:  
  
`PRINT N'Current database name is AdventureWorks2012''SELECT @@VERSION --' ;`  
  
In diesem Fall wird die eingefügte Anweisung `SELECT @@VERSION` nicht ausgeführt. Stattdessen wird durch das überzählige einfache Anführungszeichen der Server veranlasst, die eingefügte Anweisung als Zeichenfolge zu analysieren. Wenn die Zeichenfolge, durch die das Token ersetzt werden soll, keine einfachen Anführungszeichen enthält, werden keine Zeichen umgangen, und der Auftragsschritt mit dem Token wird wie beabsichtigt ausgeführt.  
  
Verwenden Sie zum Debuggen der Tokenverwendung in Auftragsschritten Druckanweisungen, wie z.&amp;nbsp;B. `PRINT N'$(ESCAPE_SQUOTE(SQLDIR))'`, und speichern Sie die Auftragsschrittausgabe in einer Datei oder Tabelle. Verwenden der **Erweitert** auf der Seite der **Auftragsschritt-Eigenschaften** Dialogfeld Geben Sie einen Auftragsschritt ausgeben, Datei oder Tabelle.  
  
## SQL Server-Agent-Token und -Makros  
In der folgenden Tabelle sind die vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent unterstützten Token und Makros aufgelistet und beschrieben.  
  
### SQL Server-Agent-Token  
  
|Token|Beschreibung|  
|---------|---------------|  
|**(A\-DBN)**|Datenbankname. Wenn der Auftrag durch eine Warnung ausgeführt wird, ersetzt der Wert des Datenbanknamens dieses Token im Auftragsschritt automatisch.|  
|**(A\-SVR)**|Servername. Wenn der Auftrag durch eine Warnung ausgeführt wird, ersetzt der Wert des Servernamens dieses Token im Auftragsschritt automatisch.|  
|**(A\-ERR)**|Die Fehlernummer. Wenn der Auftrag durch eine Warnung ausgeführt wird, ersetzt der Wert der Fehlernummer dieses Token im Auftragsschritt automatisch.|  
|**(A\-SCHWEREGRAD)**|Fehlerschweregrad. Wenn der Auftrag durch eine Warnung ausgeführt wird, ersetzt der Wert des Fehlerschweregrads dieses Token im Auftragsschritt automatisch.|  
|**(A\-MSG)**|Meldungstext. Wenn der Auftrag durch eine Warnung ausgeführt wird, ersetzt der Wert des Meldungstexts dieses Token im Auftragsschritt automatisch.|  
|**(AGENT\_AUFTRAG\_NAME)**|Der Name des Auftrags.|  
|**(AGENT\_SCHRITT\_NAME)**|Der Name des Schrittes.|  
|**(DATE)**|Das aktuelle Datum (im Format YYYYMMDD).|  
|**(INST)**|Der Instanzname. Für eine Standardinstanz erhält dieses Token den Standardinstanznamen: MSSQLSERVER.|  
|**(JOBID)**|Auftrags-ID.|  
|**(MACH)**|Computername.|  
|**(MSSA)**|Name des Master-SQLServerAgent-Diensts.|  
|**(OSCMD)**|Präfix des Programms zur Ausführung von **CmdExec** Auftragsschritten.|  
|**(SQLDIR)**|Verzeichnis, in dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] installiert ist. Dieser Wert ist standardmäßig "c:"\\Program Files\\Microsoft SQL Server\\MSSQL.|  
|**(SQLLOGDIR)**|Token-Ersatz für die SQL Server Ordner Fehlerprotokollpfad – z. B. $(ESCAPE\_SQUOTE(SQLLOGDIR)).|  
|**(STEPCT)**|Die Angabe, wie oft dieser Schritt ausgeführt wurde (ohne Abbrüche). Mit diesem Token kann der Schrittbefehl den Abbruch einer aus mehreren Schritten bestehenden Schleife erzwingen.|  
|**(STEPID)**|Schritt-ID.|  
|**(SRVR)**|Name des Computers, auf dem [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ausgeführt wird. Wenn es sich bei der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Instanz um eine benannte Instanz handelt, ist auch der Name der Instanz angegeben.|  
|**(TIME)**|Die aktuelle Zeit (im Format HHMMSS).|  
|**(STRTTM)**|Uhrzeit (im Format HHMMSS), zu der die Ausführung des Auftrags begonnen hat.|  
|**(STRTDT)**|Datum (im Format YYYYMMDD), an dem die Ausführung des Auftrags begonnen hat.|  
|**(WMI (***Eigenschaft***))**|Bei Aufträgen, die als Antwort auf WMI-Warnungen ausgeführt, der Wert der Eigenschaft gemäß der *Eigenschaft*. Z. B. `$(WMI(DatabaseName))` liefert den Wert der **DatabaseName** -Eigenschaft für das WMI-Ereignis, die Ausführung die Warnung verursacht hat.|  
  
### SQL Server-Agent-Escapemakros  
  
|Escapemakros|Beschreibung|  
|-----------------|---------------|  
|**$(ESCAPE\_SQUOTE (***Token\_Name***))**|Umgeht einfache Anführungszeichen (') in der Token-Ersetzungszeichenfolge. Ein einfaches Anführungszeichen wird durch zwei einfache Anführungszeichen ersetzt.|  
|**$(ESCAPE\_DQUOTE (***Token\_Name***))**|Umgeht doppelte Anführungszeichen (") in der Token-Ersetzungszeichenfolge. Ein doppeltes Anführungszeichen wird durch zwei doppelte Anführungszeichen ersetzt.|  
|**$(ESCAPE\_RBRACKET (***Token\_Name***))**|Umgeht rechte eckige Klammern (]) in der Token-Ersetzungszeichenfolge. Ersetzt jede rechte eckige Klammer durch zwei rechte eckige Klammern.|  
|**$(ESCAPE\_NONE (***Token\_Name***))**|Ersetzt Token, ohne irgendein Zeichen in der Zeichenfolge zu umgehen. Dieses Makro wird zur Unterstützung der Abwärtskompatibilität in Umgebungen bereitgestellt, in denen Token-Ersetzungszeichenfolgen nur von vertrauenswürdigen Benutzern erwartet werden. Weitere Informationen finden Sie weiter unten im Abschnitt zum Aktualisieren von Auftragsschritten für die Verwendung von Makros.|  
  
## Aktualisieren von Auftragsschritten für die Verwendung von Makros  
Seit [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] Service Pack 1 können Auftragsschritte, die Token ohne Escapemakros enthalten, nicht ausgeführt werden. In diesen Fällen wird eine Fehlermeldung zurückgegeben, die darauf hinweist, dass der Auftragsschritt ein oder mehrere Token enthält, die mit einem Makro versehen werden müssen, bevor der Auftrag ausgeführt werden kann.  
  
Ein Skript erfolgt mit [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] Knowledge Base-Artikel 915845: [SQL Server-Agent-Auftrag Schritte, dass verwenden Token nicht in SQL Server 2005 Service Pack 1](http://support.microsoft.com/kb/915845). Sie können dieses Skript verwenden, alle Ihre Auftragsschritte aktualisieren, die Token mit den **ESCAPE-\_NONE** Makro. Nach dem verwenden dieses Skripts wird empfohlen, dass Sie die Auftragsschritte, die beim Verwenden von Token werden so bald wie möglich überprüfen, und Ersetzen Sie die **ESCAPE\_NONE** Makro mit einem escapemakro, die für den Kontext des Auftragsschritts geeignet ist.  
  
Die folgende Tabelle beschreibt, wie die symbolische Ersetzung von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent behandelt wird. Um die tokenersetzung zu aktivieren oder deaktivieren, mit der rechten Maustaste\-Klicken Sie auf **SQL Server-Agent** Wählen Sie im Objekt-Explorer **Eigenschaften**, auf die **Warnungssystem** Aktivieren oder Deaktivieren der **Token für alle Auftragsantworten auf Warnungen ersetzen** das Kontrollkästchen.  
  
|Tokensyntax|Tokenersetzung durch Warnungen aktiviert|Tokenersetzung durch Warnungen deaktiviert|  
|----------------|------------------------------|-------------------------------|  
|ESCAPE-Makro verwendet|Alle Token in Auftragsschritten werden erfolgreich ersetzt.|Durch Warnungen aktivierte Token werden nicht ersetzt. Diese Token werden **ein\-DBN**, **ein\-SVR**, **ein\-ERR**, **ein\-Schweregrad**, **ein\-MSG**, und **WMI (***Eigenschaft***)**. Andere, statische Token werden erfolgreich ersetzt.|  
|Kein ESCAPE-Makro verwendet|Alle Auftragsschritte mit Token werden nicht ausgeführt.|Alle Auftragsschritte mit Token werden nicht ausgeführt.|  
  
## Beispiele für Updates der Tokensyntax  
  
### A. Verwenden von Token in nicht\-geschachtelten Zeichenfolgen  
Das folgende Beispiel zeigt, wie Sie eine einfache nicht aktualisieren\-Skript mit dem entsprechenden escapemakro geschachtelt. Vor dem Ausführen des Updateskripts verwendet das folgende Auftragsschrittskript ein Auftragsschritttoken, um den entsprechenden Datenbanknamen zu drucken:  
  
`PRINT N'Current database name is $(A-DBN)' ;`  
  
Nach dem Ausführen des Updateskripts wird vor dem `ESCAPE_NONE`-Token ein `A-DBN`-Makro eingefügt. Da die Druckzeichenfolge durch einfache Anführungszeichen begrenzt wird, müssen Sie den Auftragsschritt aktualisieren, indem Sie das `ESCAPE_SQUOTE`-Makro folgendermaßen einfügen:  
  
`PRINT N'Current database name is $(ESCAPE_SQUOTE(A-DBN))' ;`  
  
### B. Verwenden von Token in geschachtelten Zeichenfolgen  
In Auftragsschritten, in denen Token in geschachtelten Zeichenfolgen oder Anweisungen verwendet werden, sollten die geschachtelten Anweisungen als Einzelanweisungen neu geschrieben werden, bevor die entsprechenden Escapemakros eingefügt werden.  
  
Betrachten Sie z.&amp;nbsp;B. den folgenden Auftragsschritt, der das Token `A-MSG` verwendet und nicht mit einem Escapemakro aktualisiert wurde:  
  
`PRINT N'Print ''$(A-MSG)''' ;`  
  
Nach dem Ausführen des Updateskripts wird mit dem Token ein `ESCAPE_NONE`-Makro eingefügt. In diesem Fall müssten Sie das Skript jedoch ohne Verwenden von Schachtelungen folgendermaßen neu schreiben und das `ESCAPE_SQUOTE`-Makro einfügen, damit die in der Token-Ersetzungszeichenfolge möglicherweise übergebenen Begrenzungszeichen richtig umgangen werden:  
  
<pre>Deklarieren Sie @msgString nvarchar(max)  
SET @msgString = ' $(ESCAPE_SQUOTE(A-MSG))'  
SET @msgString = QUOTENAME(@msgString,''')  
Drucken von N'Print ' + @msgString;</pre>  
  
Beachten Sie auch, dass in diesem Beispiel mit der Funktion QUOTENAME das Anführungszeichen festgelegt wird.  
  
### C. Verwenden von Token mit der ESCAPESEQUENZ\_NONE-Makro  
Das folgende Beispiel ist Teil eines Skripts, mit dem die Auftrags-ID (`job_id`) aus der `sysjobs`-Tabelle abgerufen wird und mithilfe des `JOBID`-Tokens die zuvor im Skript als binärer Datentyp deklarierte `@JobID`-Variable aufgefüllt wird. Beachten Sie, dass mit dem `ESCAPE_NONE`-Token das `JOBID`-Makro verwendet wird, da für binäre Datentypen keine Begrenzungszeichen erforderlich sind. In diesem Fall muss der Auftragsschritt nach Ausführen des Updateskripts nicht aktualisiert werden.  
  
<pre>Wählen Sie * aus msdb.dbo.sysjobs  
WHERE @JobID = CONVERT (vom Datentyp Uniqueidentifier und $(ESCAPE_NONE(JOBID)));</pre>  
  
## Siehe auch  
[Implementieren von Aufträgen](../content/Implement-Jobs.md)  
[Verwalten von Auftragsschritten](../content/Manage-Job-Steps.md)  
  
