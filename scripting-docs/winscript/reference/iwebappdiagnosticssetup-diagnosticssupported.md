---
title: IWebAppDiagnosticsSetup::DiagnosticsSupported | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IWebAppDiagnosticsSetup::DiagnosticsSupported
ms.assetid: 5bbcd0d0-1460-4cf7-bbb1-f4f4a04f739a
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: df9296ac251d93105229fc0af365f6797a413f2b
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/16/2019
ms.locfileid: "54349691"
---
# <a name="iwebappdiagnosticssetupdiagnosticssupported"></a>IWebAppDiagnosticsSetup::DiagnosticsSupported
Determina si los diagnósticos se admiten en esta aplicación. Si [SetSite](http://go.microsoft.com/fwlink/?LinkId=232439) se ha llamado en el objeto que implementa esta interfaz con un valor distinto de NULL, [DiagnosticsSupported](../../winscript/reference/iwebappdiagnosticssetup-diagnosticssupported.md) devuelve `true`. Si no, devuelve `false` y las llamadas a [IWebAppDiagnosticsSetup::CreateObjectWithSiteAtWebApp](../../winscript/reference/iwebappdiagnosticssetup-createobjectwithsiteatwebapp.md) producirá un error.  
  
> [!IMPORTANT]
>  [IWebAppDiagnosticsSetup (interfaz)](../../winscript/reference/iwebappdiagnosticssetup-interface.md) es implementada por PDM v11.0 y versiones posteriores. Se encuentra en activdbg100.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp  
HRESULT DiagnosticsSupported(        [out, retval] VARIANT_BOOL* pRetVal        );  
```  
  
#### <a name="parameters"></a>Parámetros  
 `pRetVal`  
 Si [SetSite](http://go.microsoft.com/fwlink/?LinkId=232439) se ha llamado en el objeto que implementa esta interfaz con un valor distinto de NULL, [DiagnosticsSupported](../../winscript/reference/iwebappdiagnosticssetup-diagnosticssupported.md) devuelve `true`. Si no, devuelve `false`y las llamadas a [IWebAppDiagnosticsSetup::CreateObjectWithSiteAtWebApp](../../winscript/reference/iwebappdiagnosticssetup-createobjectwithsiteatwebapp.md) producirá un error.