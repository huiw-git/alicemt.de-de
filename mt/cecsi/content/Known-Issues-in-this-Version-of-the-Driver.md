---
title: "Bekannte Probleme in dieser Version des Treibers"
ms.custom: na
ms.date: 06/09/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6a175513-f1bc-4040-b14f-774276bdb884
caps.latest.revision: 28
caps.handback.revision: 27
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
# Bekannte Probleme in dieser Version des Treibers
Dieses Thema enthält eine Liste der bekannten Probleme mit Microsoft ODBC Driver 11 for SQL Server on Linux.  
  
Weitere Probleme werden auf dem [Microsoft ODBC Driver\-Teamblog](http://blogs.msdn.com/b/sqlnativeclient/) gepostet.  
  
-   Windows und Linux können Zeichen aus dem benutzerdefinierten Bereich \(PUA\) oder EUDC\-Zeichen unterschiedlich konvertieren. Konvertierungen, die auf dem Server in [!INCLUDE[tsql](../content/includes/tsql_md.md)] ausgeführt werden, verwenden die Microsoft Konvertierungsbibliothek. Konvertierungen im Treiber verwenden die Linux Konvertierungsbibliothek. Jede dieser Bibliotheken führt möglicherweise zu unterschiedlichen Ergebnissen, wenn sie die Konvertierung ausführt. Weitere Informationen finden Sie unter [EUDC\-Zeichen und Zeichen des benutzerdefinierten Bereichs](http://msdn.microsoft.com/library/dd317802.aspx).  
  
-   Der Treiber\-Manager konvertiert nicht immer korrekt von UTF\-8 in UTF\-16. Aktuell werden Daten beschädigt, wenn 1 oder mehrere Zeichen in der Zeichenfolge kein gültiges UTF\-8 Zeichen darstellen. ASCII\-Zeichen werden korrekt zugeordnet. Der Treiber\-Manager wird versuchen, diese Konvertierung beim Aufruf der SQLCHAR\-Versionen der ODBC\-API \(zum Beispiel SQLDriverConnectA\) durchzuführen. Der Treiber\-Manager wird nicht versuchen, diese Konvertierung beim Aufruf der SQLWCHAR\-Versionen der ODBC\-API \(zum Beispiel SQLDriverConnectW\) durchzuführen.  
  
-   Der *ColumnSize*\-Parameter der **SQLBindParameter** bezieht sich auf die Anzahl der Zeichen. Wenn jedoch der SQL\-Datentyp varchar\(n\) oder char\(n\) ist und die Anwendung den Parameter als SQL\_C\_CHAR oder SQL\_C\_VARCHAR bindet und wenn der Client Code die UTF\-8 Codepage verwendet, erhalten Sie vom Treiber eventuell die Fehlermeldung „Zeichenfolgedaten rechts abgeschnitten“, selbst wenn der Wert der *ColumnSize* auf die Größe des Datentyps auf dem Server ausgerichtet ist. Dieser Fehler kann auftreten, wenn ein Zeichen in einigen Codepages, z. B. CP\-1252, eine andere Anzahl von Bytes in UTF\-8 aufweisen kann. Ein rechtes Apostrophzeichen, das in CP\-1252 als 0x92 codiert ist, ist als Sequenz 0xe2 0x80 0x99 in UTF\-8 codiert, die 3 Bytes besitzt.  
  
    Wenn Sie angeben, dass 1 für *ColumnSize* in **SQLBindParameter** für ein Zeichen festgelegt werden soll, vergleicht der Treiber *ColumnSize* mit der *Pufferlänge* in **SQLBindParameter**, bevor er die Konvertierung zwischen den verschiedenen Codepages auf dem Client und Server ausführt. Da ein *ColumnSize* von 1 kleiner ist als eine *Pufferlänge* von \(z. B.\) 3, generiert der Treiber einen Fehler. Um diesen Fehler zu vermeiden, verwenden Sie den Wert der *Pufferlänge* \(und nicht die konvertierte Länge\) in *ColumnSize*.*ColumnSize* darf für den varchar\(n\)\-Typ nicht größer sein als 8000.  
  
## Siehe auch  
[Microsoft ODBC Driver for SQL Server on Linux](../content/Microsoft-ODBC-Driver-for-SQL-Server-on-Linux.md)  
  
