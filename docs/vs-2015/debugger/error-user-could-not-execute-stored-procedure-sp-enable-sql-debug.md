---
title: 'Error: Usuario podría no ejecutar el procedimiento almacenado sp_enable_sql_debug | Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.debug.error.sqlde_accessdenied
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: 11957495-c238-4cc5-8937-e4026f5e10e1
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 172b7b7870e3bf35b2cda5fc04a894b6c52c70d4
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47576581"
---
# <a name="error-user-could-not-execute-stored-procedure-spenablesqldebug"></a>Error: El usuario no pudo ejecutar el procedimiento almacenado sp_enable_sql_debug
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [Error: usuario podría no ejecutar el procedimiento almacenado sp_enable_sql_debug](https://docs.microsoft.com/visualstudio/debugger/error-user-could-not-execute-stored-procedure-sp-enable-sql-debug).  
  
El procedimiento almacenado sp_enable_sql_debug no se pudo ejecutar en el servidor. Esto se puede producir por:  
  
-   Un problema de conexión. Necesita tener una conexión estable al servidor.  
  
-   Faltan permisos necesarios en el servidor. Para depurar en SQL Server 2005, la cuenta que ejecuta Visual Studio y la cuenta empleada para conectar a SQL Server tienen que ser miembros del rol sysadmin. La cuenta empleada para conectar a SQL Server es la cuenta de usuario de Windows (si se utiliza la Autenticación de Windows) o una cuenta con id. de usuario y contraseña (si se utiliza la Autenticación SQL).  
  
 Para obtener más información, consulte [Cómo: establecer permisos de SQL Server para la depuración](http://msdn.microsoft.com/en-us/84e088d0-0409-41d4-841b-f5d4b0fda414).  
  
## <a name="see-also"></a>Vea también  
 [Cómo: establecer permisos de SQL Server para la depuración](http://msdn.microsoft.com/en-us/84e088d0-0409-41d4-841b-f5d4b0fda414)   
 [Configurar la depuración de SQL](http://msdn.microsoft.com/en-us/3db09e68-edcc-42de-9c22-4e97cfd55ab3)


