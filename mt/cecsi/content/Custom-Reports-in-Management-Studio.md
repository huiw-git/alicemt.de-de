---
title: "Benutzerdefinierte Berichte in Management Studio"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1ba3f758-f39b-4f5f-91ca-516cedc78979
caps.latest.revision: 5
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
# Benutzerdefinierte Berichte in Management Studio
In [!INCLUDE[ssManStudioFull](../content/includes/ssManStudioFull_md.md)], viele Objekt-Explorer-Knoten ein Satz von Standardberichten durch die erstellte angezeigt [!INCLUDE[msCoName](../content/includes/msCoName_md.md)]. In diesen Berichten werden häufig angeforderte Serverinformationen zusammengefasst. Beginnend mit [!INCLUDE[ssVersion2005](../content/includes/ssVersion2005_md.md)] Service Pack 2, Administratoren können benutzerdefinierte Berichte ausführen, die in erstellt wurden [!INCLUDE[ssBIDevStudioFull](../content/includes/ssBIDevStudioFull_md.md)] aus [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)].  
  
## Implementierung  
Benutzerdefinierte Berichte werden als RDL-Dateien gespeichert und mithilfe der Berichtsdefinitionssprache (Report Definition Language, RDL) erstellt. In der Berichtsdefinitionssprache sind Informationen zum Datenabruf und Datenlayout für einen Bericht in einem XML-Format enthalten. Die Berichtsdefinitionssprache ist ein offenes Schema. Entwickler können die Berichtsdefinitionssprache mit zusätzlichen Attributen und Elementen erweitern. Jede gültige [!INCLUDE[tsql](../content/includes/tsql_md.md)]-Anweisung in einem Bericht kann von Berichten ausgeführt wird.  
  
Wurde für den Objekt-Explorer eine Verbindung mit einem Server hergestellt, können benutzerdefinierte Berichte im Kontext der aktuellen Objekt-Explorer-Auswahl ausgeführt werden, wenn von den Berichten auf Berichtsparameter dieses Knotens verwiesen wird. Dadurch wird ermöglicht, dass im Bericht der aktuelle Kontext (beispielsweise die aktuelle Datenbank) oder ein konsistenter Kontext (beispielsweise die Angabe einer designierten Datenbank als Teil der im benutzerdefinierten Bericht enthaltenen [!INCLUDE[tsql](../content/includes/tsql_md.md)]-Anweisung) verwendet wird.  
  
## Ausführen eines benutzerdefinierten Berichts  
Es gibt folgenden Möglichkeiten zum Ausführen eines benutzerdefinierten Berichts in [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)]:  
  
-   Rechts\-Klicken Sie auf einen Knoten im Objekt-Explorer, zeigen Sie auf **Berichte** und linken\-Klicken Sie auf **benutzerdefinierte Berichte**. In der **Datei öffnen** Klicken Sie im Dialogfeld Suchen Sie einen Ordner mit RDL-Dateien, und öffnen Sie dann die entsprechende Berichtsdatei.  
  
-   Rechts\-Klicken Sie auf einen Knoten im Objekt-Explorer, zeigen Sie auf **Berichte**, zeigen Sie auf **benutzerdefinierte Berichte**, und wählen Sie dann einen benutzerdefinierten Bericht aus der Liste der zuletzt verwendeten Dateien.  
  
## Einschränkungen  
Berücksichtigen Sie bei der Verwendung benutzerdefinierter Berichte die folgenden Einschränkungen:  
  
-   Um die unbeabsichtigte Ausführung von bösartigem Code zu verhindern, kann [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] auch dann nicht für das automatische Ausführen eines Berichts konfiguriert werden, wenn das Dateisystem so konfiguriert ist, dass RDL-Dateien [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] zugeordnet werden. In [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] können Berichte weder programmgesteuert noch an der Eingabeaufforderung über [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] ausgeführt werden.  
  
-   Benutzerdefinierte Berichte können in einem Kontext ausgeführt werden, in dem die erwarteten Werte nicht erstellt werden. Sie können beispielsweise einen Bericht über die Replikation im Kontext einer Datenbank ausführen, die nicht in der Replikation involviert ist, oder Sie können einen Bericht als ein Benutzer ausführen, der nicht über die Berechtigung für den Zugriff auf Informationen verfügt, die zum Generieren eines präzisen Berichts erforderlich sind. Der Ersteller des benutzerdefinierten Berichts ist für die Gültigkeit der Berichtsstruktur und seines Kontexts verantwortlich.  
  
-   Sie können der Liste der Standardberichte keinen benutzerdefinierten Bericht hinzufügen.  
  
-   Der vom Bericht verarbeitete Code kann möglicherweise Auswirkungen auf die Serverleistung haben.  
  
-   Unterberichte werden von benutzerdefinierten Berichten nicht unterstützt.  
  
-   Der Befehlstext für die einzelnen Abfragen im Bericht darf nicht über einen Ausdruck definiert sein.  
  
-   Mit jedem in einem Befehl (Abfrage) verwendeten Abfrageparameter kann nur auf einen einzelnen Berichtsparameter verwiesen werden. Ausdrucksoperatoren können nicht verwendet werden.  
  
-   Für Berichtsbefehle (Abfragen) werden nur Befehle vom Typ Text und gespeicherte Prozedur unterstützt.  
  
-   Das Berichtsframework bietet keine Parameter zum Erstellen von Escapezeichen für die Abfragen. Abfrageautoren müssen sicherstellen, dass ihre Abfragen frei von SQL Injection-Angriffen sind.  
  
## Verwalten von benutzerdefinierten Berichten  
Für Benutzer, die über eine Vielzahl benutzerdefinierter Berichte verfügen, empfiehlt es sich, diese mithilfe der Dateisystemordner zu organisieren, die über entsprechende NTFS-Dateisystemberechtigungen verfügen.  
  
## Berechtigungen  
Benutzerdefinierte Berichte werden mithilfe der Berechtigungen des aktuellen Benutzers ausgeführt. Berechtigungen für den Dateisystemordner mit den Berichtsdateien müssen so festgelegt werden, dass der Zugriff eingeschränkt wird, um das Ändern der vom Bericht ausgeführten Abfragen durch einen böswilligen Benutzer zu verhindern.  
  
Sowohl für den Benutzer als auch für das vom [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)]-Dienst verwendete Konto ist Lesezugriff auf den Dateisystemordner mit den Berichtsdateien erforderlich.  
  
Jeder gültige [!INCLUDE[dnprdnshort](../content/includes/dnprdnshort_md.md)]-Befehl kann in einen Bericht eingebettet werden, der Befehl wird jedoch nicht ausgeführt.  
  
> [!CAUTION]  
> Jede gültige [!INCLUDE[tsql](../content/includes/tsql_md.md)]-Anweisung kann in einem Bericht eingebettet und von einem Bericht aus ausgeführt werden. Ausführen eines Berichts unter hoher\-privilegiertes Benutzerkonto ermöglicht eine problemlose Ausführung dieser eingebetteten Anweisungen.  
  
## Beispielberichte  
[Beispielberichte](http://go.microsoft.com/fwlink/?LinkId=81792), einschließlich der Standardberichte, die vom erstellten [!INCLUDE[msCoName](../content/includes/msCoName_md.md)], zum Download zur Verfügung. Diese Beispiele können mithilfe von [!INCLUDE[ssBIDevStudioFull](../content/includes/ssBIDevStudioFull_md.md)] geändert werden.  
  
## Siehe auch  
[Hinzufügen eines benutzerdefinierten Berichts zu Management Studio](../content/Add-a-Custom-Report-to-Management-Studio.md)  
[Aufheben der Unterdrückung von Warnungen für das Ausführen von benutzerdefinierten Berichten](../content/Unsuppress-Run-Custom-Report-Warnings.md)  
[Verwenden benutzerdefinierter Berichte mit Eigenschaften von Objekt-Explorer-Knoten](../content/Use-Custom-Reports-with-Object-Explorer-Node-Properties.md)  
  
