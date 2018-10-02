---
title: Descripción de los valores de datos de contención de recursos | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- concurrency profiling method
- Profiling Tools, concurrency method
ms.assetid: 071c0f0f-1eba-4dc8-ae87-0810e4086dd0
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 10c06805db7ef817421f7c9f85e316af8d4b5b35
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47576173"
---
# <a name="understanding-resource-contention-data-values"></a>Descripción de los valores de datos de contención de recursos
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [valores de datos de contención de recursos de descripción](https://docs.microsoft.com/visualstudio/profiling/understanding-resource-contention-data-values).  
  
La generación de perfiles de contención de recursos recopila información detallada de la pila de llamadas cada vez que subprocesos competidores en una aplicación se ven obligados a esperar para obtener acceso a un recurso compartido.  
  
 **Requisitos**  
  
-   [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)], [!INCLUDE[vsPro](../includes/vspro-md.md)]  
  
 Los informes de contención de recursos muestran el número total de contenciones y el tiempo total invertido esperando a un recurso por los módulos, funciones, líneas del código fuente e instrucciones en los que se produjo la espera.  
  
-   Los valores inclusivos muestran el número total de contenciones que obligan a una función a esperar por las contenciones de recursos y el tiempo total de espera de la función.  Las contenciones originadas por funciones secundarias llamadas por la función se incluyen en los valores inclusivos.  
  
-   Los valores exclusivos muestran solo el número de contenciones que obligan a una función a esperar y que están causadas por el código en el cuerpo de la función. No se incluyen las contenciones producidas por funciones secundarias. El tiempo exclusivo de la función también incluye los tiempos de espera producidos por instrucciones del cuerpo de la función.  
  
 Las vistas de informes de contención de recursos también incluyen gráficos de escala de tiempo que se muestran los eventos de contención individuales a lo largo del tiempo y muestran las pilas de llamadas que crearon el evento concreto. Para obtener más información, consulte uno de los temas siguientes:  
  
-   [Vista Detalles del subproceso](../profiling/thread-details-view-contention-data.md)  
  
-   [Vista Detalles de recursos](../profiling/resource-details-view-contention-data.md)  
  
 Para obtener más información sobre el segundo modo de generación de perfiles de simultaneidad, consulte [visualizador de simultaneidad](../profiling/concurrency-visualizer.md).


