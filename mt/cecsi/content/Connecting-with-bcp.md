---
title: "Herstellen einer Verbindung mit bcp"
ms.custom: na
ms.date: 06/09/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3eca5717-e50f-40db-be16-a1cebbdfee70
caps.latest.revision: 33
caps.handback.revision: 32
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
# Herstellen einer Verbindung mit bcp
Das [bcp](http://go.microsoft.com/fwlink/?LinkID=190626)\-Hilfsprogramm ist im [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] ODBC Driver for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] on Linux verfügbar.  
  
Das Feldabschlusszeichen ist ein Tabulator \(„\\t“\).  
  
Das Zeilenabschlusszeichen ist ein Zeilenvorschub \(„\\n“\).  
  
Zeichenmodus ist das bevorzugte Format für bcp\-Formatdateien und \-Datendateien, die keine Sonderzeichen enthalten.  
  
> [!NOTE]  
> Ein umgekehrter Schrägstrich ' \\' für ein Befehlszeilenargument muss entweder mit Anführungszeichen oder mit Escapezeichen versehen sein. Um z. B. einen Zeilenumbruch als benutzerdefiniertes Zeilenabschlusszeichen anzugeben, müssen Sie einen der folgenden Mechanismen verwenden:  
>   
> -   \-r\\\\n  
> -   \-r"\\n"  
> -   \-r'\\n'  
  
Der folgende Code ist ein Beispiel\-Befehlsaufruf von bcp zum Kopieren von Tabellenzeilen in eine Textdatei:  
  
```  
bcp AdventureWorks2008R2.Person.Address out test.dat -Usa -Pxxxx -Sxxx.xxx.xxx.xxx  
```  
  
## Verfügbare bcp\-Optionen  
In der aktuellen Version sind die folgende bcp\-Syntax und die folgenden Optionen verfügbar:  
  
\[*database***.**\]*schema***.***table*  **in**  *data\_file* | **out**  *data\_file*  
  
\-a *packet\_size*  
Gibt an, wie viele Bytes pro Netzwerkpaket an den Server bzw. vom Server gesendet werden.  
  
\-b *batch\_size*  
Gibt die Anzahl von Zeilen pro importierten Datenbatch an.  
  
\-c  
Verwendet einen Zeichendatentyp.  
  
\-d *database\_name*  
Gibt die Datenbank an, mit der eine Verbindung hergestellt werden soll.  
  
\-D  
Bewirkt, dass der Wert, der an die \-S\-Option von sqlcmd übergeben wird, als Datenquellenname \(DSN\) interpretiert wird. Weitere Informationen finden Sie unter „DSN\-Unterstützung in sqlcmd und bcp“ in [Herstellen einer Verbindung mit sqlcmd](../content/Connecting-with-sqlcmd.md).  
  
\-e *eror\_file*  
Gibt den vollständigen Pfad einer Fehlerdatei an, in der alle Zeilen gespeichert werden, die das bcp\-Hilfsprogramm nicht von der Datei in die Datenbank übertragen kann.  
  
\-E  
Verwendet für die Identitätsspalte in der importierten Datendatei einen Identitätswert oder \-werte.  
  
\-f *format\_file*  
Gibt den vollständigen Pfad einer Formatdatei an.  
  
\-F *first\_row*  
Gibt die Nummer der ersten Zeile an, die aus einer Tabelle exportiert oder von einer Datendatei importiert werden soll.  
  
\-k  
Gibt an, dass während des Vorgangs keine Standardwerte in leere Spalten eingefügt werden, sondern ein NULL\-Wert für diese Spalten beibehalten werden soll.  
  
\-l  
Gibt einen Anmeldungstimeout an. Die Option \-I gibt an, wie viele Sekunden beim Herstellen einer Verbindung mit einem Server verstreichen dürfen, bevor für eine bcp\-Anmeldung bei [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] ein Timeout eintritt. Das Standardtimeout für bcp für die Anmeldung bei [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] beträgt 15 Sekunden. Der Timeoutwert für den Anmeldungszeitraum muss eine Zahl zwischen 0 und 65534 sein. Wenn der angegebene Wert kein numerischer Wert ist oder außerhalb dieses Bereichs liegt, generiert bcp eine Fehlermeldung. Mit dem Wert 0 wird eine unbegrenzte Wartezeit festgelegt.  
  
\-L *last\_row*  
Gibt die Nummer der letzten Zeile an, die aus einer Tabelle exportiert oder von einer Datendatei importiert werden soll.  
  
\-m *max\_errors*  
Gibt an, wie viele Syntaxfehler maximal auftreten können, bevor der bcp\-Vorgang abgebrochen wird.  
  
\-n  
Verwendet die systemeigenen \(Datenbank\-\) Datentypen, um den Massenkopiervorgang auszuführen.  
  
\-P *password*  
Gibt das Kennwort für die Anmelde\-ID an.  
  
\-q  
Führt die SET QUOTED\_IDENTIFIERS ON\-Anweisung in der Verbindung zwischen dem bcp\-Hilfsprogramm und einer [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz aus.  
  
\-r *row\_terminator*  
Gibt das Zeilenabschlusszeichen an.  
  
\-R  
Gibt an, dass beim Massenkopieren von Währungs\-, Datums\- und Zeitdaten in [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] das Länderformat verwendet wird, das durch die Gebietsschemaeinstellung des Clientcomputers definiert wird.  
  
\-S *server*  
Gibt den Namen der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Instanz an, mit der eine Verbindung hergestellt werden soll. Oder, wenn \-D verwendet wird, einen DSN.  
  
\-t *field\_terminator*  
Gibt das Feldabschlusszeichen an.  
  
\-T  
Gibt an, dass das bcp\-Hilfsprogramm die Verbindung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] mithilfe einer vertrauenswürdigen Verbindung \(integrierte Sicherheit\) herstellt.  
  
\-U *login\_id*  
Gibt die Anmelde\-ID an, die zum Herstellen einer Verbindung mit [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] verwendet wird.  
  
\-v  
Meldet die Versionsnummer des bcp\-Hilfsprogramms und das Copyright.  
  
\-w  
Verwendet Unicode\-Zeichen, um den Massenkopiervorgang auszuführen.  
  
In dieser Version werden Latin\-1\- und UTF\-16\-Zeichen unterstützt.  
  
## Nicht verfügbare bcp\-Optionen  
In der aktuellen Version sind die folgende bcp\-Syntax und die folgenden Optionen nicht verfügbar:  
  
\-C  
Gibt die Codepage für die in der Datendatei enthaltenen Daten an.  
  
\-h *hint*  
Gibt den oder die Hinweise an, die beim Massenimportieren von Daten in eine Tabelle oder Sicht verwendet werden.  
  
\-i *input\_file*  
Gibt den Namen einer Antwortdatei an.  
  
\-N  
Verwendet die systemeigenen \(Datenbank\-\) Datentypen für Daten, die keinen Zeichendatentyp haben, sowie Unicode\-Zeichen für Zeichendaten.  
  
\-o *output\_file*  
Gibt den Namen einer Datei an, in die die Ausgabe geschrieben wird, die von der Eingabeaufforderung umgeleitet wurde.  
  
\-V \(80 | 90 | 100\)  
Verwendet Datentypen aus einer früheren Version von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)].  
  
\-x  
Bei Verwendung mit den Optionen Format und \-f format\_file wird anstelle der standardmäßigen Nicht\-XML\-Formatdatei eine XML\-basierte Formatdatei generiert.  
  
## Siehe auch  
[Microsoft ODBC Driver for SQL Server on Linux](../content/Microsoft-ODBC-Driver-for-SQL-Server-on-Linux.md)  
  
