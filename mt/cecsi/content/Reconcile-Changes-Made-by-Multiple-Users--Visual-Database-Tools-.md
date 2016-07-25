---
title: "Abstimmen der &#196;nderungen von mehreren Benutzern (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fc7ed4f2-ad3d-47fc-a3ef-51e5bb069ef0
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
# Abstimmen der &#196;nderungen von mehreren Benutzern (Visual Database Tools)
In einer Mehrbenutzerumgebung können mehrere Benutzer gleichzeitig Änderungen an ein und demselben Objekt vornehmen. Diese Situation kann auftreten, wenn Sie an der Struktur des Objekts im Tabellen-Designer oder im Datenbankdiagramm-Designer arbeiten, oder bei Ergebniswerten, die im Ergebnisbereich des Abfrage- und Sicht-Designers zurückgegeben werden. Dies kann Konflikte verursachen, die aufgelöst werden sollten.  
  
## Konflikte im Tabellen-Designer oder im Datenbankdiagramm-Designer  
Beispielsweise kann ein Benutzer eine Tabelle löschen oder umbenennen, während Sie gerade an derselben Tabelle oder einer verknüpften Tabelle im Tabellen-Designer arbeiten. Wenn Sie versuchen, die Tabelle speichern die [Datenbank Änderungen festgestellt (Dialogfeld) & #40; Visual Database Tools & #41;](../content/Database-Changes-Detected-Dialog-Box--Visual-Database-Tools-.md) benachrichtigt Sie, dass die Datenbank nach dem Öffnen der Tabelle aktualisiert wurde.  
  
In diesem Dialogfeld finden Sie auch eine Liste der Datenbankobjekte, die durch das Speichern der Tabelle beeinflusst werden. Sie können hier eine der folgenden Aktionen ausführen:  
  
-   Wählen Sie **Ja** Speichern Sie die Tabelle, und aktualisieren die Datenbank mit allen Änderungen in der Liste.  
  
    Diese Aktion kann sich auch auf Tabellen auswirken, die dieselben Datenbankobjekte nutzen. Nehmen wir beispielsweise an, Sie bearbeiten die `au`\_`id` -Spalte in der `titleauthors` Tabelle, während ein anderer Benutzer arbeitet der `authors` verknüpft ist die `titleauthors` Tabelle, indem Sie die `au`\_`id` Spalte. Wenn Sie Ihre Tabelle speichern, wirkt sich dies auf die Tabelle des anderen Benutzers aus. Ein ähnlicher Fall liegt vor, wenn ein anderer Benutzer in der Tabelle `qty` eine CHECK-Einschränkung für die Spalte `sales` definiert hat. Wenn Sie die Spalte `qty` löschen und die Tabelle `sales` speichern, wirkt sich dies auf die CHECK-Einschränkung des anderen Benutzers aus.  
  
-   Wählen Sie **Nr.** um den Speichervorgang abzubrechen Aktion.  
  
    Sie können die Tabelle jetzt schließen, ohne sie zu speichern. Wenn Sie die Tabelle erneut öffnen, wird diese mit dem Inhalt der Datenbank angepasst.  
  
-   Wählen Sie **Textdatei speichern** um eine Liste der Änderungen zu speichern.  
  
    Sie können die Liste der datenbankänderungen in speichern die **Datenbank Änderungen erkannt** im Dialogfeld Text-Datei, damit Sie die Ursache der Änderungen anderer Benutzer untersuchen können. Wenn ein anderer Benutzer z. B. eine Tabelle geändert hat, die Sie zum Löschen ausgewählt haben, können Sie überprüfen, ob die Tabelle vor dem Aktualisieren der Datenbank gelöscht werden soll.  
  
## Konflikte im Abfrage- und Sicht-Designer  
Wenn Sie eine Abfrage ausführen oder die Ergebnisse einer Ansicht zurückgeben, sehen Sie die Daten der [im Ergebnisbereich](../content/Results-Pane--Visual-Database-Tools-.md). Da mehrere Benutzer gleichzeitig an derselben Gruppe von Daten arbeiten können, kann es zu Konflikten kommen.  
  
Beispielsweise führen Sie und ein Kollege jeweils eine Abfrage aus, um die gesamten Daten in der Tabelle `titleauthors` anzuzeigen. Ihr Kollege ändert den ersten Namen im ersten zurückgegebenen Datensatz von Barb in Barbara. Zu diesem Zeitpunkt enthält dieses Feld in der Datenbank Barbara, während in Ihrem Resultset immer noch Barb angezeigt wird. Sie geben jetzt Barbara ein und klicken auf eine Stelle außerhalb der Zeile. Daraufhin erhalten Sie eine Meldung, in der Sie zum Auflösen des Konflikts aufgefordert werden.  
  
-   Klicken Sie auf **Ja** zum Aktualisieren der Datenbank mit den Änderungen.  
  
    Dadurch werden die Änderungen Ihres Kollegen überschrieben.  
  
-   Klicken Sie auf **keine** haben das Resultset mit den aktuellen in der Datenbank aktualisieren.  
  
    Dadurch werden Ihre Änderungen mit den Änderungen Ihres Kollegen überschrieben.  
  
-   Klicken Sie auf **Abbrechen** Weiter bearbeiten, ohne den Konflikt aufzulösen.  
  
    In diesem Fall können Sie Ihre Änderungen nicht in die Datenbank übernehmen.  
  
## Siehe auch  
[Datenbankänderungen erkannt Dialogfeld & #40; Visual Database Tools & #41;](../content/Database-Changes-Detected-Dialog-Box--Visual-Database-Tools-.md)  
  
