---
title: 'Vista Módulos: datos de muestreo | Microsoft Docs'
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
- Modules view
- sampling profiling method,Modules view
ms.assetid: 816f5633-65d7-41e5-aee1-033628d4e2df
caps.latest.revision: 18
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ec3349922acb6a9fb5a08bd11675454e9f8cbad3
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47577790"
---
# <a name="modules-view---sampling-data"></a>Vista Módulos: datos de muestreo
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [vista módulos: datos de muestreo](https://docs.microsoft.com/visualstudio/profiling/modules-view-sampling-data).  
  
La vista Módulos de datos de muestro muestra datos de rendimiento agrupados por los módulos de los que se toman muestras en los datos de generación de perfiles. Cada módulo es la raíz de un árbol jerárquico. Las funciones del módulo de las que se toman muestras se enumeran bajo el nodo de módulo.  
  
> [!NOTE]
>  Las características de seguridad mejoradas en Windows 8 y Windows Server 2012 requirieron cambios significativos en la forma en que el generador de perfiles de Visual Studio recopila datos en estas plataformas. Las aplicaciones de la Tienda Windows también requieren nuevas técnicas de recolección. Consulte [Herramientas de rendimiento en aplicaciones de Windows 8 y Windows Server 2012](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md).  
  
 Si la función se estaba ejecutando cuando se recopilaron las muestras (es decir, si la función estaba en la parte superior de la pila de llamadas), las líneas de código fuente y las direcciones de instrucción que se estaban ejecutando aparecen debajo del nodo de función. Dado que cuando se ejecuta la línea o la instrucción, se recopilan datos de una línea de código fuente o un puntero de instrucción, los valores inclusivos y exclusivos siempre son los mismos para los datos de línea y de instrucción.  
  
|Columna|Descripción|  
|------------|-----------------|  
|**Name**|El nombre del módulo, función, número de línea o dirección del puntero de instrucción.|  
|**Identificador del proceso**|Identificador de proceso (PID) de la ejecución de generación de perfiles.|  
|**Nombre de proceso**|Nombre del proceso.|  
|**Nombre del módulo**|Nombre del módulo que contiene la función, línea o dirección del puntero de instrucción.|  
|**Ruta de acceso del módulo**|La ruta de acceso del módulo que contiene el módulo, función, línea o dirección del puntero de instrucción.|  
|**Archivo de código fuente**|Archivo de origen que contiene la definición de esta función.|  
|**Número de línea de la función**|Número de línea del inicio de esta función en el archivo de origen.|  
|**Muestras inclusivas**|-   Para una función, el número de muestras en las que se estaba ejecutando esta función u otra función a la que llamó esta función, es decir, el número de muestras de la pila de llamadas que contienen esta función.<br />-   Para un módulo, el número de muestras en las que al menos una función del módulo se estaba ejecutando.<br />-   Para una línea o instrucción, el número de muestras en las que se estaba ejecutando esta línea o instrucción.|  
|**Porcentaje de muestras inclusivas**|-   Para una función o un módulo, el porcentaje de todas las muestras de la generación de perfiles que fueron muestras inclusivas de esta función o módulo.<br />-   Para una línea o instrucción, el porcentaje de todas las muestras de la generación de perfiles en las que se estaba ejecutando esta línea o instrucción.|  
|**Muestras exclusivas**|-   Para una función, el número de muestras de la pila de llamadas en las que se estaba ejecutando directamente esta función, es decir, el número de muestras en las que esta función estaba en la parte superior de la pila de llamadas.<br />-   Para un módulo, la suma de muestras exclusivas de las funciones del módulo.<br />-   Para una línea o instrucción, el número de muestras en las que se estaba ejecutando esta línea o instrucción.|  
|**Porcentaje de muestras exclusivas**|-   Para una función o un módulo, el porcentaje de todas las muestras de la generación de perfiles que fueron muestras exclusivas de esta función o módulo.<br />-   Para una línea o instrucción, el porcentaje de todas las muestras de la generación de perfiles en las que se estaba ejecutando esta línea o instrucción.|  
  
## <a name="see-also"></a>Vea también  
 [Vista Módulos: muestreo](../profiling/modules-view-dotnet-memory-sampling-data.md)   
 [Vista Módulos: instrumentación](../profiling/modules-view-dotnet-memory-instrumentation-data.md)   
 [Vista Módulos](../profiling/modules-view-instrumentation-data.md)


