---
title: BusinessPhoneNumbers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ecbe4f1c-1c9e-44e0-a8f7-08c160a0fddb
description: El elemento BusinessPhoneNumbers especifica una matriz de números de teléfono empresarial y los identificadores de sus atribuciones de origen para la persona asociada.
ms.openlocfilehash: 6de6bb2be8632c2872ff7ac771d559121c6454a0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518886"
---
# <a name="businessphonenumbers"></a>BusinessPhoneNumbers

El **elemento BusinessPhoneNumbers** especifica una matriz de números de teléfono empresarial y los identificadores de sus atribuciones de origen para la persona asociada. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Value (PersonaPhoneNumberType)](value-personaphonenumbertype.md) <br/> |Especifica un número de teléfono y una información de tipo y está asociado a un conjunto de atribuciones.  <br/> |
|[Attributions (ArrayOfValueAttributionsType)](attributions-arrayofvalueattributionstype.md) <br/> |Especifica una matriz de atribuciones para su elemento **Value** asociado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Rol](persona.md) <br/> |Especifica un conjunto de datos de persona devueltos por una **solicitud GetPersona.**  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

