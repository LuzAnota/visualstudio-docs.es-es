---
title: PDB_TYPE | Microsoft Docs
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
- PDB_TYPE
helpviewer_keywords:
- PDB_TYPE structure
ms.assetid: 1c1bb772-77d6-4870-90b2-fd9247d0004e
caps.latest.revision: 8
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 1e63fb8f32e6d28428a8b3f52196f37bdca0da81
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47577113"
---
# <a name="pdbtype"></a>PDB_TYPE
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [PDB_TYPE](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/pdb-type).  
  
Esta estructura especifica información sobre un tipo de campo realizada desde un símbolo PDB.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp#  
typedef struct _tagTYPE_PDB {  
   ULONG32 ulAppDomainID;  
   GUID    guidModule;  
   DWORD   symid;  
} PDB_TYPE;  
```  
  
```csharp  
public struct PDB_TYPE {  
   public uint ulAppDomainID;  
   public Guid guidModule;  
   public uint symid;  
};  
```  
  
#### <a name="parameters"></a>Parámetros  
 ulAppDomainID  
 Identificador de la aplicación del que procede el símbolo. Esto se utiliza para identificar de forma exclusiva una instancia de la aplicación.  
  
 guidModule  
 El GUID del módulo que contiene este campo.  
  
 symid  
 El identificador del símbolo que corresponde a este campo.  
  
## <a name="remarks"></a>Comentarios  
 Esta estructura aparece como parte de la unión en el [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md) estructura cuando la `dwKind` campo de la `TYPE_INFO` estructura está establecida en `TYPE_KIND_PDB` (un valor de la [dwTYPE_KIND](../../../extensibility/debugger/reference/dwtype-kind.md) enumeración).  
  
## <a name="requirements"></a>Requisitos  
 Encabezado: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Ensamblado: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Vea también  
 [Estructuras y uniones](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md)   
 [dwTYPE_KIND](../../../extensibility/debugger/reference/dwtype-kind.md)
