---
title: "La variable temporal en línea - refactorización (Visual Basic) | Documentos de Microsoft"
ms.custom: 
ms.date: 11/17/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: a63d6407-5acb-4d5f-8c0e-ecedddc07177
author: gewarren
ms.author: gewarren
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: 3607e646f5f1ccc6121e5ee8a5b71772008f1ce8
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/22/2017
---
# <a name="inline-a-temporary-variable-in-visual-basic"></a>En línea una variable temporal en Visual Basic
**¿Qué:** le permite quitar el uso de una variable temporal y reemplácelo por el código real en su lugar.

**Cuándo:** el uso de la variable temporal hace que el código sea más difícil de entender.  

**Por este motivo:** quita una variable temporal puede hacer que el código más fácil de leer en ciertas situaciones

**Cómo:**

1. Resalte o coloque el cursor de texto dentro de la variable temporal se inserte:

   ![Código que aparece resaltado](media/inline_highlight.png)

1. A continuación, realice una de las siguientes acciones:
   * **Teclado**
     * Presione **Ctrl +.** Para activar el **acciones rápidas y refactorizaciones** menú y seleccione **variable temporal en línea** desde la ventana emergente de ventana de vista previa.
   * **Mouse**
     * Haga clic en el código, seleccione la **acciones rápidas y refactorizaciones** menú y seleccione **variable temporal en línea** desde la ventana emergente de ventana de vista previa.

   La variable que se va a quitar y sus usos se sustituye por el valor de la variable de forma inmediata.

   ![Resultados inline](media/inline_result.png)

## <a name="see-also"></a>Vea también
[Refactorización (Visual Basic)](../refactoring-vb.md)