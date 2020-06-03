---
title: Teléfono (PhoneEntityType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f6925cc9-7f22-478f-b9ba-b77575772471
description: El elemento Phone especifica un único número de teléfono que resulta de una extracción de entidades de números de teléfono.
ms.openlocfilehash: eec05fbb1cbbfa5c9b47cdb3cef1af6085ab51b6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457560"
---
# <a name="phone-phoneentitytype"></a>Teléfono (PhoneEntityType)

El elemento **Phone** especifica un único número de teléfono que resulta de una extracción de entidades de números de teléfono. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

[Posición](position.md)  |  [OriginalPhoneString](originalphonestring.md)  |  [PhoneString](phonestring.md)  |  [Tipo (cadena)](type-string.md)
  
### <a name="parent-elements"></a>Elementos principales

[PhoneNumbers (ArrayOfPhoneEntitiesType)](phonenumbers-arrayofphoneentitiestype.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   

