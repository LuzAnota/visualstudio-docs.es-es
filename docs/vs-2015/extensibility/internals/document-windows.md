---
title: Documentos de Windows | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Visual Studio SDK, document windows
ms.assetid: 50081d48-987f-43db-8bf9-51b7cf76e9c0
caps.latest.revision: 18
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: c620de56e3658c3aef33da136930221578b9be4a
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47574683"
---
# <a name="document-windows"></a>Ventanas de documento
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [documento Windows](https://docs.microsoft.com/visualstudio/extensibility/internals/document-windows).  
  
En Visual Studio, un *ventana de documento* es una ventana secundaria de tramas que está asociada a una ventana de interfaz de múltiples documentos (MDI). Normalmente se usan las ventanas de documento para la visualización y modificación de código fuente o el texto, pero también pueden hospedar otros tipos funcionales. Ventanas de documento:  
  
-   Se pueden organizar en grupos de pestañas independientes de horizontal o vertical en el elemento primario MDI para que se pueden ver varios archivos al mismo tiempo.  
  
-   Se pueden acoplar en cualquier orden en el elemento primario MDI.  
  
-   Puede flotar libremente.  
  
-   Se vinculan en orden de tabulación en otras ventanas MDI.  
  
 Comandos para la agrupación, acopladas y flotantes pueden encontrarse en el menú contextual de una pestaña de ventana de documento.  
  
 Para obtener más información sobre el comportamiento de las ventanas en Visual Studio, consulte [personalizar los diseños de ventana](../../ide/customizing-window-layouts-in-visual-studio.md).  
  
## <a name="document-window-implementation"></a>Implementación de la ventana de documento  
 Ventanas de documento se crean mediante la implementación de un editor. El <xref:Microsoft.VisualStudio.Shell.Interop.IVsEditorFactory> interfaz crea ventanas de documento como parte de la creación de instancias de un editor. Para obtener más información, consulte [Interfaces heredadas en el Editor de](../../extensibility/legacy-interfaces-in-the-editor.md).  
  
> [!NOTE]
>  Para proporcionar hacia atrás y reenviar los puntos de navegación en una ventana, implemente el <xref:Microsoft.VisualStudio.Shell.Interop.IVsBackForwardNavigation> interfaz. El editor de texto usa marcadores de texto para identificar puntos de navegación en el documento.  
  
## <a name="the-running-document-table"></a>La tabla de documentos en ejecución  
 El IDE usa la tabla de documentos en ejecución (RDT) para un seguimiento del estado de cada ventana de documento. La RDT es el mecanismo a través de qué documento son una notificación de eventos, como cuando se cierra una solución o cuando se ha editado un archivo de windows. Para obtener más información, consulte [tabla de documentos en ejecución](../../extensibility/internals/running-document-table.md).  
  
## <a name="see-also"></a>Vea también  
 [Carga de documentos retrasada](../../extensibility/internals/delayed-document-loading.md)
