---
title: 'CA1041: Proporcionar un mensaje ObsoleteAttribute'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1041
- ProvideObsoleteAttributeMessage
helpviewer_keywords:
- ProvideObsoleteAttributeMessage
- CA1041
ms.assetid: be5bee69-d2d2-44e1-be2e-3ea451969003
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: bb8281cb299b9b6ada7470deca82b9158fb323d1
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/08/2019
ms.locfileid: "55953105"
---
# <a name="ca1041-provide-obsoleteattribute-message"></a>CA1041: Proporcionar un mensaje ObsoleteAttribute

|||
|-|-|
|TypeName|ProvideObsoleteAttributeMessage|
|Identificador de comprobación|CA1041|
|Categoría|Microsoft.Design|
|Cambio problemático|Poco problemático|

## <a name="cause"></a>Motivo
 Un tipo o miembro se marca con un <xref:System.ObsoleteAttribute?displayProperty=fullName> atributo que no tiene su <xref:System.ObsoleteAttribute.Message%2A?displayProperty=fullName> propiedad especificada.

## <a name="rule-description"></a>Descripción de la regla
 <xref:System.ObsoleteAttribute> se utiliza para marcar una biblioteca en desuso tipos y miembros. Los consumidores de la biblioteca deben evitar el uso de cualquier tipo o miembro que está marcado como obsoleto. Esto es porque es posible que no se admite y, finalmente, se quitará de las versiones posteriores de la biblioteca. Cuando un tipo o miembro marcado mediante <xref:System.ObsoleteAttribute> se compila, el <xref:System.ObsoleteAttribute.Message%2A> se muestra la propiedad del atributo. Esto proporciona información al usuario sobre el miembro o tipo obsoleto. Por lo general, esta información incluye cuánto tipo obsoleto o miembro se admitirá en los diseñadores de biblioteca y el reemplazo preferido para usar.

## <a name="how-to-fix-violations"></a>Cómo corregir infracciones
 Para corregir una infracción de esta regla, agregue el `message` parámetro para el <xref:System.ObsoleteAttribute> constructor.

## <a name="when-to-suppress-warnings"></a>Cuándo Suprimir advertencias
 No suprima una advertencia de esta regla porque el <xref:System.ObsoleteAttribute.Message%2A> propiedad proporciona información crítica sobre el tipo o miembro obsoleto.

## <a name="example"></a>Ejemplo
 El ejemplo siguiente muestra un miembro obsoleto que tiene declarado correctamente <xref:System.ObsoleteAttribute>.

 [!code-cpp[FxCop.Design.ObsoleteAttributeOnMember#1](../code-quality/codesnippet/CPP/ca1041-provide-obsoleteattribute-message_1.cpp)]
 [!code-csharp[FxCop.Design.ObsoleteAttributeOnMember#1](../code-quality/codesnippet/CSharp/ca1041-provide-obsoleteattribute-message_1.cs)]
 [!code-vb[FxCop.Design.ObsoleteAttributeOnMember#1](../code-quality/codesnippet/VisualBasic/ca1041-provide-obsoleteattribute-message_1.vb)]

## <a name="see-also"></a>Vea también
 <xref:System.ObsoleteAttribute?displayProperty=fullName>