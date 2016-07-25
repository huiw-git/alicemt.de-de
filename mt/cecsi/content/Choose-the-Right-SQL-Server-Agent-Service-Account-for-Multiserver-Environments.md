---
title: "Ausw&#228;hlen des richtigen SQL Server-Agent-Dienstkontos f&#252;r Multiserverumgebungen"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a07e2f38-281c-495b-965b-13fad03ba548
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
# Ausw&#228;hlen des richtigen SQL Server-Agent-Dienstkontos f&#252;r Multiserverumgebungen
Das Windows-Konto, das Sie für den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienst auswählen, kann sich wie im Folgenden beschrieben auf das Verhalten einer Multiserverumgebung auswirken:  
  
-   Wenn Sie den [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent-Dienst unter einem Konto ausführen, das nicht Mitglied der lokalen Windows-Administratorengruppe ist, treten beim Eintragen von Zielservern bei Masterservern u. U. Fehler auf. In diesem Fall wird die folgende Fehlermeldung zurückgegeben:  
  
    "Fehler beim Eintragungsvorgang."  
  
    Starten Sie die Dienste von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] und [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent neu, um das Problem zu beheben.  
  
-   Wenn die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienst wird ausgeführt, unter dem lokalen Systemkonto Masterserver\-Vorgänge werden nur unterstützt, wenn sowohl auf dem Masterserver und auf den Zielserver auf demselben Computer befinden. Wenn Sie diese Konfiguration verwenden, wird beim Eintragen von Zielservern bei einem Masterserver die folgende Meldung zurückgegeben:  
  
    "Sicherstellen der-Agent-Start\-Einrichten des Kontos für *< Ziel\_Server\_Computer\_Name >* Anmeldung als Zielserver besitzt."  
  
    Sie können diese zu Informationszwecken ausgegebene Meldung ignorieren. Der Eintragungsvorgang wird dennoch erfolgreich abgeschlossen.  
  
Weitere Informationen zum Auswählen eines Kontos für die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Agent-Dienst finden Sie unter [Wählen Sie ein Konto für den SQL Server-Agent-Dienst](../content/Select-an-Account-for-the-SQL-Server-Agent-Service.md).  
  
