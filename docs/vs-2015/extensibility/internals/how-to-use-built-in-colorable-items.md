---
title: 'Cómo: usar elementos coloreables integrados | Microsoft Docs'
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
- colorable items
- language services, built-in colorable items
ms.assetid: 5e5f3436-6bad-4fd2-8823-6a30353ba648
caps.latest.revision: 18
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 20ed9b5424363eceec8cf4c3c5275a3a937a7003
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47566854"
---
# <a name="how-to-use-built-in-colorable-items"></a>Cómo: usar elementos coloreables integrados
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [Cómo: uso de elementos coloreables integrados](https://docs.microsoft.com/visualstudio/extensibility/internals/how-to-use-built-in-colorable-items).  
  
Antes de usar los elementos coloreables integrados, debe en primer lugar señalar al entorno de desarrollo integrado (IDE) que no proporcionan sus propios elementos coloreables personalizados, que en este caso sería <xref:Microsoft.VisualStudio.TextManager.Interop.IVsProvideColorableItems> objetos. Para ello, establezca una entrada del registro del servicio de lenguaje.  
  
### <a name="to-use-built-in-colorable-items"></a>Para usar elementos coloreables integrados  
  
1.  En HKEY_LOCAL_MACHINE\VisualStudio\\*X.Y*\Languages\Language servicios\\*Nombreidioma*, donde *X.Y* es una versión de [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] y *Nombreidioma* es el nombre de su lenguaje, cree un valor de entrada del Registro DWORD llamado `RequestStockColors`.  
  
2.  Establecer el `RequestStockColors` valor de la entrada del registro en 1.  
  
     Después de crear la entrada del registro, el Coloreador <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer.ColorizeLine%2A> método puede utilizar los miembros de la <xref:Microsoft.VisualStudio.TextManager.Interop.DEFAULTITEMS> enumeración para rellenar la matriz de atributos de color para su uso por el editor.  
  
    > [!NOTE]
    >  No establezca esta entrada del registro si va a proporcionar elementos coloreables personalizados. Para obtener más información, consulte [elementos coloreables personalizados](../../extensibility/internals/custom-colorable-items.md).  
  
## <a name="see-also"></a>Vea también  
 [Colores de sintaxis en editores personalizados](../../extensibility/syntax-coloring-in-custom-editors.md)   
 [Colores de sintaxis en un servicio de lenguaje heredado](../../extensibility/internals/syntax-coloring-in-a-legacy-language-service.md)   
 [Implementación de colores de sintaxis](../../extensibility/internals/implementing-syntax-coloring.md)   
 [Elementos coloreables personalizados](../../extensibility/internals/custom-colorable-items.md)   
 [Registro de un servicio de lenguaje heredado](../../extensibility/internals/registering-a-legacy-language-service2.md)
