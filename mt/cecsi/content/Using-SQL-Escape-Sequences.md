---
title: "Verwenden von SQL-Escapesequenzen"
ms.custom: na
ms.date: 07/01/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 00f9e25a-088e-4ac6-aa75-43eacace8f03
caps.latest.revision: 25
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
  - sv-se
  - zh-cn
  - zh-tw
---
# Verwenden von SQL-Escapesequenzen
  [!INCLUDE[jdbcNoVersion](../content/includes/jdbcNoVersion_md.md)] unterstützt die Verwendung von SQL\-Escapesequenzen, wie von der JDBC\-API definiert. Mithilfe von Escapesequenzen wird in einer SQL\-Anweisung für den Treiber angegeben, dass der Teil der SQL\-Zeichenfolge mit Escapezeichen anders behandelt werden soll. Wenn der JDBC\-Treiber den Teil einer SQL\-Anweisung mit Escapezeichen verarbeitet, wird dieser Teil der Zeichenfolge in SQL\-Code übersetzt, den SQL Server verwenden kann.  
  
 Es gibt fünf Arten von Escapesequenzen, die für die JDBC\-API erforderlich sind. Alle werden vom JDBC\-Treiber unterstützt:  
  
-   LIKE\-Platzhalterliterale  
  
-   Funktionsbehandlung  
  
-   Datums\- und Zeitliterale  
  
-   Aufrufe gespeicherter Prozeduren  
  
-   Äußere Joins  
  
-   LIMIT\-Escapesyntax  
  
 JDBC\-Treiber verwendet die folgende Escapesequenzsyntax:  
  
 `{keyword ...parameters...}`  
  
> [!NOTE]  
>  Die SQL\-Escapeverarbeitung ist für den JDBC\-Treiber immer aktiviert.  
  
 In den folgenden Abschnitten werden die fünf Arten von Escapesequenzen und ihre Unterstützung durch den JDBC\-Treiber beschrieben.  
  
## LIKE\-Platzhalterliterale  
 Der JDBC\-Treiber unterstützt die `{escape 'escape character'}`\-Syntax zum Verwenden von LIKE\-Klauselplatzhaltern als Literale. Der folgende Code gibt beispielsweise Werte für „col3“ zurück, wenn der Wert von „col2“ wirklich mit einem Unterstrich beginnt \(und nicht mit dem Platzhalter\).  
  
```  
ResultSet rst = stmt.executeQuery("SELECT col3 FROM test1 WHERE col2   
LIKE '\\_%' {escape '\\'}");  
```  
  
> [!NOTE]  
>  Die Escapesequenz muss sich am Ende der SQL\-Anweisung befinden. Bei mehreren SQL\-Anweisungen in einer Befehlszeichenfolge muss sich die Escapesequenz am Ende jeder relevanten SQL\-Anweisung befinden.  
  
## Funktionsbehandlung  
 Der JDBC\-Treiber unterstützt Funktionsescapesequenzen in SQL\-Anweisungen mit der folgenden Syntax:  
  
```  
{fn functionName}  
```  
  
 Dabei ist `functionName` eine vom JDBC\-Treiber unterstützte Funktion. Beispiel:  
  
```  
SELECT {fn UCASE(Name)} FROM Employee  
```  
  
 In der folgenden Tabelle werden die unterschiedlichen Funktionen aufgeführt, die der JDBC\-Treiber bei der Verwendung einer Funktionsescapesequenz unterstützt.  
  
|Zeichenfolgenfunktionen|Numerische Funktionen|datetime\-Funktionen|Systemfunktionen|  
|-----------------------------|---------------------------|--------------------------|----------------------|  
|ASCII<br /><br /> CHAR<br /><br /> CONCAT<br /><br /> DIFFERENCE<br /><br /> INSERT<br /><br /> LCASE<br /><br /> LEFT<br /><br /> LENGTH<br /><br /> LOCATE<br /><br /> LTRIM<br /><br /> REPEAT<br /><br /> REPLACE<br /><br /> RIGHT<br /><br /> RTRIM<br /><br /> SOUNDEX<br /><br /> LEERTASTE<br /><br /> SUBSTRING<br /><br /> UCASE|ABS<br /><br /> ACOS<br /><br /> ASIN<br /><br /> ATAN<br /><br /> ATAN2<br /><br /> CEILING<br /><br /> COS<br /><br /> COT<br /><br /> DEGREES<br /><br /> EXP<br /><br /> FLOOR<br /><br /> LOG<br /><br /> LOG10<br /><br /> MOD<br /><br /> PI<br /><br /> POWER<br /><br /> RADIANS<br /><br /> RAND<br /><br /> ROUND<br /><br /> SIGN<br /><br /> SIN<br /><br /> SQRT<br /><br /> TAN<br /><br /> TRUNCATE|CURDATE<br /><br /> CURTIME<br /><br /> DAYNAME<br /><br /> DAYOFMONTH<br /><br /> TAGDERWOCHE<br /><br /> TAGDESJAHRES<br /><br /> EXTRACT<br /><br /> HOUR<br /><br /> MINUTE<br /><br /> MONTH<br /><br /> MONTHNAME<br /><br /> JETZT<br /><br /> QUARTAL<br /><br /> SECOND<br /><br /> TIMESTAMPADD<br /><br /> TIMESTAMPDIFF<br /><br /> WOCHE<br /><br /> YEAR|DATABASE<br /><br /> IFNULL<br /><br /> USER|  
  
> [!NOTE]  
>  Wenn Sie versuchen, eine von der Datenbank nicht unterstützte Funktion zu verwenden, tritt ein Fehler auf.  
  
## Datums\- und Zeitliterale  
 Die Escapesyntax für Datums\-, Zeit\- und Timestampliterale lautet wie folgt:  
  
```  
{literal-type 'value'}  
```  
  
 Dabei ist `literal-type` einer der folgenden Typen:  
  
|Literaltyp|Beschreibung|Wertformat|  
|----------------|------------------|----------------|  
|d|Datum|yyyy\-mm\-dd|  
|t|Uhrzeit|hh:mm:ss \[1\]|  
|ts|Zeitstempel|yyyy\-mm\-dd hh:mm:ss\[.f...\]|  
  
 Beispiel:  
  
```  
UPDATE Orders SET OpenDate={d '2005-01-31'}   
WHERE OrderID=1025  
```  
  
## Aufrufe gespeicherter Prozeduren  
 Der JDBC\-Treiber unterstützt die `{? = call proc_name(?,...)}`\-Escapesyntax und die `{call proc_name(?,...)}`\-Escapesyntax für Aufrufe gespeicherter Prozeduren, abhängig davon, ob ein Rückgabeparameter verarbeitet werden muss.  
  
 Bei einer Prozedur handelt es sich um ein in der Datenbank gespeichertes, ausführbares Objekt. In der Regel handelt es sich dabei um eine oder mehrere vorkompilierte SQL\-Anweisungen. Die Escapesequenzsyntax zum Aufrufen einer gespeicherten Prozedur lautet wie folgt:  
  
```  
{[?=]call procedure-name[([parameter][,[parameter]]...)]}  
```  
  
 Dabei gibt `procedure-name` den Namen einer gespeicherten Prozedur an, und `parameter` gibt einen Parameter für eine gespeicherte Prozedur an.  
  
 Weitere Informationen zum Verwenden der `call`\-Escapesequenz mit gespeicherten Prozeduren finden Sie unter [Verwenden von Anweisungen mit gespeicherten Prozeduren](../content/Using-Statements-with-Stored-Procedures.md).  
  
## Äußere Joins  
 Der JDBC\-Treiber unterstützt die linke, rechte und vollständige äußere SQL92\-Joinsyntax. Die Escapesequenz für äußere Joins lautet wie folgt:  
  
```  
{oj outer-join}  
```  
  
 Dabei lautet der äußere Join:  
  
```  
table-reference {LEFT | RIGHT | FULL} OUTER JOIN    
{table-reference | outer-join} ON search-condition  
```  
  
 Dabei ist `table-reference` ein Tabellenname, und `search-condition` ist die Joinbedingung, die für die Tabellen verwendet werden soll.  
  
 Beispiel:  
  
```  
SELECT Customers.CustID, Customers.Name, Orders.OrderID, Orders.Status   
   FROM {oj Customers LEFT OUTER JOIN   
      Orders ON Customers.CustID=Orders.CustID}   
   WHERE Orders.Status='OPEN'  
```  
  
 Die folgenden Escapesequenzen für äußere Joins werden vom JDBC\-Treiber unterstützt:  
  
-   Linke äußere Joins  
  
-   Rechte äußere Joins  
  
-   Vollständige äußere Joins  
  
-   Geschachtelte äußere Joins  
  
## LIMIT\-Escapesyntax  
  
> [!NOTE]  
>  Die LIMIT\-Escapesyntax wird nur bei der Verwendung von JDBC 4.1 oder höher von Microsoft JDBC Driver 4.2 für SQL Server unterstützt.  
  
 Die Escapesyntax für LIMIT ist wie folgt:  
  
```  
LIMIT <rows> [OFFSET <row offset>]  
```  
  
 Die Escapesyntax besteht aus zwei Teilen: \<*rows*\> ist obligatorisch und gibt die Anzahl der zurückzugebenden Zeilen an. OFFSET und \<*row offset*\> sind optional und geben die Anzahl der zu überspringenden Zeilen an, bevor mit der Rückgabe von Zeilen begonnen wird. Der JDBC\-Treiber unterstützt nur den obligatorischen Teil, indem er die Abfrageklausel von LIMIT in TOP umwandelt. SQL Server unterstützt die LIMIT\-Klausel nicht.**Der JDBC\-Treiber unterstützt den optionalen Parameter \<row offset\> nicht, und der Treiber löst eine Ausnahme aus, wenn er verwendet wird**.  
  
## Siehe auch  
 [Verwenden von Anweisungen mit dem JDBC-Treiber](../content/Using-Statements-with-the-JDBC-Driver.md)  
  
  