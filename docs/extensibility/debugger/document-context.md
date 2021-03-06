---
title: Contexto de documento | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], contexts
ms.assetid: 8e8b5702-5c16-4988-953d-69dd807d8b84
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0ad3996877ee3ba0f16972fbd5cf10cb539ac975
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "54993811"
---
# <a name="document-context"></a>Contexto de documento
En [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] depuración, un *contexto de documento*:  
  
-   Representa una posición en un archivo de origen. Para los idiomas donde el archivo de origen no puede estar presente, un contexto de documento identifica una posición en un documento normalmente generado por el entorno de tiempo de ejecución. Por ejemplo, un motor de scripting podría generar un documento de script. Para obtener más información, consulte [documentar posición](../../extensibility/debugger/document-position.md).  
  
-   Describe una posición en un documento de origen que corresponde a un contexto de código. El controlador de símbolos asigna un contexto de código al contexto de la documentación, con información generada por un compilador o intérprete.  
  
-   Se implementa mediante un [IDebugDocumentContext2](../../extensibility/debugger/reference/idebugdocumentcontext2.md) interfaz.  
  
## <a name="see-also"></a>Vea también  
 [Contexto de código](../../extensibility/debugger/code-context.md)   
 [Proveedor de símbolos](../../extensibility/debugger/symbol-provider.md)   
 [Interfaces de proveedor de símbolos](../../extensibility/debugger/reference/symbol-provider-interfaces.md)   
 [Contextos de depurador](../../extensibility/debugger/debugger-contexts.md)