---
title: 'CA1717: Solo las enumeraciones FlagsAttribute deben tener nombres en plural'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1717
- OnlyFlagsEnumsShouldHavePluralNames
helpviewer_keywords:
- OnlyFlagsEnumsShouldHavePluralNames
- CA1717
ms.assetid: a6855d8b-d78a-42c1-834e-61c31f5572ed
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7fb7a0ebe6dd068b9552a32b914e1936f1053aa3
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/08/2019
ms.locfileid: "55921710"
---
# <a name="ca1717-only-flagsattribute-enums-should-have-plural-names"></a>CA1717: Solo las enumeraciones FlagsAttribute deben tener nombres en plural

|||
|-|-|
|TypeName|OnlyFlagsEnumsShouldHavePluralNames|
|Identificador de comprobación|CA1717|
|Categoría|Microsoft.Naming|
|Cambio problemático|Problemático|

## <a name="cause"></a>Motivo
 El nombre de una enumeración visible externamente termina en una palabra en plural y la enumeración no está marcada con el <xref:System.FlagsAttribute?displayProperty=fullName> atributo.

## <a name="rule-description"></a>Descripción de la regla
 Convenciones de nomenclatura dictan que un nombre plural para una enumeración indica que se puede especificar más de un valor de la enumeración al mismo tiempo. El <xref:System.FlagsAttribute> indica a los compiladores que la enumeración debe tratarse como un campo de bits que habilita las operaciones bit a bit en la enumeración.

 Si solo puede especificarse un valor de enumeración a la vez, el nombre de la enumeración debe ser una palabra en singular. Por ejemplo, una enumeración que define los días de la semana esté destinada para su uso en una aplicación que se pueden especificar varios días. Esta enumeración debe tener el <xref:System.FlagsAttribute> y podría denominarse 'Días'. Una enumeración similar que permite sólo un día que se especifique no tendría el atributo y podría ser denominada 'Day'.

 Las convenciones de nomenclatura proporcionan una apariencia común para las bibliotecas destinadas a Common Language Runtime. Esto reduce el tiempo que se requiere para obtener información sobre una nueva biblioteca de software y aumenta la confianza del cliente que la biblioteca fue desarrollada por alguien que tenga experiencia en desarrollo de código administrado.

## <a name="how-to-fix-violations"></a>Cómo corregir infracciones
 Cambie el nombre de la enumeración de una palabra en singular o agregar el <xref:System.FlagsAttribute>.

## <a name="when-to-suppress-warnings"></a>Cuándo Suprimir advertencias
 Es seguro suprimir una advertencia de la regla si el nombre termina en una palabra en singular.

## <a name="related-rules"></a>Reglas relacionadas
 [CA1714: Las enumeraciones Flags deberían tener nombres en plurales](../code-quality/ca1714-flags-enums-should-have-plural-names.md)

 [CA1027: Marcar enumeraciones con FlagsAttribute](../code-quality/ca1027-mark-enums-with-flagsattribute.md)

 [CA2217: No marcar enumeraciones con FlagsAttribute](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)

## <a name="see-also"></a>Vea también

- <xref:System.FlagsAttribute?displayProperty=fullName>
- [Diseño de enumeraciones](/dotnet/standard/design-guidelines/enum)