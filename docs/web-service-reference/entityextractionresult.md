---
title: EntityExtractionResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 643b99ab-ff90-4411-864c-1077623028d6
description: El elemento EntityExtractionResult especifica la propiedad EntityExtractionResult de un elemento.
ms.openlocfilehash: ef99629beb95f1e1123569fa99e3f495c1b56e95
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764429"
---
# <a name="entityextractionresult"></a>EntityExtractionResult

El elemento **EntityExtractionResult** especifica la propiedad **EntityExtractionResult** de un elemento. 
  
```XML
<EntityExtractionResult>
    <Addresses/>
    <MeetingSuggestions/>
    <TaskSuggestions/>
    <EmailAddresses/>
    <Contacts/>
    <Urls/>
    <PhoneNumbers/>
</EntityExtractionResult>
```

 **EntityExtractionResultType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Direcciones (ArrayOfAddressEntitiesType)](addresses-arrayofaddressentitiestype.md) <br/> |Especifica una matriz de elementos de **AddressEntity** .  <br/> |
|[MeetingSuggestions](meetingsuggestions.md) <br/> |Especifica una matriz de elementos de **MeetingSuggestion** .  <br/> |
|[TaskSuggestions](tasksuggestions.md) <br/> |Especifica una matriz de elementos de **TaskSuggestion** .  <br/> |
|[EmailAddresses (ArrayOfEmailAddressEntitiesType)](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |Especifica una matriz de entidades de la dirección de correo electrónico.  <br/> |
|[Contactos (ArrayOfContactsType)](contacts-arrayofcontactstype.md) <br/> |Especifica una matriz de los contactos.  <br/> |
|[Direcciones URL (ArrayOfUrlEntitiesType)](urls-arrayofurlentitiestype.md) <br/> |Especifica una matriz de direcciones URL.  <br/> |
|[PhoneNumbers (ArrayOfPhoneEntitiesType)](phonenumbers-arrayofphoneentitiestype.md) <br/> |Especifica una matriz de números de teléfono.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Item](item.md) <br/> |Representa un elemento genérico en el almacén de Exchange.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

