---
title: "Verwenden von „Immer verschl&#252;sselt“ mit Windows ODBC Driver"
ms.custom: na
ms.date: 06/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1cae4db8-9775-4de2-bf3f-fa44a15e5d0b
caps.latest.revision: 18
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
  - zh-cn
  - zh-tw
---
# Verwenden von „Immer verschl&#252;sselt“ mit Windows ODBC Driver
  „Immer verschlüsselt“ ermöglicht es Clients, sensible Daten in Clientanwendungen zu verschlüsseln und die Verschlüsselungsschlüssel niemals an SQL Server weiterzugeben. Ein auf dem Clientcomputer installierter Treiber, bei dem „Immer verschlüsselt“ aktiviert ist, erreicht dies durch die automatische Ver- und Entschlüsselung von sensiblen Daten in der SQL Server-Clientanwendung. Der Treiber verschlüsselt die Daten in vertraulichen Spalten, bevor er sie an SQL Server weitergibt, und schreibt Abfragen automatisch neu, sodass die Semantik der Anwendung beibehalten wird. Auf ähnliche Weise entschlüsselt der Treiber transparent Daten in verschlüsselten Datenbankspalten, die in Abfrageergebnissen enthalten sind. Weitere Informationen finden Sie unter [Immer verschlüsselt \(\)Datenbankmodul](https://msdn.microsoft.com/en-us/library/mt163865.aspx).  
  
 **Einschränkungen der Vorschauversion**  
  
> [!NOTE]  
>  „Immer verschlüsselt“ wird nur von Microsoft ODBC Driver 13 \(Preview\) for SQL Server mit SQL Server 2016 \(Preview 3.4\+\) unterstützt. Diese Vorschauversion unterstützt Folgendes **nicht** :  
>   
>  -   Massenvorgänge über BCP oder ODBC-Massenfunktionen  
> -   Vorgang mit gespeicherten Prozeduren  
> -   Andere Gebietsschemas als EN\-US  
> -   Die folgenden Datentypen werden getestet. Alle anderen können nicht oder noch nicht mit verschlüsselten Spalten arbeiten  
>   
>      SQL\_C\_CHAR, SQL\_C\_WCHAR, SQL\_C\_STINYINT, SQL\_C\_UTINYINT, SQL\_C\_TINYINT, SQL\_C\_SBIGINT, SQL\_C\_UBIGINT, SQL\_C\_BIGINT, SQL\_C\_SSHORT, SQL\_C\_USHORT, SQL\_C\_SHORT, SQL\_C\_SLONG, SQL\_C\_ULONG, SQL\_C\_LONG, SQL\_C\_FLOAT, SQL\_C\_DOUBLE, SQL\_C\_BINARY, SQL\_C\_TYPE\_DATE, SQL\_C\_TYPE\_TIME  
> -   SqlCmd-Vorgänge  
> -   Azure Key Vault und benutzerdefinierte Schlüsselspeicheranbieter \(Hinweis: Schlüsselspeicheranbieter lokaler Computer **werden** unterstützt.\)  
  
## Entwickeln von Clientanwendungen, um auf immer verschlüsselte Daten zuzugreifen  
 Das Abfragen einer Datenbank mit „Immer verschlüsselt“ von einer Clientanwendung aus erfordert minimalen Entwicklungsaufwand. Im Folgenden werden die  Komponenten und Maßnahmen zusammengefasst, die erforderlich sind, damit Ihre Anwendung immer verschlüsselte Daten lesen und schreiben kann.  
  
### Voraussetzungen  
  
-   Konfigurieren Sie den Server gemäß der Anweisungen im Abschnitt **Erste Schritte mit „Immer verschlüsselt“** des Themas [Immer verschlüsselt \(Datenbankmodul\)](https://msdn.microsoft.com/en-us/library/mt163865.aspx).  
  
-   Installieren Sie Microsoft ODBC Driver 13 \(Preview\) for SQL Server auf dem Clientcomputer.  
  
### Einrichten der Clientanwendung  
 Die Clientanwendung muss so konfiguriert sein, dass sie Zugriff auf einen Schlüsselspeicher hat, der einen Spaltenhauptschlüssel \(Column Master Key, CMK\) enthält. Dieser schützt die Daten, auf die die Anwendung zugreift. Weitere Informationen zu Hauptschlüsseln finden Sie unter [Immer verschlüsselt \(Datenbankmodul\)](https://msdn.microsoft.com/en-us/library/mt163865.aspx). Der ODBC-Treiber unterstützt das Speichern von CMKs in den Schlüsselspeichern der lokalen Computer: lokaler Benutzer und lokaler Computer.  
  
### Verwenden des lokalen Schlüsselspeicheranbieters  
 Der ODBC-Treiber ist mit einer integrierten Schlüsselspeicheranbieter-Implementierung für den Schlüsselspeicher des lokalen Computers und lokalen Benutzers ausgestattet. Clientanwendungen müssen keine besonderen Maßnahmen ergreifen, um diese Schlüsselspeicher zu aktivieren; sie sind im Betriebssystem integriert. Der Ersteller\/Administrator von Zertifikaten \(normalerweise der DBA\) muss den CMK auf alle Clientcomputer verteilen, die mit verschlüsselten Spalten arbeiten sollen.  Weitere Informationen zur Vorgehensweise finden Sie auf der Seite [Immer verschlüsselt \(Datenbankmodul\)](https://msdn.microsoft.com/en-us/library/mt163865.aspx).  
  
### Aktivieren von „Immer verschlüsselt“ für eine Clientverbindung  
 Ändern Sie die Verbindungszeichenfolge in der Clientanwendung, indem Sie den Parameter **ColumnEncryption\=Enabled** zur Verbindungszeichenfolge hinzufügen.  
  
 Im Folgenden finden Sie ein Beispiel für eine Verbindungszeichenfolge für den Microsoft ODBC Driver 13 for SQL Server, der „Immer verschlüsselt“ aktiviert:  
  
```  
SQLWCHAR *connString = L"DRIVER=ODBC Driver 13 for SQL Server;SERVER=.;ColumnEncryption=Enabled";   
```  
  
### Einfügen\/Abrufen von Daten (Beispiel)  
 Fügen Sie mit den Funktionen **SQLPrepare**\/**SQLExecute** oder **SQLExecDirect** in Verbindung mit der **SQLBindParam** -Funktion Daten in verschlüsselte Spalten ein. Die Anwendung übergibt Klartext-SQL mit Parametermarkierungen an die Funktionsargumente und bindet Puffer mit Klartextwerten für alle markierten Parameter. Der Treiber verschlüsselt diese Werte dann transparent und übergibt die verschlüsselten Werte an den Server. Wenn verschlüsselte Spalten über BindCol- oder GetData-Funktionen abgerufen werden, entschlüsselt der Treiber auf ähnliche Weise transparent die Werte, bevor er sie an die Anzahlpuffer der Anwendung sendet. Wenn eine Spalte verschlüsselt wird, sind für SQL Server keine Klartextdaten verfügbar. Er sendet\/empfängt nur verschlüsselte Daten.  
  
 Aus der Perspektive eines Entwicklers gibt es bei Verwendung des ODBC-Treibers mit verschlüsselten Spalten keinen Unterschied in der normalen Ausführung. Unter [ODBC-Beispielcode](https://code.msdn.microsoft.com/windowsapps/ODBC-sample-191624ae/sourcecode?fileId=51137&pathId=1980325953) finden Sie ein Beispiel für die Interaktion mit dem Treiber.  
  
> [!NOTE]  
>  Die Preview-Version von Microsoft ODBC Driver 13 for SQL Server verfügt über eingeschränkten Support für „Immer verschlüsselt“ mit gespeicherten Prozeduren. Es werden noch keine Vorgänge mit gespeicherten Prozeduren bei aktiviertem „Immer verschlüsselt“ unterstützt.  
  
> [!NOTE]  
>  Abfragen können auf Spalten Übereinstimmungsvergleiche ausführen, wenn sie mittels deterministischer Verschlüsselung verschlüsselt sind. Weitere Informationen finden Sie im Abschnitt **Auswählen von deterministischer oder zufälliger Verschlüsselung** des Themas [Immer verschlüsselt \(Datenbankmodul\)](https://msdn.microsoft.com/en-us/library/mt163865.aspx).  
  
### „Immer verschlüsselt“ – API-Referenz  
 Es gibt eine Änderung der ODBC-Treiber-API für die Verwendung in Clientanwendungen, die „Immer verschlüsselt“ verwenden.  
  
> [!NOTE]  
>  Dieses Update ist nur in Microsoft ODBC Driver 13 \(Preview\) for SQL Server verfügbar.  
  
 **ODBC-Verbindungszeichenfolge wie für die SQLDriverConnect-Funktion übergeben**  
  
|Name|Beschreibung|  
|----------|-----------------|  
|Neues Verbindungszeichenfolgen-Schlüsselwort:<br /><br /> ColumnEncryption|ColumnEncryption\=Enabled aktiviert die „Immer verschlüsselt“-Funktionalität für die Verbindung und ColumnEncryption\=Disabled deaktiviert sie. Zulässige Werte sind „Enabled“\/„Disabled“. Der Standardwert ist „Disabled“.|  
  
## Siehe auch  
 [Microsoft ODBC Driver for SQL Server on Windows](../content/Microsoft-ODBC-Driver-for-SQL-Server-on-Windows.md)   
 [„Immer verschlüsselt“ \(Datenbankmodul\)](https://msdn.microsoft.com/en-us/library/mt163865.aspx)  
  
  