---
title: "Verbindung mit Server herstellen (Seite &#39;Zus&#228;tzliche Verbindungsparameter&#39;)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ba34b01a-6289-4eb8-8341-fa3d9ec87b3f
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
# Verbindung mit Server herstellen (Seite &#39;Zus&#228;tzliche Verbindungsparameter&#39;)
Im Dialogfeld **Verbinden mit** von [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)] werden die gängigsten Verbindungszeichenfolgenwerte als Optionen angezeigt. Mithilfe der Seite **Zusätzliche Verbindungsparameter** können Sie der Verbindungszeichenfolge weitere Verbindungsparameter hinzufügen.  
  
-   Zusätzliche Verbindungsparameter können beliebige ODBC-Verbindungsparameter sein.  
  
-   Zusätzliche Verbindungsparameter hinzugefügt werden sollen, im Format **; parameter1\=Wert1; parameter2\=value2**.  
  
-   Parameter, die mithilfe der Seite **Zusätzliche Verbindungsparameter** hinzugefügt werden, werden den Parametern hinzugefügt, die mithilfe der Optionen des Dialogfelds **Verbinden mit** ausgewählt wurden.  
  
-   Durch die letzte Instanz eines Parameters werden alle vorherigen Instanzen des Parameters überschrieben. Parameter, die mithilfe der Seite **Zusätzliche Verbindungsparameter** hinzugefügt werden, orientieren sich an den Parametern, die auf den Registerkarten **Anmeldung** und **Verbindungseigenschaften** bereitgestellt sind, und ersetzen diese. Z. B. wenn die **Anmeldung** bietet die Registerkarte **SERVER1** als die **Servername**, und die **zusätzliche Verbindungsparameter** Seite enthält **; SERVER\=SERVER2**, wird die Verbindung hergestellt werden **SERVER2**.  
  
-   Parameter, die mithilfe der Seite **Zusätzliche Verbindungsparameter** hinzugefügt wurden, werden immer als Nur-Text übergeben.  
  
    > [!IMPORTANT]  
    > Auf der Seite **Zusätzliche Verbindungsparameter** dürfen keine Anmeldeinformationen und Kennwörter eingefügt werden. Sie werden nicht verschlüsselt, wenn sie über das Netzwerk übergeben werden. Verwenden Sie stattdessen die Registerkarte **Anmeldung** .  
  
## Aufgabenliste  
  
### So zeigen Sie die Seite 'Zusätzliche Verbindungsparameter' an  
  
1.  Zeigen Sie in [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)]im Menü **Abfrage** auf **Verbindung**, und klicken Sie dann auf **Verbinden**.  
  
2.  Klicken Sie im Dialogfeld **Verbinden mit** auf **Optionen**, und klicken Sie dann auf die Registerkarte **Zusätzliche Verbindungsparameter** .  
  
## Beispiele  
  
### Beispiel A: Herstellen einer Verbindung mit dem Datenbankmodul  
Um eine Verbindung mit der [!INCLUDE[ssSampleDBnormal](../content/includes/ssSampleDBnormal_md.md)] -Datenbank auf einem Server mit dem Namen ACCOUNTING herzustellen, geben Sie auf der Seite **Zusätzliche Verbindungsparameter** Folgendes ein:  
  
```  
;SERVER=ACCOUNTING;DATABASE=AdventureWorks2012  
```  
  
### Beispiel B: Herstellen einer Verbindung mit Analysis Services  
Um eine Verbindung mit der Analysis-Server herstellen und bewirken, dass alle Partitionen überwacht Benachrichtigungen in Echtzeit (caching umgangen wird) abgefragt werden und für rückschreibewert auf 5 festzulegen, geben Sie Folgendes in die **zusätzliche Verbindungsparameter** Seite:  
  
```  
;Real Time Olap=TRUE;Writeback Timeout=5  
```  
  
