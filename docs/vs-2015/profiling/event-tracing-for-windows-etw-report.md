---
title: Informe Seguimiento de eventos para Windows (ETW) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- Event tracing for Windows profiling report
- ETW profiling report
ms.assetid: 81e88162-b88a-40b6-8b85-a232c8096a47
caps.latest.revision: 17
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: ba40e16f70451a288a17c138bdfa3b2070d56122
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MTE95
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54752254"
---
# <a name="event-tracing-for-windows-etw-report"></a>Informe Seguimiento de eventos para Windows (ETW)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

El informe Seguimiento de eventos para Windows (ETW) muestra los eventos ETW registrados en una sesión de rendimiento de las Herramientas de generación de perfiles de [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. Los datos ETW se recopilan en un archivo binario (.etl).  
  
> [!NOTE]
>  No se puede mostrar informes ETW en la interfaz de [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].  
  
-   Para obtener información sobre cómo recopilar datos ETW mediante las Herramientas de generación de perfiles desde la interfaz de [!INCLUDE[vsprvs](../includes/vsprvs-md.md)], vea [Cómo: Recopilar datos de Seguimiento de eventos para Windows (ETW)](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md).  
  
-   Para obtener información sobre cómo recopilar datos ETW mediante las herramientas de la línea de comandos [VSPerfCmd](../profiling/vsperfcmd.md), vea [Eventos](../profiling/events-vsperfcmd.md).  
  
-   Genere el informe ETW mediante el comando **VSReport/Summary:ETW**. Para obtener más información, consulte [VSPerfReport](../profiling/vsperfreport.md).  
  
|Columna|Descripción|  
|------------|-----------------|  
|**Marca de tiempo**|Identifica la hora en la que se ha producido el evento.|  
|**Identificador del proceso**|Identifica el proceso que ha generado el evento.|  
|**Identificador de subproceso**|Identifica el subproceso que ha generado el evento.|  
|**Descripción**|Identifica el proveedor del evento.|  
|**Type**|Identifica el tipo de evento.|  
|**Propiedades**|Propiedades del evento. Cada evento es un par nombre-valor separado por comas e incluido entre corchetes.|
