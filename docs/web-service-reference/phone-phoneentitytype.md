---
title: Teléfono (PhoneEntityType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f6925cc9-7f22-478f-b9ba-b77575772471
description: El elemento de teléfono especifica un número de teléfono único que dan como resultado de una extracción de entidades de número de teléfono.
ms.openlocfilehash: 654e8fc378ce3483cb3ebd9be33f3737ddd86bcb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836754"
---
# <a name="phone-phoneentitytype"></a>Teléfono (PhoneEntityType)

El elemento de **teléfono** especifica un número de teléfono único que dan como resultado de una extracción de entidades de número de teléfono. 
  
```XML
<Phone>
   <Position/>
   <OriginalPhoneString/>
   <PhoneString/>
   <Type/>
</Phone>
```

 **PhoneEntityType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[Posición](position.md) | [OriginalPhoneString](originalphonestring.md) | [PhoneString](phonestring.md) | [tipo (cadena)](type-string.md)
  
### <a name="parent-elements"></a>Elementos principales

[PhoneNumbers (ArrayOfPhoneEntitiesType)](phonenumbers-arrayofphoneentitiestype.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

