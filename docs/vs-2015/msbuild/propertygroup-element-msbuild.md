---
title: Elemento PropertyGroup (MSBuild) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#PropertyGroup
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- <PropertyGroup> element [MSBuild]
- PropertyGroup element [MSBuild]
ms.assetid: ff1e6c68-b9a1-4263-a1ce-dc3b829a64d4
caps.latest.revision: 24
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: fb3ae2ba566c42ef1cde10e4a758fe8f9698ed13
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MTE95
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2019
ms.locfileid: "54772532"
---
# <a name="propertygroup-element-msbuild"></a>Elemento PropertyGroup (MSBuild)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
Contiene un conjunto de elementos [Property](../msbuild/property-element-msbuild.md) definidos por el usuario. Cada elemento `Property` utilizado en un proyecto de [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] debe ser un elemento secundario de un elemento `PropertyGroup`.  
  
 \<Project>  
 \<PropertyGroup >  
  
## <a name="syntax"></a>Sintaxis  
  
```  
<PropertyGroup Condition="'String A' == 'String B'">  
    <Property1>...</Property1>  
    <Property2>...</Property2>  
</PropertyGroup>  
```  
  
## <a name="attributes-and-elements"></a>Atributos y elementos  
 En las siguientes secciones se describen los atributos, los elementos secundarios y los elementos primarios.  
  
### <a name="attributes"></a>Atributos  
  
|Atributo|Descripción|  
|---------------|-----------------|  
|Condición|Atributo opcional.<br /><br /> Condición que se va a evaluar. Para obtener más información, consulte [Condiciones](../msbuild/msbuild-conditions.md).|  
  
### <a name="child-elements"></a>Elementos secundarios  
  
|Elemento|Descripción|  
|-------------|-----------------|  
|[Property](../msbuild/property-element-msbuild.md)|Elemento opcional.<br /><br /> Un nombre de propiedad definido por el usuario, que contiene el valor de propiedad. Puede haber cero o más elementos *Property* en un elemento `PropertyGroup`.|  
  
### <a name="parent-elements"></a>Elementos primarios  
  
|Elemento|Descripción|  
|-------------|-----------------|  
|[Proyecto](../msbuild/project-element-msbuild.md)|Elemento raíz necesario de un archivo de proyecto [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] .|  
  
## <a name="example"></a>Ejemplo  
 En el ejemplo de código siguiente se muestra cómo establecer propiedades basadas en una condición. En este ejemplo, si el valor de la propiedad `CompileConfig` es `DEBUG`, se establecen las propiedades `Optimization`, `Obfuscate` y `OutputPath` dentro del elemento `PropertyGroup`.  
  
```  
<PropertyGroup Condition="'$(CompileConfig)' == 'DEBUG'" >  
    <Optimization>false</Optimization>  
    <Obfuscate>false</Obfuscate>  
    <OutputPath>$(OutputPath)\debug</OutputPath>  
</PropertyGroup>  
```  
  
## <a name="see-also"></a>Vea también  
 [Referencia de esquemas de archivo del proyecto](../msbuild/msbuild-project-file-schema-reference.md)  
 [Propiedades de MSBuild](msbuild-properties1.md)
