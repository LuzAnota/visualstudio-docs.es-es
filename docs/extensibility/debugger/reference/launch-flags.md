---
title: LAUNCH_FLAGS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- LAUNCH_FLAGS
helpviewer_keywords:
- LAUNCH_FLAGS enumeration
ms.assetid: f51aab02-d257-4302-bb79-b7d8ba9ac4e5
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d793adfd8be2fb86f51e94cfd43e8dbcbd75036f
ms.sourcegitcommit: 845442e2b515c3ca1e4e47b46cc1cef4df4f08d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2019
ms.locfileid: "56450001"
---
# <a name="launchflags"></a>LAUNCH_FLAGS
Especifica las marcas de inicio de depuración.

## <a name="syntax"></a>Sintaxis

```cpp
enum enum_LAUNCH_FLAGS {
    LAUNCH_DEBUG      = 0x0000,
    LAUNCH_NODEBUG    = 0x0001,
    LAUNCH_ENABLE_ENC = 0x0002,
    LAUNCH_MERGE_ENV  = 0x0004
};
typedef DWORD LAUNCH_FLAGS;
```

```csharp
public enum enum_LAUNCH_FLAGS {
    LAUNCH_DEBUG      = 0x0000,
    LAUNCH_NODEBUG    = 0x0001,
    LAUNCH_ENABLE_ENC = 0x0002,
    LAUNCH_MERGE_ENV  = 0x0004
};
```

## <a name="members"></a>Miembros
LAUNCH_DEBUG  
Inicia el proceso de depuración.

LAUNCH_NODEBUG  
Inicia el proceso sin depurarlo.

LAUNCH_ENABLE_ENC  
EN DESUSO, NO USE.

LAUNCH_MERGE_ENV  
Inicia el proceso y combina el entorno con el host al iniciar.

## <a name="remarks"></a>Comentarios
Estos valores se pasan como argumento a la [LaunchSuspended](../../../extensibility/debugger/reference/idebugenginelaunch2-launchsuspended.md) método.

Estas marcas se pueden combinar con un bit a bit `OR`.

## <a name="requirements"></a>Requisitos
Encabezado: msdbg.h

Espacio de nombres:  Microsoft.VisualStudio.Debugger.Interop

Ensamblado: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Vea también
[Enumeraciones](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)  
[LaunchSuspended](../../../extensibility/debugger/reference/idebugenginelaunch2-launchsuspended.md)
