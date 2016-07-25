---
title: "Vorgehensweise: Angeben der Parameterrichtung mit dem SQLSRV-Treiber"
ms.custom: na
ms.date: 06/16/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1209eeca-df75-4283-96dc-714f39956b95
caps.latest.revision: 16
caps.handback.revision: 15
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
# Vorgehensweise: Angeben der Parameterrichtung mit dem SQLSRV-Treiber
In diesem Thema wird beschrieben, wie der SQLSRV-Treiber verwendet wird, um die Parameterrichtung anzugeben, wenn Sie eine gespeicherte Prozedur aufrufen. Beachten Sie, dass die Parameterrichtung angegeben wird, wenn Sie ein Parameterarray erstellen \(Schritt 3\), das an [sqlsrv\_query](../content/sqlsrv_query.md) oder [sqlsrv\_prepare](../content/sqlsrv_prepare.md) übergeben wird.  
  
### Gehen Sie wie folgt vor, um die Parameterrichtung anzugeben:  
  
1.  Definieren Sie eine Transact\-SQL-Abfrage, die eine gespeicherte Prozedur aufruft. Verwenden Sie Fragezeichen \(?\) anstelle der Parameter, die an die gespeicherte Prozedur übergeben werden sollen. Diese Zeichenfolge z. B. ruft eine gespeicherte Prozedur auf \(UpdateVacationHours\), die zwei Parameter akzeptiert:  
  
    ```  
    $tsql = "{call UpdateVacationHours(?, ?)}";  
    ```  
  
    > [!NOTE]  
    > Die Verwendung kanonischer Syntax stellt die empfohlene Vorgehensweise für das Abrufen gespeicherter Prozeduren dar. Weitere Informationen zur kanonischen Syntax finden Sie unter [Aufrufen einer gespeicherten Prozedur](http://go.microsoft.com/fwlink/?linkid=119517).  
  
2.  Initialisieren oder aktualisieren Sie PHP-Variablen, die den Platzhaltern in der Transact\-SQL-Abfrage entsprechen.  Zum Beispiel aktualisiert folgender Code die zwei in der Prozedur UpdateVacationHours gespeicherten Parameter.  
  
    ```  
    $employeeId = 101;  
    $usedVacationHours = 8;  
    ```  
  
    > [!NOTE]  
    > Variablen, die auf **NULL**, **DateTime** oder Streamtypen aktualisiert oder initialisiert werden, können nicht als Ausgabeparameter verwendet werden.  
  
3.  Verwenden Sie Ihre PHP-Variablen aus Schritt 2, um ein Array von Parameterwerten zu erstellen oder zu aktualisieren. Dieses soll der Reihenfolge der Parameterplatzhalter in der Transact\-SQL-Zeichenfolge entsprechen. Geben Sie die Richtung  jedes Parameters im Array an. Die Richtung jedes einzelnen Parameters wird durch eine von zwei Möglichkeiten festgelegt: standardmäßig \(für Eingabeparameter\) oder mithilfe von **SQLSRV\_PARAM\_\***-Konstanten \(für Ausgabeparameter und bidirektionale Parameter\). Der folgende Code gibt beispielsweise den *$employeeId* -Parameter als Eingabeparameter und den *$usedVacationHours* -Parameter als bidirektionaler Parameter an:  
  
    ```  
    $params = array(  
                     array($employeeId, SQLSRV_PARAM_IN),  
                     array($usedVacationHours, SQLSRV_PARAM_INOUT)  
                    );  
    ```  
  
    Um die Syntax zum Angeben der Parameterrichtung im Allgemeinen zu verstehen, nehmen Sie an, dass *$var1*, *$var2*, und *$var3* jeweils den Eingabe-, Ausgabe- und bidirektionalen Parametern entsprechen. Sie können die Richtung des Parameters in einer der folgenden Arten angeben:  
  
    -    Geben Sie den Eingabeparameter implizit und den Ausgabeparameter sowie den bidirektionalen Parameter explizit an:  
  
        ```  
        array(   
               array($var1),  
               array($var2, SQLSRV_PARAM_OUT),  
               array($var3, SQLSRV_PARAM_INOUT)  
               );  
        ```  
  
    -    Geben Sie den Eingabeparameter ,den Ausgabeparameter sowie den bidirektionalen Parameter explizit an.  
  
        ```  
        array(   
               array($var1, SQLSRV_PARAM_IN),  
               array($var2, SQLSRV_PARAM_OUT),  
               array($var3, SQLSRV_PARAM_INOUT)  
               );  
        ```  
  
4.  Führen Sie die Abfrage mit [sqlsrv\_query](../content/sqlsrv_query.md) oder mit [sqlsrv\_prepare](../content/sqlsrv_prepare.md) und [sqlsrv\_execute](../content/sqlsrv_execute.md) aus. Der folgende Code verwendet beispielsweise die Verbindung *$conn* zum Ausführen der Abfrage *$tsql* mit Parameterwerten, die in *$params*angegeben sind:  
  
    ```  
    sqlsrv_query($conn, $tsql, $params);  
    ```  
  
## Siehe auch  
[Vorgehensweise: Abrufen von Eingabe-/Ausgabeparametern mit dem SQLSRV-Treiber](../Topic/How%20to:%20Retrieve%20Output%20Parameters%20Using%20the%20SQLSRV%20Driver.md)  
[How to: Retrieve Input and Output Parameters Using the SQLSRV Driver](../Topic/How%20to:%20Retrieve%20Input%20and%20Output%20Parameters%20Using%20the%20SQLSRV%20Driver.md)  
  
