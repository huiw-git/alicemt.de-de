---
title: "Objektabh&#228;ngigkeiten"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c63d1160-3f3d-45df-99be-6fe081125fb5
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
# Objektabh&#228;ngigkeiten
Bestimmte Datenbankobjekte sind von anderen Datenbankobjekten abhängig. Sichten und gespeicherte Prozeduren sind beispielsweise vom Vorhandensein von Tabellen abhängig, die die von der Sicht oder der Prozedur zurückgegebenen Daten enthalten. Die **Objektabhängigkeiten (Seite Allgemein)** für das aktuelle Objekt listet die Datenbankobjekte, die für das Objekt ordnungsgemäß vorhanden sein müssen und die Objekte, die vom ausgewählten Objekt abhängig. Ein Objekt, das auf ein anderes Objekt in seiner Definition verweist, die im Systemkatalog gespeicherten Definition wird aufgerufen, ein *verweisenden Entität*. Ein Objekt, das auf ein anderes Objekt verweist heißt eine *Entität verwiesen*.  
  
Die **Objektabhängigkeiten (Seite erweitert)** für das aktuelle Objekt listet die [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] Datenbankobjekte und [!INCLUDE[ssISnoversion](../content/includes/ssISnoversion_md.md)] Objekte, die vom Objekt abhängig sind. Die Objekte werden möglicherweise auf verschiedenen Servern gespeichert.  
  
Mithilfe dieses Dialogfelds können Sie sich einen Überblick über die Abhängigkeiten verschaffen, bevor Sie das ausgewählte Objekt ändern oder löschen.  
  
## Liste der Benutzeroberflächenelemente  
**Objekte, von denen abhängig** *<selected object>*  
Auf diese Schaltfläche zeigt eine Liste der Objekte, die Abhängigkeit\-nachverfolgt und, die für das ausgewählte Objekt abhängig sind.  
  
**Objekte, von denen** *<selected object>* **abhängig ist**  
Auf diese Schaltfläche zeigt eine Liste der Objekte, die Abhängigkeit\-nachverfolgt, von denen das ausgewählte Objekt abhängig ist.  
  
**Abhängigkeiten**  
Wenn **Objekte, abhängig** *<selected object>* ist geklickt haben, diese zeigt eine hierarchische Ansicht der Objekte, die vom ausgewählten Objekt abhängig sind. Wenn **Objekte, von denen** *<selected object>* **hängt** ist geklickt haben, diese zeigt eine hierarchische Ansicht der Objekte, von denen das ausgewählte Objekt abhängig ist.  
  
**Name**  
Zeigt den Namen des Objekts im ausgewählten der **Abhängigkeiten** Strukturansicht oben.  
  
**Typ**  
Zeigt den Typ des Objekts im ausgewählten der **Abhängigkeiten** Strukturansicht oben.  
  
**Letzte Synchronisierung**  
> [!NOTE]  
> Diese Option steht nur für die **Erweitert** Seite.  
  
Gibt das Datum und die Uhrzeit des letzten Updates der Abhängigkeitsinformationen an.  
  
**Abhängigkeitstyp**  
> [!NOTE]  
> Diese Option steht nur auf die **Allgemein** Seite.  
  
Zeigt den Typ der Abhängigkeit zwischen zwei Objekten an. Dabei kann es sich um eine der folgenden sein:  
  
-   Schema\-Abhängigkeit gebunden  
  
    Dies ist eine Beziehung zwischen zwei Objekten, mit der verhindert wird, dass das Objekt, auf das verwiesen wird, gelöscht oder geändert wird, solange das verweisende Objekt vorhanden ist. Ein Schema\-gebundenen Abhängigkeit wird erstellt, wenn eine Sicht oder Benutzer\-definierte Funktion erstellt mithilfe der WITH SCHEMABINDING-Klausel, oder wenn ein anderes Objekt durch eine CHECK- oder DEFAULT-Einschränkung oder in der Definition einer berechneten Spalte auf eine Tabelle verweist.  
  
-   Nicht\-Schema\-Abhängigkeit gebunden  
  
    Dies ist eine Beziehung zwischen zwei Objekten, mit der nicht verhindert wird, dass das Objekt, auf das verwiesen wird, gelöscht oder geändert wird.  
  
-   Nicht verfügbare oder nicht aufgelöste Entität  
  
    Gibt an, dass der Abhängigkeitstyp nicht bestimmt werden kann. Dies geschieht nur, wenn sich das ausgewählte Objekt auf einer Instanz von [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] befindet, bei der es sich um eine frühere Version von [!INCLUDE[ssKatmai](../content/includes/ssKatmai_md.md)] handelt.  
  
