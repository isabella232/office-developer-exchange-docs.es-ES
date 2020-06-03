---
title: BusinessPhoneNumbers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ecbe4f1c-1c9e-44e0-a8f7-08c160a0fddb
description: El elemento BusinessPhoneNumbers especifica una matriz de números de teléfono de la empresa y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: 8713af3ad302a2940cab247ff7188e55e8021ca0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461621"
---
# <a name="businessphonenumbers"></a>BusinessPhoneNumbers

El elemento **BusinessPhoneNumbers** especifica una matriz de números de teléfono de la empresa y los identificadores de sus atribuciones de origen para el rol asociado. 
  
```XML
<BusinessPhoneNumbers>
    <Value></Value>
    <Attributions></Attributions>
</BusinessPhoneNumbers>
```

 **ArrayOfPhoneNumberAttributedValuesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Valor (PersonaPhoneNumberType)](value-personaphonenumbertype.md) <br/> |Especifica un número de teléfono y la información del tipo y está asociado a un conjunto de atribuciones.  <br/> |
|[Atribuciones (ArrayOfValueAttributionsType)](attributions-arrayofvalueattributionstype.md) <br/> |Especifica una matriz de atribuciones para su elemento de **valor** asociado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Rol](persona.md) <br/> |Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

