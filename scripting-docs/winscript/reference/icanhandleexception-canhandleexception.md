---
title: ICanHandleException::CanHandleException | Documentos de Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- ICanHandleException.CanHandleException
apilocation:
- scrobj.dll
helpviewer_keywords:
- ICanHandleException::CanHandleException
ms.assetid: 0fc703bf-9518-487e-af20-00e073b640f1
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 784463f9e465aac005f5454be28a0043069dcb69
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2019
ms.locfileid: "54090004"
---
# <a name="icanhandleexceptioncanhandleexception"></a>ICanHandleException::CanHandleException
Determina si el autor de llamada del motor de secuencia de comandos puede controlar una excepción especificada.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp
HRESULT CanHandleException(  
   EXCEPINFO*  pExcepInfo,  
   VARIANT*    pvar  
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 `pExcepInfo`  
 [in] Puntero a un `EXCEPINFO` estructura que contiene la información que se notificará si no se encuentra ningún controlador de excepciones.  
  
 `pvar`  
 [in] Un valor asociado con la excepción, como el valor producida por un `throw` instrucción. Este parámetro puede ser `NULL`.  
  
## <a name="return-value"></a>Valor devuelto  
 El método devuelve un objeto `HRESULT`. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.  
  
|Valor|Descripción|  
|-----------|-----------------|  
|`S_OK`|El llamador puede controlar la excepción|  
|`E_FAIL`|El llamador no puede controlar la excepción.|  
  
## <a name="remarks"></a>Comentarios  
 Si una llamada a `IDispatchEx::InvokeEx`, o un método similar, da como resultado una excepción, el motor de secuencia de comandos comprueba para un llamador de cadena de autor de llamada de la secuencia de comandos que admite el `ICanHandleException` interfaz e indica que puede controlar la excepción. Si ningún llamador pueda controlar la excepción, se detiene el motor de scripts.  
  
## <a name="see-also"></a>Vea también  
 [ICanHandleException (interfaz)](../../winscript/reference/icanhandleexception-interface.md)   
 [IDispatchEx::InvokeEx](../../winscript/reference/idispatchex-invokeex.md)