---
title: "Auftragsschritt-Eigenschaften - Neuer Auftragsschritt (Seite erweitert)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bdecfd4f-bcd8-4ba2-8ada-fbb636314f40
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
# Auftragsschritt-Eigenschaften - Neuer Auftragsschritt (Seite erweitert)
Verwenden Sie diese Seite zum Anzeigen und Ändern der Eigenschaften einer [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Agent-Auftragsschritt.  
  
## Optionen  
**Aktion bei Erfolg**  
Legt fest, welche Aktion der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent bei erfolgreicher Auftragsausführung ausführen soll.  
  
**Wiederholungsversuche**  
Legt fest, wie oft vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent versucht werden soll, einen fehlgeschlagenen Auftragsschritt erneut auszuführen.  
  
**Wiederholungsintervall (Min)**  
Legt fest, wie lange der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent bis zum nächsten Wiederholungsversuch warten soll.  
  
**Aktion bei Fehler**  
Legt fest, welche Aktion der [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Agent bei Fehlschlagen des Auftrags ausführen soll.  
  
## Optionen für Transact\-SQL-Auftragsschritte  
**Ausgabedatei**  
Legt fest, welche Datei für die Ausgabe aus dem Auftragsschritt verwendet werden soll. Diese Option steht nur für Mitglieder der **Sysadmin** festen Serverrolle.  
  
**...**  
Nach der Datei, die für die Ausgabe aus dem Auftragsschritt verwendet werden soll, können Sie suchen.  
  
**Sicht**  
In [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)], diese Schaltfläche ist für die Anzeige von Ausgabedateien deaktiviert. Nutzen Sie stattdessen den Editor für die Anzeige von Auftragsschritt-Ausgabedateien.  
  
**Ausgabe an vorhandene Datei anfügen**  
Fügt die Ausgabe an den vorhandenen Inhalt der Datei an. Andernfalls wird der vorige Inhalt der Datei bei jeder Ausführung des Auftragsschritts überschrieben.  
  
**In Tabelle protokollieren**  
Protokolliert die Ausgabe der Auftragsschritte, die **Sysjobstepslogs** -Tabelle in der **Msdb** Datenbank.  
  
**Sicht**  
Nachdem der Auftragsschritt mindestens einmal ausgeführt wurde, klicken Sie auf **Ansicht** um die Ausgabe in der Tabelle anzuzeigen.  
  
**Ausgabe an vorhandenen Eintrag in Tabelle anfügen**  
Fügt die Ausgabe an den vorhandenen Inhalt der Tabelle an. Andernfalls wird der vorige Inhalt der Tabelle bei jeder Ausführung des Auftragsschritts überschrieben.  
  
**Schrittausgabe in Verlauf einschließen**  
Wählen Sie diese Option aus, wenn die Ausgabe des Auftragsschritts in den Auftragsverlauf aufgenommen werden soll.  
  
**Ausführen als Benutzer**  
Wenn Sie ein Mitglied der **Sysadmin** festen Serverrolle können Sie einen anderen SQL-Anmeldenamen Ausführung dieses Auftragsschritts auswählen.  
  
## Optionen für Auftragsschritte des Betriebssystems (CmdExec)  
**Ausgabedatei**  
Legt fest, welche Datei für die Ausgabe aus dem Auftragsschritt verwendet werden soll.  
  
**...**  
Nach der Datei, die für die Ausgabe aus dem Auftragsschritt verwendet werden soll, können Sie suchen.  
  
**Sicht**  
In [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)], diese Schaltfläche ist für die Anzeige von Ausgabedateien deaktiviert. Nutzen Sie stattdessen den Editor für die Anzeige von Auftragsschritt-Ausgabedateien.  
  
**Ausgabe an vorhandene Datei anfügen**  
Fügt die Auftragsschrittausgabe bei jeder Ausführung des Schritts an den vorhandenen Inhalt der Datei an.  
  
**In Tabelle protokollieren**  
Protokolliert die Ausgabe der Auftragsschritte, die **Sysjobstepslogs** -Tabelle in der **Msdb** Datenbank.  
  
**Sicht**  
Nachdem der Auftragsschritt mindestens einmal ausgeführt wurde, klicken Sie auf **Ansicht** um die Ausgabe in der Tabelle anzuzeigen.  
  
**Ausgabe an vorhandenen Eintrag in Tabelle anfügen**  
Fügt die Ausgabe an den vorhandenen Inhalt der Tabelle an. Andernfalls wird der vorige Inhalt der Tabelle bei jeder Ausführung des Auftragsschritts überschrieben.  
  
**Schrittausgabe in Verlauf einschließen**  
Wählen Sie diese Option aus, wenn die Ausgabe des Auftragsschritts in den Auftragsverlauf aufgenommen werden soll.  
  
## Optionen für PowerShell-Auftragsschritte  
**Ausgabedatei**  
Legt fest, welche Datei für die Ausgabe aus dem Auftragsschritt verwendet werden soll.  
  
**...**  
Nach der Datei, die für die Ausgabe aus dem Auftragsschritt verwendet werden soll, können Sie suchen.  
  
**Sicht**  
In [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)], diese Schaltfläche ist für die Anzeige von Ausgabedateien deaktiviert. Nutzen Sie stattdessen den Editor für die Anzeige von Auftragsschritt-Ausgabedateien.  
  
**Ausgabe an vorhandene Datei anfügen**  
Fügt die Auftragsschrittausgabe bei jeder Ausführung des Schritts an den vorhandenen Inhalt der Datei an.  
  
**In Tabelle protokollieren**  
Protokolliert die Ausgabe der Auftragsschritte, die **Sysjobstepslogs** -Tabelle in der **Msdb** Datenbank.  
  
**Sicht**  
Nachdem der Auftragsschritt mindestens einmal ausgeführt wurde, klicken Sie auf **Ansicht** um die Ausgabe in der Tabelle anzuzeigen.  
  
**Ausgabe an vorhandenen Eintrag in Tabelle anfügen**  
Fügt die Ausgabe an den vorhandenen Inhalt der Tabelle an. Andernfalls wird der vorige Inhalt der Tabelle bei jeder Ausführung des Auftragsschritts überschrieben.  
  
**Schrittausgabe in Verlauf einschließen**  
Wählen Sie diese Option aus, wenn die Ausgabe des Auftragsschritts in den Auftragsverlauf aufgenommen werden soll.  
  
## Optionen für Auftragsschritte des Replikation-Warteschlangenlesers  
**Server**  
Legt fest, welcher Server für einen Auftragsschritt des Replikation-Warteschlangenlesers verwendet werden soll.  
  
**Datenbank**  
Legt fest, welche Datenbank für einen Auftragsschritt des Replikation-Warteschlangenlesers verwendet werden soll.  
  
## Optionen für Auftragsschritte von SQL Server Analysis Services  
**Ausgabedatei**  
Legt fest, welche Datei für die Ausgabe aus dem Auftragsschritt verwendet werden soll. Diese Option steht nur für Mitglieder der **Sysadmin** festen Serverrolle.  
  
**...**  
Nach der Datei, die für die Ausgabe aus dem Auftragsschritt verwendet werden soll, können Sie suchen.  
  
**Sicht**  
In [!INCLUDE[ssCurrent](../content/includes/ssCurrent_md.md)] ist diese Schaltfläche für die Anzeige von Ausgabedateien deaktiviert. Nutzen Sie stattdessen den Editor für die Anzeige von Auftragsschritt-Ausgabedateien.  
  
**Ausgabe an vorhandene Datei anfügen**  
Fügt die Ausgabe an den vorhandenen Inhalt der Datei an. Andernfalls wird der vorige Inhalt der Datei bei jeder Ausführung des Auftragsschritts überschrieben.  
  
**In Tabelle protokollieren**  
Protokolliert die Ausgabe der Auftragsschritte, die **Sysjobstepslogs** -Tabelle in der **Msdb** Datenbank.  
  
**Sicht**  
Nachdem der Auftragsschritt mindestens einmal ausgeführt wurde, klicken Sie auf **Ansicht** um die Ausgabe in der Tabelle anzuzeigen.  
  
**Ausgabe an vorhandenen Eintrag in Tabelle anfügen**  
Fügt die Ausgabe an den vorhandenen Inhalt der Tabelle an. Andernfalls wird der vorige Inhalt der Tabelle bei jeder Ausführung des Auftragsschritts überschrieben.  
  
**Schrittausgabe in Verlauf einschließen**  
Wählen Sie diese Option aus, wenn die Ausgabe des Auftragsschritts in den Auftragsverlauf aufgenommen werden soll.  
  
## Siehe auch  
[Verwalten von Auftragsschritten](../content/Manage-Job-Steps.md)  
  
