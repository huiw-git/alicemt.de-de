---
title: "Spalteneigenschaften (Visual Database Tools)"
ms.custom: na
ms.date: 07/15/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e549a2a8-4154-4ec8-b146-614564169b39
caps.latest.revision: 5
caps.handback.revision: 4
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
# Spalteneigenschaften (Visual Database Tools)
Es gibt zwei Sätze von Eigenschaften für Spalten: einen vollständigen Satz, in dem Sie sehen die **Spalteneigenschaften** im Tabellen-Designer auf der Registerkarte (verfügbar nur für [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Datenbanken) und eine Teilmenge, die Sie im Eigenschaftenfenster im Server-Explorer sehen können.  
  
> [!NOTE]  
> Die in diesem Thema behandelten Eigenschaften sind nicht alphabetisch, sondern nach Kategorie angeordnet.  
  
> [!NOTE]  
> Die angezeigten Dialogfelder und Menübefehle können von den in der Hilfe beschriebenen abweichen. Dies hängt von Ihren aktiven Einstellungen oder Ihrer Edition ab. Wählen Sie zum Ändern Ihrer Einstellungen **Einstellungen importieren und exportieren** auf die **Tools** Menü.  
  
## Eigenschaftenfenster  
Die folgenden Eigenschaften werden im Eigenschaftenfenster angezeigt, wenn Sie im Server-Explorer eine Spalte auswählen.  
  
> [!NOTE]  
> Diese Eigenschaften mithilfe von Server-Explorer zugegriffen werden gelesen,\-nur. Um die Spalteneigenschaften für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] -Datenbanken zu bearbeiten, müssen Sie die Spalte im Tabellen-Designer auswählen. Diese Eigenschaften werden später in diesem Thema beschrieben.  
  
**Kategorie Identität**  
Erweitert die Anzeige um die **Namen** und **Datenbank** Eigenschaften.  
  
**Name**  
Zeigt den Namen der Spalte an.  
  
**Datenbank**  
Zeigt den Namen der Datenquelle für die ausgewählte Spalte an. (Gilt nur für OLE DB.)  
  
**Kategorie Verschiedenes**  
Wird erweitert, um die restlichen Eigenschaften anzuzeigen.  
  
**Datentyp**  
Zeigt den Datentyp der ausgewählten Spalte an. Weitere Informationen finden Sie unter [-Datentypen (Transact-SQL)](assetId:///a54f7373-b247-4d61-8fb8-7f2ec7a8d0a4).  
  
**ID-Schrittweite**  
Zeigt den inkrementellen Wert an, die hinzugefügt werden, die **ID-Startwert** für jede weitere Zeile der Identity-Spalte. (Gilt nur für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)].)  
  
**ID-Startwert**  
Zeigt den der ersten Tabellenzeile der Identitätsspalte zugeordneten Startwert an. (Gilt nur für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)].)  
  
**Ist Identity**  
Zeigt, ob die ausgewählte Spalte die Identity-Spalte der Tabelle ist. (Gilt nur für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)].)  
  
**Länge**  
Zeigt die Anzahl der zulässigen Zeichen für Zeichen\-Basis-Datentypen.  
  
**NULL zulassen**  
Zeigt an, ob die Spalte NULL-Werte zulässt.  
  
**Genauigkeit**  
Zeigt die maximale Anzahl der für numerische Datentypen zulässigen Stellen. Bei nicht numerischen Datentypen wird diese Eigenschaft mit **0** angegeben.  
  
**Dezimalstellen**  
Zeigt die maximale Anzahl von Stellen an, die bei numerischen Datentypen rechts vom Dezimalkomma erscheinen können. Dieser Wert muss kleiner oder gleich der Genauigkeit sein. Bei nicht numerischen Datentypen wird diese Eigenschaft mit **0** angegeben.  
  
## Registerkarte Spalteneigenschaften  
Auf diese Eigenschaften im Server-Explorer rechts\-Klicken Sie auf die Tabelle, zu der die Spalte gehört, wählen Sie **Tabellendefinition öffnen**, und wählen Sie die Zeile in der Tabelle im Tabellen-Designer.  
  
> [!NOTE]  
> Diese Eigenschaften gelten nur für [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)].  
  
**Kategorie Allgemein**  
Erweitert die Anzeige um **Namen**, **NULL-Werte zulassen**, **-Datentyp**, **Standardwert oder-Bindung**, **Länge**, **Genauigkeit**, und **Skalieren**.  
  
**Name**  
Zeigt den Namen der Spalte an. Bearbeiten Sie das Textfeld, um den Namen zu ändern.  
  
> [!CAUTION]  
> Wenn vorhandene, Ansichten, Benutzer fragt\-definierten Funktionen, gespeicherte Prozeduren oder Programme finden Sie in der Spalte, die Namensänderung wird diese Objekte ungültig.  
  
**NULL-Werte zulassen**  
Zeigt an, ob der Datentyp der Spalte NULL-Werte zulässt.  
  
**Datentyp**  
Zeigt den Datentyp der ausgewählten Spalte an. Um diese Eigenschaft zu bearbeiten, klicken Sie auf den Wert, erweitern Sie die Dropdownliste\-Liste unten, und wählen Sie einen anderen Wert. Weitere Informationen finden Sie unter [-Datentypen (Transact-SQL)](assetId:///a54f7373-b247-4d61-8fb8-7f2ec7a8d0a4).  
  
**Standardwert oder -bindung**  
Zeigt, welcher Standardwert für die Spalte verwendet wird, wenn kein Wert angegeben ist. Die Dropdownliste\--Liste enthält alle in der Datenquelle definierten globalen Standardwerte. Wählen Sie die Bindung die Spalte an einen globalen Standardwert aus der\--Liste. Sie können den Standardwert aber auch direkt als Text eingeben, um eine Standardeinschränkung für die Spalte zu erstellen.  
  
**Länge**  
Zeigt die Anzahl der zulässigen Zeichen für Zeichen\-Basis-Datentypen. Diese Eigenschaft ist nur verfügbar für Zeichen\-Basis-Datentypen.  
  
**Genauigkeit**  
Zeigt die maximale Anzahl der für numerische Datentypen zulässigen Stellen. Bei nicht numerischen Datentypen wird diese Eigenschaft mit **0** angegeben. Diese Eigenschaft ist nur für numerische Datentypen verfügbar.  
  
**Dezimalstellen**  
Zeigt die maximale Anzahl von Stellen an, die bei numerischen Datentypen rechts vom Dezimalkomma erscheinen können. Dieser Wert muss kleiner oder gleich der Genauigkeit sein. Bei nicht numerischen Datentypen wird diese Eigenschaft mit **0** angegeben. Diese Eigenschaft ist nur für numerische Datentypen verfügbar.  
  
**Kategorie Tabellen-Designer**  
Wird erweitert, um die restlichen Eigenschaften anzuzeigen.  
  
**Sortierung**  
Zeigt die Sortierungseinstellung der ausgewählten Spalte an. Um diese Einstellung zu ändern, klicken Sie auf **Sortierung** und klicken Sie dann auf die Auslassungspunkte **(...)** rechts neben dem Wert.  
  
**Spezifikationskategorie der berechneten Spalte**  
Erweitert die Anzeige um Eigenschaften für **Formel** und **wird beibehalten,**. Wenn die Spalte berechnet ist, wird außerdem die Formel angezeigt. Um die Formel zu bearbeiten, erweitern Sie diese Kategorie, und bearbeiten Sie sie in der **Formel** Eigenschaft.  
  
**Formel**  
Zeigt, wenn es sich um eine berechnete Spalte handelt, die von der ausgewählten Spalte verwendete Formel. In diesem Feld können Sie eine Formel angeben oder ändern.  
  
**Ist beständig**  
Ermöglicht das Speichern der berechneten Spalte mit der Datenquelle. Eine persistente berechnete Spalte kann indiziert werden.  
  
**Datentyp-Kurzform**  
Zeigt die Informationen zum Felddatentyp an, im gleichen Format wie in der SQL-Anweisung CREATE TABLE. Z. B. ein Feld, die eine Variable\-Zeichenfolge der Länge mit einer maximalen Länge von 20 Zeichen dargestellt werden würde, als "varchar(20)"." Um diese Eigenschaft zu ändern, geben Sie den Wert direkt ein.  
  
**Beschreibung**  
Zeigt die Beschreibung der Spalte an. Um die vollständige Beschreibung anzuzeigen oder zu bearbeiten, klicken Sie auf Beschreibung, und klicken Sie dann auf die Auslassungspunkte **(...)** rechts neben der Eigenschaft.  
  
**Vollständige\-Text Angabe-Kategorie**  
Erweitert die Anzeige um Eigenschaften für vollständige\-Text-Spalten.  
  
**Ist Full\-Text indiziert**  
Gibt an, ob diese Spalte voll ist\-volltextindiziert. Diese Eigenschaft kann festgelegt werden, um **Ja** nur, wenn der Datentyp für diese Spalte vollständige ist\-Text durchsucht werden kann und in die Tabelle, zu der diese Spalte gehört, eine vollständige\-Textindex dafür angegeben. Um diesen Wert zu ändern, klicken Sie darauf, erweitern Sie die Dropdownliste\-Liste unten, und wählen Sie einen neuen Wert.  
  
**Vollständige\-Text-Spalte**  
Zeigt, welche Spalte verwendet wird, um den Dokumenttyp einer Spalte vom Typ Image zu definieren. Der Datentyp Image kann verwendet werden, um Dokumente zu speichern, die von DOC-Dateien bis zu XML-Dateien reichen.  
  
**Sprache**  
Gibt die für die Indizierung der Spalte verwendete Sprache an.  
  
**Statistische Semantik**  
Wählen Sie aus, ob die statistische semantische Indizierung für die ausgewählte Spalte aktiviert werden soll. Weitere Informationen finden Sie unter [semantische Suche Platzhalter](assetId:///cd8faa9d-07db-420d-93f4-a2ea7c974b97).  
  
Wenn Sie eine **Sprache** vor der Option **Statistische Semantik**auswählen und die ausgewählte Sprache über kein zugeordnetes semantisches Sprachmodell verfügt, ist die Option **Statistische Semantik** auf **Nein** festgelegt, und sie kann nicht geändert werden. Wenn Sie die Option **Statistische Semantik** auf **Ja** festlegen, bevor Sie eine **Sprache**auswählen, sind in der Spalte **Sprache** nur die Sprachen verfügbar, für die das semantische Sprachmodell unterstützt wird.  
  
**Verfügt nicht über\-SQL Server-Abonnenten**  
Zeigt an, ob die Spalte nicht hat\-Microsoft SQL Server-Abonnenten.  
  
**Identitätsspezifikationskategorie**  
Erweitert die Anzeige um Eigenschaften für **ist Identity**, **ID-Schrittweite**, und **ID-Startwert**.  
  
**Ist Identity**  
Zeigt, ob die ausgewählte Spalte die Identity-Spalte der Tabelle ist. Um die Eigenschaft zu ändern, öffnen Sie die Tabelle im Tabellen-Designer, und bearbeiten Sie die Eigenschaften in der **Eigenschaften** Fenster. Diese Einstellung gilt nur für Spalten mit einer Anzahl\--Datentyp, wie z. B. basierend *Int*.  
  
**ID-Schrittweite**  
Zeigt den inkrementellen Wert an, die hinzugefügt werden, die **ID-Startwert** für jede weitere Zeile. Wenn Sie nichts eingeben, wird standardmäßig der Wert 1 zugewiesen. Um diese Eigenschaft zu bearbeiten, geben Sie den Wert direkt ein.  
  
**ID-Startwert**  
Zeigt den der ersten Zeile der Tabelle zugewiesenen Wert an. Wenn Sie nichts eingeben, wird standardmäßig der Wert 1 zugewiesen. Um diese Eigenschaft zu bearbeiten, geben Sie den Wert direkt ein.  
  
**Ist deterministisch**  
Zeigt, ob der Datentyp der ausgewählten Spalte mit Sicherheit bestimmt werden kann.  
  
**DTS ist\-veröffentlicht**  
Zeigt an, ob die Spalte DTS\-veröffentlicht.  
  
**Ist indizierbar**  
Zeigt, ob die ausgewählte Spalte indiziert werden kann. Z. B. nicht\-nichtdeterministische, berechnete Spalten können nicht indiziert werden.  
  
**Ist "Merge"\-veröffentlicht**  
Zeigt an, ob die Spalte Merge\-veröffentlicht.  
  
**Ist nicht zu replizieren**  
Gibt an, ob die ursprünglichen Identitätswerte bei der Replikation erhalten bleiben. Um diese Eigenschaft zu bearbeiten, klicken Sie auf den Wert, erweitern Sie die Dropdownliste\-Liste unten, und wählen Sie einen anderen Wert.  
  
**Ist repliziert**  
Zeigt, ob diese Spalte an einem anderen Speicherort repliziert wird.  
  
**Ist RowGuid**  
Gibt an, ob [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] die Spalte als ROWGUID verwendet. Sie können diesen Wert festlegen, um **Ja** nur für eine Spalte mit dem Datentyp der **Uniqueidentifier**. Um diese Eigenschaft zu bearbeiten, klicken Sie auf den Wert, erweitern Sie die Dropdownliste\-Liste unten, und wählen Sie einen anderen Wert.  
  
**Schriftgrad**  
Zeigt die für den Datentyp der Spalte zulässige Größe in Byte an. Zum Beispiel eine **Nchar** -Datentyp kann eine Länge von 10 (die Anzahl der Zeichen) besitzen, aber haben eine Größe von 20 Unicode-Zeichensätze.  
  
> [!NOTE]  
> Die Länge einer **varchar(max)** -Datentyps variiert für jede Zeile. SP\_Hilfe gibt (\-1) als die Länge des **varchar(max)** Spalte. [!INCLUDE[ssManStudio](../content/includes/ssManStudio_md.md)] Zeigt \-1 als die Größe der Spalte.  
  
