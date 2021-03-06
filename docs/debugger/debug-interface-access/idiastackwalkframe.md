---
title: IDiaStackWalkFrame | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaStackWalkFrame interface
ms.assetid: 42d82845-d6f6-4846-9ecd-9dd169216077
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: cf14665b4a8f6f57e01d53debedbb3534fa025d1
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "55015491"
---
# <a name="idiastackwalkframe"></a>IDiaStackWalkFrame
Mantiene el contexto de la pila entre las invocaciones de la [Idiaframedata](../../debugger/debug-interface-access/idiaframedata-execute.md) método.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
IDiaStackWalkFrame : IUnknown  
```  
  
## <a name="methods-in-vtable-order"></a>Métodos en orden de Vtable  
 La tabla siguiente muestran los métodos de `IDiaStackWalkFrame`.  
  
|Método|Descripción|  
|------------|-----------------|  
|[IDiaStackWalkFrame::get_registerValue](../../debugger/debug-interface-access/idiastackwalkframe-get-registervalue.md)|Recupera el valor de un registro.|  
|[IDiaStackWalkFrame::put_registerValue](../../debugger/debug-interface-access/idiastackwalkframe-put-registervalue.md)|Establece el valor de un registro.|  
|[IDiaStackWalkFrame::readMemory](../../debugger/debug-interface-access/idiastackwalkframe-readmemory.md)|Lee de la imagen de memoria.|  
|[IDiaStackWalkFrame::searchForReturnAddress](../../debugger/debug-interface-access/idiastackwalkframe-searchforreturnaddress.md)|Busca el marco de pila especificado para la dirección de devolución de función más cercano.|  
|[IDiaStackWalkFrame::searchForReturnAddressStart](../../debugger/debug-interface-access/idiastackwalkframe-searchforreturnaddressstart.md)|Busca el marco de pila especificado para una dirección de retorno en o cerca de la dirección especificada.|  
  
## <a name="remarks"></a>Comentarios  
 Esta interfaz se usa durante la ejecución del programa para leer y escribir los registros, así como obtener acceso a memoria y buscar direcciones de devolución.  
  
## <a name="notes-for-callers"></a>Notas para los llamadores  
 La aplicación cliente implementa esta interfaz y pasa una instancia de la interfaz para el [Idiaframedata](../../debugger/debug-interface-access/idiaframedata-execute.md) método. La misma instancia de esta interfaz se usa y otra vez para mantener el estado de los registros durante cada invocación de la `execute` método. El `execute` método también usa esta interfaz para determinar la dirección de retorno.  
  
## <a name="requirements"></a>Requisitos  
 Encabezado: dia2.h  
  
 Biblioteca: diaguids.lib  
  
 DLL: msdia80.dll  
  
## <a name="see-also"></a>Vea también  
 [Interfaces (SDK de acceso a la interfaz de depuración)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)   
 [IDiaFrameData::execute](../../debugger/debug-interface-access/idiaframedata-execute.md)