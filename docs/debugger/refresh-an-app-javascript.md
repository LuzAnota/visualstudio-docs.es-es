---
title: Actualizar una aplicación para UWP | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- JavaScript debugging, refreshing pages [UWP apps]
- debugging, refreshing pages [UWP apps]
- DOM Explorer, Refresh [UWP apps]
- Refresh [UWP apps]
ms.assetid: fd99ee60-fa94-46df-8b17-369f60bfd908
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- uwp
ms.openlocfilehash: 0baa9e9a94b96682cda21dec9a5ba76cbe7f0065
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MTE95
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "54970921"
---
# <a name="refresh-a-uwp-app-in-visual-studio"></a>Actualizar una aplicación para UWP en Visual Studio
  
 Puede realizar cambios en el código mientras está depurando y, a continuación, actualice una aplicación para UWP con JavaScript eligiendo el **actualizar Windows app** situado en la **depurar** barra de herramientas. Al elegir este botón, se recarga la aplicación sin detener y reiniciar el depurador. La característica Actualizar te permite modificar código de HTML, CSS y JavaScript, y ver el resultado rápidamente. Esta característica se admite para aplicaciones UWP.  
  
 La actualización no conserva el estado de la aplicación ni refleja los siguientes cambios en la aplicación:  
  
-   Cambios en el archivo de manifiesto del paquete, incluidos los cambios de imágenes especificadas en el manifiesto del paquete.  
  
-   Cambios de referencias, como agregar o quitar una referencia de SDK, o cambios a los componentes de Windows Runtime (archivos .winmd).  
  
-   Cambios de recursos, como los aplicados a cadenas de archivos .resjson.  
  
-   Cambios del archivo de proyecto que dan lugar a cambios del nombre de la ruta de acceso, nuevos archivos de proyecto o archivos eliminados.  
  
-   Cambios de propiedades del proyecto y de elementos, como cambios en el dispositivo de depuración seleccionado, o en la acción de empaquetado de un archivo (en la ventana Propiedades).  
  
> [!IMPORTANT]
>  Cuando cambias las referencias, cambias el manifiesto del paquete o realizas otros cambios especificados en la lista anterior, debes detener y reiniciar el depurador para actualizar los archivos de código fuente HTML, CSS y JavaScript.  
  
### <a name="to-refresh-an-app"></a>Para actualizar una aplicación  
  
1.  Con el proyecto UWP abierto en Visual Studio, seleccione **máquina Local** como el destino de depuración.
  
     ![Lista de destinos de depuración seleccione](../debugger/media/js_select_target.png "JS_Select_Target")  
  
3.  Presiona F5 para ejecutar la aplicación en modo de depuración.  
  
4.  Cambia a Visual Studio. 
  
5.  En la página principal de la aplicación para UWP, editar algunas de HTML.
  
7.  Haz clic en el botón Actualizar aplicación de Windows **, que tiene este aspecto:** . ![Botón de la aplicación de Windows actualizar](../debugger/media/js_refresh.png "JS_Refresh"). (O bien, presiona F4).  
  
8.  Cambia a la aplicación. Se vuelve a cargar la aplicación y el HTML actualizado se usa para representar la aplicación.
  
## <a name="see-also"></a>Vea también  
 [Inicio rápido: depuración de HTML y CSS](../debugger/quickstart-debug-html-and-css.md)