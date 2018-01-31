---
title: "Generación de un campo, una propiedad o un valor local: generación de código (C#) | Microsoft Docs"
ms.custom: 
ms.date: 11/16/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: c11888e0-31b1-44cc-9037-98d3f8b3623b
author: gewarren
ms.author: gewarren
manager: ghogen
ms.workload: dotnet
ms.openlocfilehash: 7cc27d498cbc082ad76d47d2326d1ee8fb0ebbb0
ms.sourcegitcommit: f89ed5fc2e5078213e30a6ade4604e34df48181f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/13/2018
---
# <a name="generate-a-field-property-or-local-in-c"></a>Generación de un campo, una propiedad o un valor local en C# #
**Qué:** Le permite generar inmediatamente el código para un campo, una propiedad o un valor local no declarados previamente. 

**Cuándo:** Introduce un nuevo campo, propiedad o valor local mientras escribe y desea declararlo de manera adecuada y de inmediato.  

**Por qué:** Podría declarar el campo, la propiedad o el valor local antes de usarlos; sin embargo, esta característica generará la declaración y el tipo automáticamente. 

**Cómo**:

1. Coloque el cursor en la línea donde hay un subrayado ondulado de color rojo que indica que ha utilizado un campo, una propiedad o un valor local que aún no existe.

   ![Código resaltado](media/field-highlight-cs.png)

1. A continuación, realice alguno de los siguientes procedimientos:
   * **Teclado**
     * Presione **Ctrl +.** para activar el menú **Acciones rápidas y refactorizaciones** y seleccione **Generate field/property/local** (Generar campo/propiedad/valor local) en el menú emergente de la ventana Vista previa.
   * **Mouse**
     * Haga clic con el botón derecho y seleccione el menú **Acciones rápidas y refactorizaciones** y elija **Generate field/property/local** (Generar campo/propiedad/valor local) en el menú emergente de la ventana Vista previa.
     * Mantenga el mouse sobre el subrayado ondulado de color rojo y haga clic en el botón ![de icono Bombilla](media/bulb-cs.png) que aparece.
     * Haga clic en el botón ![de icono Bombilla](media/bulb-cs.png) que aparece en el margen izquierdo si el cursor de texto ya está en la línea con el subrayado ondulado de color rojo.

   ![Vista previa de la generación de campo, propiedad o valor local](media/field-preview-cs.png)

   >[!TIP]
   >Use el vínculo [**Vista previa de los cambios**](../../ide/preview-changes.md) en la parte inferior de la ventana de vista previa para ver todos los cambios que se aplicarán antes de hacer la selección.

1. El campo, la propiedad o el valor local se creará automáticamente con el tipo que se deduce de su uso.

   ![Resultado de la generación de campo, propiedad o valor local](media/field-result-cs.png)

## <a name="see-also"></a>Vea también

[Generación de código](../code-generation-in-visual-studio.md)  
[Vista previa de cambios](../../ide/preview-changes.md)