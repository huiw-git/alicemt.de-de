---
title: "Versionsanmerkungen"
ms.custom: na
ms.date: 06/09/2016
ms.prod: sql-non-specified
ms.reviewer: na
ms.suite: na
ms.technology: 
  - drivers
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 905b595b-9aac-4e6a-8ed1-3a5ed96077d8
caps.latest.revision: 6
caps.handback.revision: 5
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
# Versionsanmerkungen
Versionsanmerkungen für Microsoft ODBC Driver for SQL Server on Linux  
  
## Neuigkeiten bei [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] ODBC Driver 13 \(Preview\) for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] on Linux  
Mit dem Microsoft ODBC Driver 13 \(Preview\) für SQL Server werden jetzt auch SQL Server 2014 und SQL Server 2016 \(Preview\) unterstützt.  
  
**Always Encrypted**  
  
Unterstützung für das kürzlich vorgestellte Always Encrypted\-Feature in SQL Server 2016 \(Vorschau\), ein neues Sicherheitsfeature, das sicherstellt, dass sensible Daten in einer SQL Server\-Instanz zu keiner Zeit im Klartext sichtbar sind. Always Encrypted arbeitet mit transparenter Verschlüsselung der Daten in der Anwendung, sodass SQL Server nur die verschlüsselten Daten verarbeitet, aber keine Klartextwerte. Selbst, wenn die Integrität der SQL\-Instanz oder des Hostcomputers beschädigt ist, kann ein Angreifer sensible Daten nur als chiffrierten Text sehen. Einzelheiten finden Sie unter [Verwenden von „Immer verschlüsselt“ mit dem ODBC-Treiber für Linux](../content/Using-Always-Encrypted-with-the-Linux-ODBC-Driver.md).  
  
**Ubuntu\-Support**  
  
Ubuntu wird jetzt zusammen mit Red Hat und SUSE unterstützt. Sie können die Version für Ubuntu hier downloaden: [Microsoft ODBC Driver 13 \(Preview\) for SQL Server \- Ubuntu Linux](http://go.microsoft.com/fwlink/?LinkId=??).  
  
**unixODBC 2.3.1\-Treiber\-Manager\-Unterstützung**  
  
Informationen zur Unterstützung des Treiber\-Managers finden Sie unter [Installieren des Treiber-Managers](../content/Installing-the-Driver-Manager.md).  
  
## Neuigkeiten bei [!INCLUDE[msCoName](../content/includes/msCoName_md.md)] ODBC Driver 11 for [!INCLUDE[ssNoVersion](../content/includes/ssNoVersion_md.md)] on Linux  
Der ODBC\-Treiber unter SUSE Linux \(Preview\) unterstützt das 64\-Bit\-SUSE Linux Enterprise 11 Service Pack 2. Weitere Informationen finden Sie unter [Systemanforderungen](../content/System-Requirements.md).  
  
Der ODBC\-Treiber unter Linux unterstützt [!INCLUDE[ssHADR](../content/includes/ssHADR_md.md)]. Weitere Informationen finden Sie unter [ODBC-Treiber mit der Linux-Unterstützung für hohe Verfügbarkeit, Notfallwiederherstellung](../content/ODBC-Driver-on-Linux-Support-for-High-Availability--Disaster-Recovery.md).  
  
Der ODBC\-Treiber unter Linux unterstützt Verbindungen mit Microsoft Azure SQL\-Datenbanken. Weitere Informationen finden Sie unter [Gewusst wie: Verbinden mit Microsoft Azure SQL\-Datenbank mithilfe von ODBC](http://msdn.microsoft.com/library/hh974312.aspx).  
  
Der Treiber unterstützt die Ein\- und Ausgangs\-Ablaufverfolgung von ODBC\-API\-Aufrufen. Weitere Informationen finden Sie unter [Datenzugriffs-Ablaufverfolgung mit dem ODBC-Treiber unter Linux](../content/Data-Access-Tracing-with-the-ODBC-Driver-on-Linux.md).  
  
Die Option „**\-l**“ wurde bcp hinzugefügt. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit bcp](../content/Connecting-with-bcp.md).  
  
