---
title: SYMBOL_SEARCH_INFO_FIELDS | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- SYMBOL_SEARCH_INFO_FIELDS
helpviewer_keywords:
- SYMBOL_SEARCH_INFO_FIELDS enumeration
ms.assetid: bce35af0-722d-46d4-afa6-eaae598c51ff
caps.latest.revision: 10
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: be424e10484984ae9b7b84c39897001680729b69
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47577808"
---
# <a name="symbolsearchinfofields"></a>SYMBOL_SEARCH_INFO_FIELDS
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [SYMBOL_SEARCH_INFO_FIELDS](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/symbol-search-info-fields).  
  
Especifica el tipo de información de símbolos para recuperar.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp#  
enum enum_SYMBOL_SEARCH_INFO_FIELDS  
{  
   SSIF_NONE                = 0x00000000,  
   SSIF_VERBOSE_SEARCH_INFO = 0x00000001  
};  
typedef DWORD SYMBOL_SEARCH_INFO_FIELDS;  
```  
  
```csharp  
public enum enum_SYMBOL_SEARCH_INFO_FIELDS  
{  
   SSIF_NONE                = 0x00000000,  
   SSIF_VERBOSE_SEARCH_INFO = 0x00000001  
};  
  
```  
  
## <a name="members"></a>Miembros  
 SSIF_NONE  
 No indica ninguna marca  
  
 SSIF_VERBOSE_SEARCH_INFO  
 Devuelve que todas las rutas de acceso para buscar los símbolos de búsqueda  
  
## <a name="remarks"></a>Comentarios  
 Estas marcas se pasan como un parámetro a la [GetSymbolInfo](../../../extensibility/debugger/reference/idebugmodule3-getsymbolinfo.md) devuelto del método para determinar la cantidad de información.  
  
> [!NOTE]
>  Actualmente, solo `SSIF_VERBOSE_SEARCH_INFO` se admite, y se debe especificar como el `dwFlags` parámetro `IDebugModule3::GetSymbolInfo`. Todos los demás valores devuelven un error.  
  
## <a name="requirements"></a>Requisitos  
 Encabezado: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Ensamblado: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Vea también  
 [Enumeraciones](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [GetSymbolInfo](../../../extensibility/debugger/reference/idebugmodule3-getsymbolinfo.md)
