---
title: Uso de fuentes y colores | Documentos de Microsoft
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- fonts, controlling in IDE
- IDE, controlling text color and fonts
- Fonts and Colors property page
- font and color control [Visual Studio SDK]
- text, IDE
ms.assetid: d1a9b99f-fbdc-45ed-920a-e08c3d931ac9
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d0479fe12af73a90cf1f1bf4b2230a7fbbb9ba76
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "54919829"
---
# <a name="using-fonts-and-colors"></a>Uso de fuentes y colores
El [!INCLUDE[vsipsdk](../extensibility/includes/vsipsdk_md.md)] proporciona compatibilidad para que utilizar fuentes y colores para mostrar el texto.  
  
## <a name="in-this-section"></a>En esta sección  
 [Información general sobre fuentes y colores](../extensibility/font-and-color-overview.md)  
 Describe la configuración de fuente y color del texto en el [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] el entorno de desarrollo integrado (IDE). También se presentan los conceptos de categorías y mostrar los elementos y describe cómo utilizan los atributos de texto VSPackages y el editor básico.  
  
 [Obtención de información sobre fuentes y colores para la coloración de texto](../extensibility/getting-font-and-color-information-for-text-colorization.md)  
 Proporciona directrices para implementar la coloración de texto en los VSPackages que administran **categorías** distinto **Editor de texto**.  
  
 [Acceso a la configuración de fuentes y colores almacenados](../extensibility/accessing-stored-font-and-color-settings.md)  
 Explica cómo actual fuente y color configuración se puede almacenar, recuperar y aplicar.  
  
 [Implementación de categorías y elementos para mostrar personalizados](../extensibility/implementing-custom-categories-and-display-items.md)  
 Describe los pasos básicos que puede crear y usar su propio de una ventana **mostrar elementos** y **categorías** para admitir la presentación del texto.  
  
 Este enfoque requiere un VSPackage implementar el <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaultsProvider> interfaz y las interfaces relacionadas.  
  
 [Cómo: Obtener acceso a la combinación de colores y fuentes integradas](../extensibility/how-to-access-the-built-in-fonts-and-color-scheme.md)  
 Describe cómo definir y registrar una categoría mediante el uso de colores y fuentes integradas para iniciar el uso de colores y fuentes proporcionados por el sistema.  
  
## <a name="reference"></a>Referencia  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaultsProvider>  
 Proporciona una instancia de la `IVsFontAndColorDefaults` o <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorGroup> interfaz que corresponde a un elemento determinado que se muestran en el **mostrar valores para** lista en el **fuentes y colores** página de la **Opciones** cuadro de diálogo.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaults>  
 Habilita un VSPackage admitir el IDE **fuentes y colores** página mediante la definición predeterminada fuentes y colores de una ventana o un componente de interfaz de usuario.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorGroup>  
 Proporciona un mecanismo por el que un VSPackage que proporciona soporte técnico de fuente y color puede especificar un grupo de elemento de presentación - una supercategoría que representa la unión de dos o más categorías.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorStorage>  
 Habilita un VSPackage para recuperar datos de fuente y color, o lo guarda en el registro.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorEvents>  
 Notifica a los VSPackages que está usando la información de fuente y color acerca de los cambios en la configuración de fuente y color.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorUtilities>  
 Proporciona herramientas para trabajar con los datos de entrada y salidos que se usan los métodos de la [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] **fuente y Color** mecanismo.  
  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorCacheManager>  
 Controla el almacenamiento en caché de configuración de fuente y color.  
  
## <a name="related-sections"></a>Secciones relacionadas  
 [Desarrollo de un servicio de lenguaje heredado](../extensibility/internals/developing-a-legacy-language-service.md)  
 Se describe cómo los paquetes VSPackage pueden usar servicios de lenguaje para personalizar el [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] editor.  
  
 [Colores de sintaxis en editores personalizados](../extensibility/syntax-coloring-in-custom-editors.md)  
 Se explica cómo el [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] editor usa servicios de lenguaje para implementar los colores de sintaxis.  
  
 [Ampliación de otras partes de Visual Studio](../extensibility/extending-other-parts-of-visual-studio.md)  
 Explica cómo usar los servicios de [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] para crear elementos de interfaz de usuario que coincidan con el resto de servicios de [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].