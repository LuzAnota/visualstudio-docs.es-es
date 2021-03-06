---
title: Creación de una extensión con una ventana de herramientas | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 585b0a3a-f85b-4f92-81bb-9ca499bb8a89
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d1450a7a7e254f9045b0f29cda4359e1e0676c65
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "55034732"
---
# <a name="create-an-extension-with-a-tool-window"></a>Crear una extensión con una ventana de herramientas
En este procedimiento, aprenda a usar la plantilla de proyecto VSIX y la **ventana de herramientas personalizada** plantilla de elemento para crear una extensión con una ventana de herramientas.  
  
## <a name="prerequisites"></a>Requisitos previos  
 A partir de Visual Studio 2015, no instale el SDK de Visual Studio desde el centro de descarga. Se incluye como una característica opcional en el programa de instalación de Visual Studio. También puede instalar el SDK de VS más adelante. Para obtener más información, consulte [instalar el SDK de Visual Studio](../extensibility/installing-the-visual-studio-sdk.md).  
  
### <a name="create-a-tool-window"></a>Crear una ventana de herramientas  
  
1.  Cree un proyecto VSIX denominado **FirstWindow**. Puede encontrar la plantilla de proyecto VSIX en el **nuevo proyecto** en el cuadro de diálogo **Visual C#** > **extensibilidad**.  
  
2.  Cuando se abra el proyecto, agregue una plantilla de elemento de ventana de herramienta denominada **MyWindow**. En el **el Explorador de soluciones**, haga clic en el nodo del proyecto y seleccione **agregar** > **nuevo elemento**. En el **Agregar nuevo elemento** cuadro de diálogo, vaya a **Visual C#** > **extensibilidad** y seleccione **ventana de herramientas personalizada**. En el **nombre** campo en la parte inferior de la ventana, cambie el nombre de archivo de la ventana de herramienta a *MyWindow.cs*.  
  
3.  Compile la solución y comience la depuración.  
  
     Aparece la instancia experimental de Visual Studio. Para obtener más información acerca de la instancia experimental, consulte [la instancia experimental](../extensibility/the-experimental-instance.md).  
  
4.  En la instancia experimental, vaya a **vista** > **Other Windows**.  
  
     Debería ver un elemento de menú para **MyWindow**. Haga clic en él.  
  
     Debería ver una ventana de herramientas con el título **MyWindow** y un comentario de botón **Click Me!.**