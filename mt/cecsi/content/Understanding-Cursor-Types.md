---
title: "Grundlegendes zu Cursortypen"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4f4d3db7-4f76-450d-ab63-141237a4f034
caps.latest.revision: 51
caps.handback.revision: 47
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
# Grundlegendes zu Cursortypen
  Vorgänge in einer relationalen Datenbank beziehen sich immer auf eine vollständige Gruppe von Zeilen. Die von einer SELECT\-Anweisung zurückgegebene Gruppe von Zeilen besteht aus allen Zeilen, die die Bedingungen der WHERE\-Klausel der Anweisung erfüllen. Diese vollständige Gruppe von Zeilen, die von der Anweisung zurückgegeben wird, wird als Resultset bezeichnet. Anwendungen sind nicht immer effektiv, wenn das gesamte Resultset als eine Einheit bearbeitet wird. Diese Anwendungen benötigen einen Mechanismus, um jeweils eine Zeile oder einen kleinen Zeilenblock zu bearbeiten. Cursor sind eine Erweiterung zu Resultsets und stellen diesen Mechanismus bereit.  
  
 Cursor erweitern die Verarbeitung von Resultsets durch folgende Aktionen:  
  
-   Ermöglichen der Positionierung an bestimmten Zeilen des Resultsets.  
  
-   Abrufen einer Zeile oder eines ZeilenBlocks von der aktuellen Position im Resultset.  
  
-   Unterstützen von Datenänderungen in der Zeile an der aktuellen Position im Resultset.  
  
-   Unterstützen von unterschiedlichen Sichtbarkeitsebenen bei Änderungen, die von anderen Benutzern an den Datenbankdaten, die im Resultset dargestellt werden, ausgeführt wurden.  
  
> [!NOTE]  
>  Eine umfassende Beschreibung der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Cursortypen finden Sie im Thema zu Cursortypen \(Datenbankmodul\) in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation.  
  
 Die JDBC\-Spezifikation stellt Unterstützung für Vorwärtscursor und scrollfähige Cursor bereit, die Änderungen durch andere Aufträge berücksichtigen oder nicht berücksichtigen können und schreibgeschützt oder aktualisierbar sein können. Diese Funktionalität wird von der [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Klasse von [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] bereitgestellt.  
  
## Hinweise  
 Der JDBC\-Treiber unterstützt die folgenden Cursortypen:  
  
|Resultset<br /><br /> \(Cursor\) Typ|SQL Server\-Cursortyp|Merkmale|select<br /><br /> Methode|Antwort<br /><br /> Pufferung|Beschreibung|  
|----------------------------------|---------------------------|--------------|------------------------|---------------------------|------------------|  
|TYPE\_FORWARD\_ONLY \(CONCUR\_READ\_ONLY\)|N\/V|Vorwärtscursor, schreibgeschützt|Direkt|Volle|Die Anwendung muss ein Pass\-Through \(vorwärts\) für das Resultset ausführen. Dies ist das Standardverhalten und entspricht einem TYPE\_SS\_DIRECT\_FORWARD\_ONLY\-Cursor. Der Treiber liest das gesamte Resultset während der Ausführung der Anweisung aus dem Server in einen Speicher.|  
|TYPE\_FORWARD\_ONLY \(CONCUR\_READ\_ONLY\)|N\/V|Vorwärtscursor, schreibgeschützt|Direkt|adaptive|Die Anwendung muss ein Pass\-Through \(vorwärts\) für das Resultset ausführen. Das Verhalten entspricht dem Verhalten eines TYPE\_SS\_DIRECT\_FORWARD\_ONLY\-Cursors. Der Treiber liest Zeilen vom Server, wenn die Anwendung sie anfordert, und minimiert so die Speicherauslastung auf Clientseite.|  
|TYPE\_FORWARD\_ONLY \(CONCUR\_READ\_ONLY\)|Schneller Vorwärtscursor|Vorwärtscursor, schreibgeschützt|cursor|N\/V|Die Anwendung muss mithilfe eines Servercursors ein Pass\-Through \(vorwärts\) für das Resultset ausführen. Das Verhalten entspricht dem Verhalten eines TYPE\_SS\_SERVER\_CURSOR\_FORWARD\_ONLY\-Cursors.<br /><br /> Zeilen werden in durch die Abrufgröße angegebene Blöcke vom Server abgerufen.|  
|TYPE\_FORWARD\_ONLY \(CONCUR\_UPDATABLE\)|Dynamisch \(Vorwärtscursor\)|Vorwärtscursor, aktualisierbar|N\/V|N\/V|Die Anwendung muss ein Pass\-Through \(vorwärts\) für das Resultset ausführen, um eine oder mehrere Zeilen zu aktualisieren.<br /><br /> Zeilen werden in durch die Abrufgröße angegebene Blöcke vom Server abgerufen.<br /><br /> In der Standardeinstellung ist die Abrufgröße festgelegt, wenn die Anwendung die [setFetchSize](../content/setFetchSize-Method--SQLServerResultSet-.md)\-Methode des [SQLServerResultSet](../content/SQLServerResultSet-Class.md)\-Objekts aufruft. **Note:**  Der JDBC\-Treiber bietet eine Funktion für adaptive Pufferung, die es erlaubt, Ergebnisse der Anweisungsausführung erst dann von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] abzurufen, wenn sie in der Anwendung benötigt werden, statt alle Ergebnisse auf einmal abrufen zu müssen. Wenn die Anwendung beispielsweise eine große Datenmenge abrufen muss, für die der Anwendungsspeicher nicht ausreicht, kann die Clientanwendung den Wert mithilfe der adaptiven Pufferung als Datenstrom abrufen. Das Standardverhalten des Treibers ist "**adaptive**". Um jedoch die adaptive Pufferung für das aktualisierbare Resultset mit Vorwärtscursor zu aktivieren, muss die Anwendung die [setResponseBuffering](../content/setResponseBuffering-Method--SQLServerStatement-.md)\-Methode des [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekts explizit aufrufen, indem der **String**\-Wert "**adaptive"**" angegeben wird. Beispielcode finden Sie unter [Beispiel zum Aktualisieren umfangreicher Daten](../content/Updating-Large-Data-Sample.md).|  
|TYPE\_SCROLL\_INSENSITIVE|STATIC\-Cursor|Scrollfähig, nicht aktualisierbar<br /><br /> Externe Zeilenupdates, \-einfügungen und \-löschvorgänge sind nicht sichtbar.|N\/V|N\/V|Die Anwendung erfordert eine Datenbankmomentaufnahme. Das Resultset kann nicht aktualisiert werden. Nur CONCUR\_READ\_ONLY wird unterstützt.  Alle anderen Parallelitätstypen führen bei Verwendung mit diesem Cursortyp zu einer Ausnahme.<br /><br /> Zeilen werden in durch die Abrufgröße angegebene Blöcke vom Server abgerufen.|  
|TYPE\_SCROLL\_SENSITIVE<br /><br /> \(CONCUR\_READ\_ONLY\)|Keyset|Scrollfähig, schreibgeschützt Externe Zeilenupdates sind sichtbar, und Löschvorgänge werden als fehlende Daten angezeigt.<br /><br /> Externe Zeileneinfügungen sind nicht sichtbar.|N\/V|N\/V|Die Anwendung muss geänderte Daten nur für vorhandene Zeilen anzeigen.<br /><br /> Zeilen werden in durch die Abrufgröße angegebene Blöcke vom Server abgerufen.|  
|TYPE\_SCROLL\_SENSITIVE<br /><br /> \(CONCUR\_UPDATABLE, CONCUR\_SS\_SCROLL\_LOCKS, CONCUR\_SS\_OPTIMISTIC\_CC, CONCUR\_SS\_OPTIMISTIC\_CCVAL\)|Keyset|Scrollfähig, aktualisierbar<br /><br /> Externe und interne Zeilenupdates sind sichtbar, Löschvorgänge werden als fehlende Daten angezeigt, und Einfügungen sind nicht sichtbar.|N\/V|N\/V|Die Anwendung kann Daten in vorhandenen Zeilen mit dem ResultSet\-Objekt ändern. Auch Änderungen an Zeilen, die von anderen außerhalb des ResultSet\-Objekts vorgenommen werden, müssen für die Anwendung sichtbar sein.<br /><br /> Zeilen werden in durch die Abrufgröße angegebene Blöcke vom Server abgerufen.|  
|TYPE\_SS\_DIRECT\_FORWARD\_ONLY|N\/V|Vorwärtscursor, schreibgeschützt|N\/V|"full" oder "adaptive"|Ganzzahliger Wert \= 2003. Stellt einen schreibgeschützten clientseitigen Cursor bereit, der vollständig gepuffert wird. Es wird kein Servercursor erstellt.<br /><br /> Nur der Parallelitätstyp CONCUR\_READ\_ONLY wird unterstützt. Alle anderen Parallelitätstypen führen bei Verwendung mit diesem Cursortyp zu einer Ausnahme.|  
|TYPE\_SS\_SERVER\_CURSOR\_FORWARD\_ONLY|Schneller Vorwärtscursor|Vorwärtscursor|N\/V|N\/V|Ganzzahliger Wert \= 2004. Schnell, greift über einen Servercursor auf alle Daten zu. Bei Verwendung mit dem Parallelitätstyp CONCUR\_UPDATABLE aktualisierbar.<br /><br /> Zeilen werden in durch die Abrufgröße angegebene Blöcke vom Server abgerufen.<br /><br /> Zum Abrufen der adaptiven Pufferung in diesem Fall muss die Anwendung die [setResponseBuffering](../content/setResponseBuffering-Method--SQLServerStatement-.md)\-Methode des [SQLServerStatement](../content/SQLServerStatement-Class.md)\-Objekts explizit aufrufen, indem der **String**\-Wert "**adaptive"**" angegeben wird. Beispielcode finden Sie unter [Beispiel zum Aktualisieren umfangreicher Daten](../content/Updating-Large-Data-Sample.md).|  
|TYPE\_SS\_SCROLL\_STATIC|STATIC\-Cursor|Die Updates von anderen Benutzern werden nicht reflektiert.|N\/V|N\/V|Ganzzahliger Wert \= 1004. Die Anwendung erfordert einen Datenbanksnapshot. Dies ist das [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-spezifische Synonym für JDBC TYPE\_SCROLL\_INSENSITIVE und weist das gleiche Verhalten für die Festlegung der Parallelität auf.<br /><br /> Zeilen werden in durch die Abrufgröße angegebene Blöcke vom Server abgerufen.|  
|TYPE\_SS\_SCROLL\_KEYSET<br /><br /> \(CONCUR\_READ\_ONLY\)|Keyset|Scrollfähig, schreibgeschützt Externe Zeilenupdates sind sichtbar, und Löschvorgänge werden als fehlende Daten angezeigt.<br /><br /> Externe Zeileneinfügungen sind nicht sichtbar.|N\/V|N\/V|Ganzzahliger Wert \= 1005. Die Anwendung muss geänderte Daten nur für vorhandene Zeilen anzeigen. Dies ist das [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-spezifische Synonym für JDBC TYPE\_SCROLL\_SENSITIVE und weist das gleiche Verhalten für die Festlegung der Parallelität auf.<br /><br /> Zeilen werden in durch die Abrufgröße angegebene Blöcke vom Server abgerufen.|  
|TYPE\_SS\_SCROLL\_KEYSET<br /><br /> \(CONCUR\_UPDATABLE, CONCUR\_SS\_SCROLL\_LOCKS, CONCUR\_SS\_OPTIMISTIC\_CC, CONCUR\_SS\_OPTIMISTIC\_CCVAL\)|Keyset|Scrollfähig, aktualisierbar<br /><br /> Externe und interne Zeilenupdates sind sichtbar, Löschvorgänge werden als fehlende Daten angezeigt, und Einfügungen sind nicht sichtbar.|N\/V|N\/V|Ganzzahliger Wert \= 1005. Die Anwendung muss Daten ändern oder geänderte Daten für vorhandene Zeilen anzeigen. Dies ist das [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-spezifische Synonym für JDBC TYPE\_SCROLL\_SENSITIVE und weist das gleiche Verhalten für die Festlegung der Parallelität auf.<br /><br /> Zeilen werden in durch die Abrufgröße angegebene Blöcke vom Server abgerufen.|  
|TYPE\_SS\_SCROLL\_DYNAMIC<br /><br /> \(CONCUR\_READ\_ONLY\)|Dynamisch|Scrollfähig, schreibgeschützt<br /><br /> Externe Zeilenupdates und \-einfügungen werden angezeigt. Löschvorgänge werden als temporäre fehlende Daten im aktuellen Fetchpuffer angezeigt.|N\/V|N\/V|Ganzzahliger Wert \= 1006. Die Anwendung muss geänderte Daten für vorhandene Zeilen anzeigen und eingefügte und gelöschte Zeilen während der Lebensdauer des Cursors anzeigen.<br /><br /> Zeilen werden in durch die Abrufgröße angegebene Blöcke vom Server abgerufen.|  
|TYPE\_SS\_SCROLL\_DYNAMIC<br /><br /> \(CONCUR\_UPDATABLE, CONCUR\_SS\_SCROLL\_LOCKS, CONCUR\_SS\_OPTIMISTIC\_CC, CONCUR\_SS\_OPTIMISTIC\_CCVAL\)|Dynamisch|Scrollfähig, aktualisierbar<br /><br /> Externe und interne Zeilenupdates und \-einfügungen werden angezeigt. Löschvorgänge werden als temporäre fehlende Daten im aktuellen Fetchpuffer angezeigt.|N\/V|N\/V|Ganzzahliger Wert \= 1006. Die Anwendung kann Daten für vorhandene Zeilen ändern oder mit dem ResultSet\-Objekt einfügen oder löschen. Auch Änderungen, Einfügungen und Löschvorgänge für Zeilen, die von anderen außerhalb des ResultSet\-Objekts vorgenommen werden, müssen für die Anwendung sichtbar sein.<br /><br /> Zeilen werden in durch die Abrufgröße angegebene Blöcke vom Server abgerufen.|  
  
## Cursorpositionierung  
 Die Cursor TYPE\_FORWARD\_ONLY, TYPE\_SS\_DIRECT\_FORWARD\_ONLY und TYPE\_SS\_SERVER\_CURSOR\_FORWARD\_ONLY unterstützen nur die [next](../content/next-Method--SQLServerResultSet-.md)\-Positionierungsmethode.  
  
 Der TYPE\_SS\_SCROLL\_DYNAMIC\-Cursor unterstützt nicht die [absolute](../content/absolute-Method--SQLServerResultSet-.md)\-Methode und die [getRow](../content/getRow-Method--SQLServerResultSet-.md)\-Methode. Die absolute\-Methode kann durch eine Kombination von Aufrufen der [first](../content/first-Method--SQLServerResultSet-.md)\-Methode und der [relative](../content/relative-Method--SQLServerResultSet-.md)\-Methode für dynamische Cursor angeglichen werden.  
  
 Die getRow\-Methode wird nur von den Cursorn TYPE\_FORWARD\_ONLY, TYPE\_SS\_DIRECT\_FORWARD\_ONLY, TYPE\_SS\_SERVER\_CURSOR\_FORWARD\_ONLY, TYPE\_SS\_SCROLL\_KEYSET und TYPE\_SS\_SCROLL\_STATIC unterstützt. Die getRow\-Methode gibt mit allen Vorwärtscursortypen die Anzahl der bisher über den Cursor gelesenen Zeilen zurück.  
  
> [!NOTE]  
>  Wenn eine Anwendung einen nicht unterstützten Cursorpositionierungsaufruf oder einen nicht unterstützten Aufruf der getRow\-Methode ausführt, wird eine Ausnahme mit der folgenden Meldung ausgelöst: "Der angeforderte Vorgang wird für diesen Cursortyp nicht unterstützt."  
  
 Nur der TYPE\_SS\_SCROLL\_KEYSET\-Cursor und der entsprechende TYPE\_SCROLL\_SENSITIVE\-Cursor machen gelöschte Zeilen verfügbar. Wenn der Cursor in einer gelöschten Zeile positioniert wird, sind die Spaltenwerte nicht verfügbar, und die [rowDeleted](../content/rowDeleted-Method--SQLServerResultSet-.md)\-Methode gibt "true" zurück. Aufrufe der get\<Type\>\-Methoden lösen eine Ausnahme mit der folgenden Meldung aus: "Wert aus gelöschter Zeile kann nicht abgerufen werden." Gelöschte Zeilen können nicht aktualisiert werden. Wenn Sie versuchen, eine update\<Type\>\-Methode für eine gelöschte Zeile aufzurufen, wird eine Ausnahme mit der folgenden Meldung ausgelöst: "Eine gelöschte Zeile kann nicht aktualisiert werden." Der TYPE\_SS\_SCROLL\_DYNAMIC\-Cursor weist dasselbe Verhalten auf, bis der Cursor aus dem aktuellen Fetchpuffer verschoben wird.  
  
 Vorwärtscursor und dynamische Cursor machen gelöschte Zeilen auf ähnliche Weise verfügbar, jedoch nur, wenn auf die Cursor weiterhin im Fetchpuffer zugegriffen werden kann. Für Vorwärtscursor ist dies relativ einfach. Bei dynamischen Cursorn ist dies komplexer, wenn die Fetchgröße größer als 1 ist. Eine Anwendung kann den Cursor in dem vom Fetchpuffer definierten Fenster vorwärts und rückwärts verschieben, die gelöschte Zeile wird jedoch nicht mehr angezeigt, wenn der ursprüngliche Fetchpuffer, in dem sie aktualisiert wurde, verlassen wird. Wenn eine Anwendung keine temporären gelöschten Zeilen mithilfe von dynamischen Cursorn anzeigen soll, sollte eine Fetchrelative \(0\) verwendet werden.  
  
 Wenn die Schlüsselwerte einer TYPE\_SS\_SCROLL\_KEYSET\-Cursorzeile oder einer TYPE\_SCROLL\_SENSITIVE\-Cursorzeile mit dem Cursor aktualisiert werden, behält die Zeile die ursprüngliche Position im Resultset bei, unabhängig davon, ob die aktualisierte Zeile die Auswahlkriterien des Cursors erfüllt. Wenn die Zeile außerhalb des Cursors aktualisiert wurde, wird eine gelöschte Zeile an der ursprünglichen Position der Zeile angezeigt, die Zeile wird jedoch nur im Cursor angezeigt, wenn eine andere Zeile mit den neuen Schlüsselwerten im Cursor vorhanden war, aber anschließend gelöscht wurde.  
  
 Bei dynamischen Cursorn behalten aktualisierte Zeilen ihre Position im Fetchpuffer bei, bis das vom Fetchpuffer definierte Fenster verlassen wird. Aktualisierte Zeilen werden möglicherweise anschließend an anderen Positionen im Resultset erneut angezeigt oder überhaupt nicht mehr angezeigt. In Anwendungen, in denen temporäre Inkonsistenzen im Resultset vermieden werden sollen, sollte eine Fetchgröße von 1 verwendet werden. \(Der Standardwert beträgt 8 Zeilen bei CONCUR\_SS\_SCROLL\_LOCKS\-Parallelität und 128 Zeilen bei anderen Parallelitäten.\)  
  
## Cursorkonvertierung  
 In [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] wird in einigen Fällen ein anderer Cursortyp als der angeforderte implementiert. Dies wird als implizite Cursorkonvertierung \(oder Cursordegradierung\) bezeichnet. Weitere Informationen zur impliziten Cursorkonvertierung finden Sie im Thema "Verwenden impliziter Cursorkonvertierungen" in der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]\-Onlinedokumentation.  
  
 Wenn Sie in [!INCLUDE[ssVersion2000](../content/includes/ssVersion2000_md.md)] die Daten über das ResultSet.TYPE\_SCROLL\_SENSITIVE\-Resultset und das ResultSet.CONCUR\_UPDATABLE\-Resultset aktualisieren, wird eine Ausnahme mit der folgenden Meldung ausgelöst: "Der Cursor ist schreibgeschützt \(READ ONLY\)." Diese Ausnahme tritt auf, weil [!INCLUDE[ssVersion2000](../content/includes/ssVersion2000_md.md)] eine implizite Cursorkonvertierung für das Resultset ausgeführt und nicht den angeforderten aktualisierbaren Cursor zurückgegeben hat.  
  
 Um dieses Problem zu umgehen, können Sie eine der folgenden Lösungen auswählen:  
  
-   Stellen Sie sicher, dass die zugrunde liegende Tabelle einen Primärschlüssel aufweist.  
  
-   Verwenden Sie beim Erstellen einer Anweisung [SQLServerResultSet.TYPE\_SS\_SCROLL\_DYNAMIC](../content/TYPE_SS_SCROLL_DYNAMIC-Field--SQLServerResultSet-.md) anstelle von ResultSet.TYPE\_SCROLL\_SENSITIVE.  
  
## Cursoraktualisierung  
 Ersetzungsupdates werden bei Cursorn unterstützt, bei denen Cursortyp und Parallelität Updates unterstützen. Wenn der Cursor nicht in einer aktualisierbaren Zeile im Resultset positioniert ist \(es war kein get\<Type\>\-Methodenaufruf erfolgreich\), löst ein Aufruf einer update\<Type\>\-Methode eine Ausnahme mit der folgenden Meldung aus: "Das Resultset verfügt über keine aktuelle Zeile." Die JDBC\-Spezifikation gibt an, dass eine Ausnahme ausgelöst wird, wenn eine Updatemethode für eine Spalte eines CONCUR\_READ\_ONLY\-Cursors aufgerufen wird. Wenn die Zeile nicht aktualisiert werden kann, beispielsweise aufgrund eines Konflikts der vollständigen Parallelität durch einen konkurrierenden Aktualisierungs\- oder Löschvorgang, wird die Ausnahme möglicherweise erst ausgelöst, wenn [insertRow](../content/insertRow-Method--SQLServerResultSet-.md), [updateRow](../content/updateRow-Method--SQLServerResultSet-.md) oder [deleteRow](../content/deleteRow-Method--SQLServerResultSet-.md) aufgerufen wird  
  
 Nach einem Aufruf von update\<Type\> kann auf die betreffende Spalte erst durch get\<Type\> zugegriffen werden, wenn updateRow oder [cancelRowUpdates](../content/cancelRowUpdates-Method--SQLServerResultSet-.md) aufgerufen wurde. So werden Probleme vermieden, wenn eine Spalte durch einen anderen Typ als den vom Server zurückgegebenen Typ aktualisiert wird und folgende Abrufaufrufe clientseitige Typkonvertierungen aufrufen könnten, die ungenaue Ergebnisse liefern. Aufrufe von get\<Type\> lösen eine Ausnahme mit der folgenden Meldung aus: "Der Zugriff auf aktualisierte Spalten kann erst nach dem Aufrufen von updateRow\(\) oder cancelRowUpdates\(\) erfolgen."  
  
> [!NOTE]  
>  Wenn die updateRow\-Methode aufgerufen wird und keine Spalten aktualisiert wurden, löst der JDBC\-Treiber eine Ausnahme mit der folgenden Meldung aus: "updateRow\(\) aufgerufen, wenn keine Spalten aktualisiert wurden."  
  
 Nach dem Aufrufen von [moveToInsertRow](../content/moveToInsertRow-Method--SQLServerResultSet-.md) wird eine Ausnahme ausgelöst, wenn eine andere Methode als get\<Type\>, update\<Type\>, insertRow, und Cursorpositionierungsmethoden \(einschließlich [moveToCurrentRow](../content/moveToCurrentRow-Method--SQLServerResultSet-.md)\) für das Resultset aufgerufen wird. Die moveToInsertRow\-Methode versetzt das Resultset effektiv in den Einfügemodus, und Cursorpositionierungsmethoden beenden den Einfügemodus. Relative Cursorpositionierungsaufrufe verschieben den Cursor relativ zur Position, in der er sich vor dem Aufruf von moveToInsertRow befunden hat. Nach Cursorpositionierungsaufrufen wird die Zielcursorposition die neue Cursorposition.  
  
 Wenn der Cursorpositionierungsaufruf im Einfügemodus nicht erfolgreich ist, ist die Cursorposition nach dem Aufruf mit Fehler die ursprüngliche Cursorposition vor dem Aufruf von moveToInsetRow. Wenn bei insertRow ein Fehler auftritt, bleibt der Cursor in der Einfügezeile, und der Cursor bleibt im Einfügemodus.  
  
 Spalten in der Einfügezeile befinden sich anfänglich in einem nicht initialisierten Status. Durch Aufrufe der update\<Type\>\-Methode wird der Spaltenstatus auf initialisiert festgelegt. Ein Aufruf der get\<Type\>\-Methode für eine nicht initialisierte Spalte löst eine Ausnahme aus. Ein Aufruf der insertRow\-Methode gibt alle Spalten in der Einfügezeile in einem nicht initialisierten Status zurück.  
  
 Wenn Spalten beim Aufrufen der insertRow\-Methode nicht initialisiert sind, wird der Standardwert für die Spalte eingefügt. Wenn kein Standardwert vorhanden ist, die Spalte jedoch auf NULL festgelegt werden kann, wird NULL eingefügt. Wenn kein Standardwert vorhanden ist und die Spalte nicht auf NULL festgelegt werden kann, gibt der Server einen Fehler zurück, und es wird eine Ausnahme ausgelöst.  
  
> [!NOTE]  
>  Aufrufe der getRow\-Methode geben im Einfügemodus 0 zurück.  
>   
>  Der JDBC\-Treiber unterstützt keine positionierten Updates oder Löschvorgänge. Entsprechend der JDBC\-Spezifikation hat die [setCursorName](../content/setCursorName-Method--SQLServerStatement-.md)\-Methode keine Auswirkungen, und die [getCursorName](../content/getCursorName-Method--SQLServerResultSet-.md)\-Methode löst eine Ausnahme aus, wenn sie aufgerufen wird.  
>   
>  Schreibgeschützte und statische Cursor können nie aktualisiert werden.  
>   
>  SQL Server schränkt Servercursor auf ein einziges Resultset ein. Wenn ein Batch oder eine gespeicherte Prozedur mehrere Anweisungen enthält, muss ein schreibgeschützter Vorwärtsclientcursor verwendet werden.  
  
## Siehe auch  
 [Verwalten von Resultsets mit dem JDBC-Treiber](../content/Managing-Result-Sets-with-the-JDBC-Driver.md)  
  
  