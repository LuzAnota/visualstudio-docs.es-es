---
title: IDiaAddressMap::put_addressMapEnabled | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaAddressMap::put_addressMapEnabled method
ms.assetid: 0f205337-4e59-4383-8059-7b1d207d6dcd
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a53d66879155ae1ce2cd831c029bc5776a7dd863
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "54999215"
---
# <a name="idiaaddressmapputaddressmapenabled"></a>IDiaAddressMap::put_addressMapEnabled
Especifica si se debe usar la asignación de dirección para traducir las direcciones de símbolos.  
  
## <a name="syntax"></a>Sintaxis  
  
```C++  
HRESULT put_addressMapEnabled (   
   BOOL NewVal  
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 NewVal  
 [in] Establecido en `TRUE` para habilitar la traducción de símbolos, o `FALSE` a deshabilitar.  
  
## <a name="return-value"></a>Valor devuelto  
 Si es correcto, devuelve `S_OK`; en caso contrario, devuelve un código de error.  
  
## <a name="remarks"></a>Comentarios  
 Ejecutable procesadores posterior a la actualización a veces el archivo ejecutable. DIA contiene un mecanismo para admitir la traducción de símbolos para el nuevo diseño.  
  
 Cuando se carga un archivo PDB, se habilita la asignación de dirección almacenada en el archivo. Veces, sin embargo, cuando una aplicación cliente que necesite proporcionar su propio mapa de direcciones mediante una llamada a la [Set_addressmap](../../debugger/debug-interface-access/idiaaddressmap-set-addressmap.md) método. Si el `set_addressMap` método se realiza correctamente, la aplicación cliente debe llamar a la `put_addressMapEnabled` método con un `NewVal` parámetro de `TRUE` para habilitar el uso de esa asignación de dirección.  
  
 Se puede recuperar el estado actual de la asignación de dirección está habilitada con una llamada a la [Get_addressmapenabled](../../debugger/debug-interface-access/idiaaddressmap-get-addressmapenabled.md) método.  
  
## <a name="see-also"></a>Vea también  
 [IDiaAddressMap](../../debugger/debug-interface-access/idiaaddressmap.md)   
 [IDiaAddressMap::set_addressMap](../../debugger/debug-interface-access/idiaaddressmap-set-addressmap.md)   
 [IDiaAddressMap::get_addressMapEnabled](../../debugger/debug-interface-access/idiaaddressmap-get-addressmapenabled.md)