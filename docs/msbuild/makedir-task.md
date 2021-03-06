---
title: Tarea MakeDir | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#MakeDir
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MakeDir task [MSBuild]
- MSBuild, MakeDir task
ms.assetid: bc951577-1bfb-4100-b1f1-bc8278c45bf7
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3e7e9e61ffd20828d73cef9c4ce3831d613d69bf
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/08/2019
ms.locfileid: "55922230"
---
# <a name="makedir-task"></a>MakeDir (tarea)
Crea directorios y, si es preciso, cualquier directorio primario.

## <a name="parameters"></a>Parámetros
En la siguiente tabla se describen los parámetros de la tarea `MakeDir` .

|Parámetro|Descripción|
|---------------|-----------------|
|`Directories`|Parámetro <xref:Microsoft.Build.Framework.ITaskItem>`[]` requerido.<br /><br /> Conjunto de directorios que se va a crear.|
|`DirectoriesCreated`|Parámetro de salida <xref:Microsoft.Build.Framework.ITaskItem>`[]` opcional.<br /><br /> Directorios que crea esta tarea. Si no se pudieron crear algunos directorios, podría no contener todos los elementos que se han pasado en el parámetro `Directories`.|

## <a name="remarks"></a>Comentarios
Además de los parámetros mencionados anteriormente, esta tarea hereda los parámetros de la clase <xref:Microsoft.Build.Tasks.TaskExtension>, que a su vez hereda de la clase <xref:Microsoft.Build.Utilities.Task>. Para obtener una lista de estos parámetros adicionales y sus descripciones, consulte [TaskExtension base class](../msbuild/taskextension-base-class.md).

## <a name="example"></a>Ejemplo
En el siguiente ejemplo de código se usa la tarea `MakeDir` para crear el directorio especificado por la propiedad `OutputDirectory`.

```xml
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">

    <PropertyGroup>
        <OutputDirectory>\Output\</OutputDirectory>
    </PropertyGroup>

    <Target Name="CreateDirectories">
        <MakeDir
            Directories="$(OutputDirectory)"/>
    </Target>

</Project>
```

## <a name="see-also"></a>Vea también
[Tareas](../msbuild/msbuild-tasks.md)  
[Referencia de tareas](../msbuild/msbuild-task-reference.md)
