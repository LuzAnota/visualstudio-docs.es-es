---
title: Filtrar Establecer atributos de CLR en un elemento
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.dsltools.EditAttributesDialog
helpviewer_keywords:
- Domain-Specific Language, custom attrributes
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b890a5d3d5c48ad3841075a8ae818d2d37d44f98
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/08/2019
ms.locfileid: "55946631"
---
# <a name="how-to-set-clr-attributes-on-an-element"></a>Filtrar Establecer atributos de CLR en un elemento
Los atributos personalizados son atributos especiales que se pueden agregar a diagramas, formas, conectores y elementos de dominio. Puede agregar cualquier atributo que hereda de la `System.Attribute` clase.

### <a name="to-add-a-custom-attribute"></a>Para agregar un atributo personalizado

1.  En el **DSL Explorer**, seleccione el elemento al que desea agregar un atributo personalizado.

2.  En el **propiedades** ventana, junto a la **atributos personalizados** propiedad, haga clic en el (**...** ) icono.

     El **editar atributos** abre el cuadro de diálogo.

3.  En el **nombre** columna, haga clic en  **\<Agregar atributo >** y escriba el nombre del atributo. Presione ENTRAR.

4.  La línea bajo el nombre del atributo muestra entre paréntesis. En esta línea, escriba un tipo de parámetro para el atributo (por ejemplo, `string`), y, a continuación, presione ENTRAR.

5.  En el **nombre de propiedad** columna, escriba un nombre adecuado, por ejemplo, `MyString`.

6.  Haga clic en **Aceptar**.

     El **atributos personalizados** propiedad ahora muestra el atributo en el formato siguiente:

     `[` *AttributeName* `(` *ParameterName* `=` *tipo* `)]`

## <a name="see-also"></a>Vea también

- [Glosario de las Herramientas del lenguaje específico de dominio](https://msdn.microsoft.com/ca5e84cb-a315-465c-be24-76aa3df276aa)