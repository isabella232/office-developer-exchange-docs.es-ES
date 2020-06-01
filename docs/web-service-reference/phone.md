---
title: Teléfono
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9381d8e0-b705-49fd-a822-00fb485bdbab
description: El elemento Phone especifica un único número de teléfono que resulta de una extracción de entidad de contacto.
ms.openlocfilehash: 7b0047eda90f2e2bb94fd7d0b8d317715ac5d2c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459710"
---
# <a name="phone"></a>Teléfono

El elemento **Phone** especifica un único número de teléfono que resulta de una extracción de entidad de contacto. 
  
```XML
<Phone>
   <OriginalPhoneString/>
   <PhoneString/>
   <Type/>
</Phone>
```

 **PhoneType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

[OriginalPhoneString](originalphonestring.md)  |  [PhoneString](phonestring.md)  |  [Tipo (cadena)](type-string.md)
  
### <a name="parent-elements"></a>Elementos principales

[PhoneNumbers (ArrayOfPhonesType)](phonenumbers-arrayofphonestype.md)
  
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
   

