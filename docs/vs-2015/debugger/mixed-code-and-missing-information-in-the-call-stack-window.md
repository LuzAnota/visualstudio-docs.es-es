---
title: Código mixto e información que falta en la ventana Pila de llamadas | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- FSharp
- VB
- CSharp
- C++
- JScript
- SQL
- VB
- CSharp
- C++
helpviewer_keywords:
- managed code, stepping
- Call Stack window, mixed-mode debugging
- Call Stack window, troubleshooting
- native frames
- managed call stacks
- mixed-mode debugging, call stack
- stepping, out of managed code
ms.assetid: dd628427-e8d6-4fc2-b524-9d6393ea5376
caps.latest.revision: 23
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c91b2e49dc94057ab7929380ad1b819cd01731d6
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47577080"
---
# <a name="mixed-code-and-missing-information-in-the-call-stack-window"></a>Código mixto e información no mostrada en la ventana Pila de llamadas
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [código mixto e información no mostrada en la ventana Pila de llamadas](https://docs.microsoft.com/visualstudio/debugger/mixed-code-and-missing-information-in-the-call-stack-window).  
  
Debido a las diferencias entre las pilas de llamadas para código administrado y código nativo, el depurador no siempre puede mostrar toda la pila de llamadas cuando se mezclan los tipos de código. Cuando código nativo llama a código administrado, es posible que tenga en cuenta las siguientes discrepancias en los **pila de llamadas** ventana:  
  
-   El marco nativo inmediatamente encima del código administrado pueden faltar desde el **pila de llamadas** ventana. Para obtener más información, consulte [Cómo: salir de código administrado cuando los marcos nativos no aparecen en la ventana Pila de llamadas](../debugger/how-to-step-out-of-managed-code-when-native-frames-are-missing-from-the-call-stack-window.md).  
  
-   Para las aplicaciones de modo mixto iniciadas fuera del depurador, el **pila de llamadas** ventana puede mostrar sólo el código administrado y ninguno de los marcos nativos será visible.  
  
 Ninguno de estos casos es habitual. En la mayoría de las llamadas nativas a código administrado, las pilas de llamadas se muestran correctamente.  
  
## <a name="see-also"></a>Vea también  
 [Cómo: Usar la ventana Pila de llamadas](../debugger/how-to-use-the-call-stack-window.md)




