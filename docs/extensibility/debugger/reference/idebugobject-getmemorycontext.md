---
title: IDebugObject::GetMemoryContext | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugObject::GetMemoryContext
helpviewer_keywords:
- IDebugObject::GetMemoryContext method
ms.assetid: 6760a0d3-a898-4e81-b68f-c45c584b225b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9fe479c93cadeb6826ee4e4d3ba41ff973cb11c9
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "55027742"
---
# <a name="idebugobjectgetmemorycontext"></a>IDebugObject::GetMemoryContext
Obtiene el contexto de la memoria que representa la dirección del valor del objeto.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp  
HRESULT GetMemoryContext(   
   IDebugMemoryContext2** pContext  
);  
```  
  
```csharp  
int GetMemoryContext(  
   ref IDebugMemoryContext2 pContext  
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 `pContext`  
 [out] Devuelve un [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md) objeto que representa la dirección del valor del objeto.  
  
## <a name="return-value"></a>Valor devuelto  
 Si se realiza correctamente, devuelve S_OK; en caso contrario, devuelve un código de error.  
  
## <a name="remarks"></a>Comentarios  
 El contexto de la memoria devuelta especifica la dirección del valor tal como está representada por este [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) objeto.  
  
## <a name="see-also"></a>Vea también  
 [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md)