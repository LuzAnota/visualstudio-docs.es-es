---
title: 'Cómo: usar la administración de la fase de reversión vinculado | Microsoft Docs'
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
- editors [Visual Studio SDK], legacy - linked undo management
ms.assetid: af5cc22a-c9cf-45b1-a894-1022d563f3ca
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 2e64d65376a85b9cbc9af525117e017c56f7b851
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47581880"
---
# <a name="how-to-use-linked-undo-management"></a>Cómo: usar la administración de la fase de reversión vinculado
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [Cómo: usar Administración de deshacer vinculada](https://docs.microsoft.com/visualstudio/extensibility/how-to-use-linked-undo-management).  
  
Fase de reversión vinculado permite al usuario simultáneamente deshacer las modificaciones mismas en varios archivos. Por ejemplo, los cambios de texto simultánea en varios archivos de programa, como un archivo de encabezado y un archivo de Visual C++, es una transacción vinculada de deshacer. Capacidad de deshacer vinculada está integrada en la implementación del entorno de que el Administrador de deshacer y <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLinkedUndoTransactionManager> permite manipular esta capacidad. Acción de deshacer vinculada se implementa mediante una unidad de deshacer primaria que se puede vincular las pilas de deshacer independiente juntos a tratarse como una unidad de deshacer única. El procedimiento para utilizar vinculada de deshacer se detalla en la sección siguiente.  
  
### <a name="to-use-linked-undo"></a>Para usar la acción de deshacer vinculada  
  
1.  Llame a `QueryService` en `SVsLinkedUndoManager` para obtener un puntero a `IVsLinkedUndoTransactionManager`.  
  
2.  Crear la unidad de deshacer vinculada principal inicial mediante una llamada a <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLinkedUndoTransactionManager.OpenLinkedUndo%2A>. Esto establece el punto de partida para un conjunto de las pilas de deshacer se agrupan en las pilas de deshacer vinculada. En el `OpenLinkedUndo` método también deberá especificar si desea que la operación de deshacer vinculada ser estricta o no es estricta. Comportamiento de deshacer vinculada no estricta significa que algunos de los documentos con la fase de reversión vinculado del mismo nivel pueden cerrar y dejar el otro vinculado elementos del mismo nivel en sus pilas de deshacer. Comportamiento de deshacer vinculada estricta especifica que todas las pilas de deshacer vinculada del mismo nivel que se deshagan conjuntamente o no. Agregar posteriores vinculado pilas de deshacer llamando [IOleUndoManager::Add](http://msdn.microsoft.com/library/windows/desktop/ms680135) método.  
  
3.  Llame a <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLinkedUndoTransactionManager.CloseLinkedUndo%2A> para implementar todas las unidades de deshacer vinculada como uno.  
  
    > [!NOTE]
    >  Para implementar la administración de la fase de reversión vinculado en un editor, agregue administración de deshacer. Para obtener más información sobre la implementación de administración de la fase de reversión vinculado, vea [Cómo: implementar la administración de deshacer](../extensibility/how-to-implement-undo-management.md).  
  
## <a name="see-also"></a>Vea también  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCompoundAction>   
 [IOleParentUndoUnit](http://msdn.microsoft.com/library/windows/desktop/ms682151)   
 [IOleUndoUnit](http://msdn.microsoft.com/library/windows/desktop/ms678476)   
 [Cómo: Implementar la administración de la fase de reversión](../extensibility/how-to-implement-undo-management.md)
