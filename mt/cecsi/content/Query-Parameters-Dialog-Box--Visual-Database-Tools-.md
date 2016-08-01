---
title: "Abfrageparameter (Dialogfeld) (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 31cdaee2-d7cd-4d64-a45f-924b27e8b1f0
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
# Abfrageparameter (Dialogfeld) (Visual Database Tools)
In diesem Dialogfeld können Sie Werte für in der Abfrage definierte Parameter eingeben. Dieses Dialogfeld wird angezeigt, wenn Sie eine Abfrage ausführen, die Parameter enthält, die End erfordern\-Benutzereingaben zur Laufzeit.  
  
## Optionen  
**Name**  
Listet die Parameter auf, die für die auszuführende Abfrage definiert sind. Wenn die Abfrage benannte Parameter enthält, werden die Namen in der Liste angezeigt. Wenn die Abfrage unbenannte Parameter System enthält\-definierten Namen für jeden Parameter in der Abfrage aufgelistet werden.  
  
**Wert**  
Geben Sie den Wert für jeden Parameter, die unter aufgeführten **Namen**. Der zuletzt verwendete Wert wird als Standardparameterwert angezeigt.  
  
## Beispiel  
Wenn die folgenden Abfrage im SQL-Bereich in der [!INCLUDE[ssSampleDBobject](../content/includes/ssSampleDBobject_md.md)]-Datenbank ausgeführt wird, wird das Dialogfeld Abfrageparameter geöffnet.  
  
```  
SELECT   FirstName, LastName  
FROM    Person.Person AS Lastname  
WHERE   (LastName = @Param1);  
```  
  
## Siehe auch  
[Abfrage mit Parametern & #40; Visual Database Tools & #41;](../content/Query-with-Parameters--Visual-Database-Tools-.md)  
  
