---
title: "Laden des PHP-SQL-Treibers"
ms.custom: na
ms.date: 06/28/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e5c114c5-8204-49c2-94eb-62ca63f5d3ec
caps.latest.revision: 41
caps.handback.revision: 40
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
# Laden des PHP-SQL-Treibers
Dieses Thema enthält Anweisungen für das Laden der [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] in den PHP verarbeitenden Speicherplatz.  
  
Es gibt zwei Optionen, um einen Treiber zu laden. Der Treiber kann geladen werden, wenn PHP gestartet wird oder während der PHP-Skriptlaufzeit.  
  
## Verschieben Sie die Treiberdatei in Ihr Erweiterungsverzeichnis  
Unabhängig davon, welches Verfahren Sie verwenden, wird im ersten Schritt die Treiberdatei in einem Verzeichnis abgelegt, wo die PHP-Laufzeit sie finden kann. Legen Sie also die Treiberdatei in Ihr PHP-Erweiterungsverzeichnis. Auf [Systemanforderungen für den PHP-SQL-Treiber](../content/System-Requirements-for-the-PHP-SQL-Driver.md) können Sie eine Liste der Treiberdateien abrufen, die mit dem [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] installiert werden.  
  
Bei Bedarf geben Sie den Speicherort der Treiberdatei in der PHP-Konfigurationsdatei \(php.ini\) an, indem Sie die Option **extension\_dir** verwenden. Wenn Sie beispielsweise die Treiberdatei in Ihr Verzeichnis „c:\\php\\ext“ einfügen, verwenden Sie diese Option:  
  
```  
extension_dir = "c:\PHP\ext"  
```  
  
## Laden des Treibers beim Starten von PHP  
Beim Laden der [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] beim Starten von PHP, verschieben Sie zunächst eine Treiberdatei in das Erweiterungsverzeichnis. Dann führen Sie folgende Schritte aus:  
  
1.  Zum Aktivieren des SQLSRV-Treibers ändern Sie **php.ini**, indem Sie die folgende Zeile im Abschnitt "Erweiterung" hinzufügen, oder ändern Sie die Zeile, die bereits vorhanden ist \(in diesem Beispiel wird die Version 3.2 threadsicherer Treiber für PHP 5.6 verwendet\):  
  
    ```  
    extension=php_sqlsrv_56_ts.dll  
    ```  
  
    Zum Aktivieren des PDO\_SQLSRV-Treibers ändern Sie **php.ini**, indem Sie die folgende Zeile im Abschnitt "Erweiterung" hinzufügen, oder ändern Sie die Zeile, die bereits vorhanden ist \(in diesem Beispiel wird die Version 3.2 threadsicherer Treiber für PHP 5.6 verwendet\):  
  
    ```  
    extension=php_pdo_sqlsrv_56_ts.dll  
    ```  
  
2.  Wenn Sie den Treiber PDO\_SQLSRV verwenden möchten, muss „php\_pdo.dll“ verfügbar sein, entweder als integrierte Erweiterung oder als dynamisch geladene Erweiterung. Wenn Sie den PDO\_SQLSRV-Treiber dynamisch laden müssen, muss die Datei „php\_pdo.dll“ im Erweiterungsverzeichnis vorhanden sein und die folgende Zeile muss in der Datei php.ini vorhanden sein:  
  
    ```php  
    extension=php_pdo.dll  
    ```  
  
3.  Starten Sie den Webserver neu.  
  
> [!NOTE]  
> Um zu bestimmen, ob der Treiber erfolgreich geladen wurde, führen Sie ein Skript aus, das [phpinfo\(\)](http://go.microsoft.com/fwlink/?LinkId=108678) aufruft.  
  
Weitere Informationen zu **php.ini** -Direktiven finden Sie unter [Beschreibung der wichtigsten php.ini-Direktiven](http://go.microsoft.com/fwlink/?LinkId=105817).  
  
## Laden des Treibers während der PHP-Skriptlaufzeit  
Beim Laden der [!INCLUDE[ssDriverPHP](../content/includes/ssDriverPHP_md.md)] während der Skriptlaufzeit verschieben Sie zunächst eine Treiberdatei in Ihr Erweiterungsverzeichnis. Dann fügen Sie die folgende Zeile am Anfang des PHP-Skripts hinzu, das den Treiber verwenden wird:  
  
```  
dl('php_pdo_sqlsrv_56_ts.dll');  
```  
  
Weitere Informationen zu PHP-Funktionen, die im Zusammenhang mit dem dynamischen Laden von Erweiterungen stehen, finden Sie unter [dl](http://go.microsoft.com/fwlink/?LinkId=105818) und [extension\_loaded](http://go.microsoft.com/fwlink/?LinkId=105819).  
  
## Siehe auch  
[Erste Schritte mit dem PHP-SQL-Treiber](../content/Getting-Started-with-the-PHP-SQL-Driver.md)
[Systemanforderungen für den PHP-SQL-Treiber](../content/System-Requirements-for-the-PHP-SQL-Driver.md)
[Programmierhandbuch für den PHP-SQL-Treiber](../content/Programming-Guide-for-PHP-SQL-Driver.md)
[SQLSRV-Treiber – API-Referenz](../content/SQLSRV-Driver-API-Reference.md)  
  
