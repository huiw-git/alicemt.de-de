---
title: "CHECK-Einschr&#228;nkungsausdruck (Dialogfeld) (Visual Database Tools)"
ms.custom: na
ms.date: 07/27/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tools-ssms
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: beb6ce43-3913-4d66-8826-8e885335b790
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
# CHECK-Einschr&#228;nkungsausdruck (Dialogfeld) (Visual Database Tools)
Wenn Sie eine CHECK-Einschränkung einer Tabelle oder Spalte anfügen, müssen Sie einen SQL-Ausdruck einschließen. Geben Sie den CHECK-Einschränkungsausdruck in das zur Verfügung gestellte Feld ein.  
  
## Liste der Benutzeroberflächenelemente  
Ausdruck  
Geben Sie den Ausdruck ein.  
  
Sie können einen einfachen Einschränkungsausdruck erstellen, um Daten auf eine einfache Bedingung zu prüfen. Sie können aber auch einen komplexen Ausdruck mithilfe boolescher Operatoren erstellen, um Daten auf mehrere Bedingungen zu prüfen. Nehmen wir beispielsweise an, die Authors-Tabelle hat eine Spalte Zip, wobei 5\-Ziffernzeichenfolge erforderlich ist. Einschränkungsausdruck stellt sicher, dass nur 5\-Ziffern sind zulässig:  
  
```  
zip LIKE '[0-9][0-9][0-9][0-9][0-9]'  
```  
  
Angenommen, die Tabelle sales enthält die Spalte qty, für die ein Wert größer als 0 erforderlich ist. Die folgende Einschränkung stellt sicher, dass nur positive Werte zulässig sind:  
  
```  
qty > 0  
```  
  
Ein weiteres Beispiel: Die orders-Tabelle schränkt die Art der Kreditkarten ein, die für Kreditkartenaufträge akzeptiert werden. Die folgende Einschränkung stellt sicher, dass nur Visa-, MasterCard- oder American Express-Kreditkarten akzeptiert werden, wenn als Zahlungsmittel für den Auftrag eine Kreditkarte verwendet wird.  
  
```  
NOT (payment_method = 'credit card') OR  
   (card_type IN ('VISA', 'MASTERCARD', 'AMERICAN EXPRESS'))  
```  
  
## So definieren Sie einen Einschränkungsausdruck  
Geben Sie auf der Registerkarte Einschränkungen überprüfen der Eigenschaftenseiten einen Ausdruck in das Feld Einschränkungsausdruck ein. Verwenden Sie dabei die folgende Syntax:  
  
<pre>{Konstante | Column_name | Funktion | (Unterabfrage)}  
[{Operator | UND | ODER | NICHT}  
{Konstante | Column_name | Funktion | (Unterabfrage)} ...]</pre>  
  
Die SQL-Syntax besteht aus folgenden Parametern:  
  
|Parameter|Beschreibung|  
|-------------|---------------|  
|Konstante|Ein Literalwert, wie numerische Daten oder Zeichendaten. Zeichendaten müssen in einfache Anführungszeichen (') eingeschlossen werden.|  
|Spalte\_Namen|Gibt eine Spalte an.|  
|Funktion|Eine integrierte\-in der Funktion.|  
|Operator|Arithmetischer oder bitweiser Operator bzw. ein Vergleichs- oder Zeichenfolgenoperator.|  
|AND|Wird in booleschen Ausdrücken verwendet, um zwei Ausdrücke miteinander zu verbinden. Wenn beide Ausdrücke True sind, werden Ergebnisse zurückgegeben.<br /><br />Wenn in einer Anweisung sowohl AND als auch OR verwendet werden, wird AND zuerst verarbeitet. Sie können die Reihenfolge der Ausführung ändern, indem Sie Klammern verwenden.|  
|OR|Wird in booleschen Ausdrücken verwendet, um zwei oder mehr Bedingungen miteinander zu verbinden. Wenn eine der beiden Bedingungen True ist, werden Ergebnisse zurückgegeben.<br /><br />Wenn in einer Anweisung sowohl AND als auch OR verwendet werden, wird zuerst AND und dann OR ausgewertet. Sie können die Reihenfolge der Ausführung ändern, indem Sie Klammern verwenden.|  
|NICHT|Negiert jeden booleschen Ausdruck (auch Schlüsselwörter wie LIKE, NULL, BETWEEN, IN und EXISTS).<br /><br />Wenn mehrere logische Operatoren in einer Anweisung verwendet werden, wird NOT zuerst verarbeitet. Sie können die Reihenfolge der Ausführung ändern, indem Sie Klammern verwenden.|  
  
## Siehe auch  
[UNIQUE- und CHECK-Einschränkungen](assetId:///637098af-2567-48f8-90f4-b41df059833e)  
[Erstellen von Unique-Einschränkungen](assetId:///a86f9d6f-f242-43be-b65d-b3435b71b62a)  
  
