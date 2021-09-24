---
title: EntityExtractionResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 643b99ab-ff90-4411-864c-1077623028d6
description: El elemento EntityExtractionResult especifica la propiedad EntityExtractionResult de un elemento.
ms.openlocfilehash: b550953233999bfd9c4dc08a7f892e798029df3c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520678"
---
# <a name="entityextractionresult"></a>EntityExtractionResult

El **elemento EntityExtractionResult** especifica la **propiedad EntityExtractionResult** de un elemento. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Addresses (ArrayOfAddressEntitiesType)](addresses-arrayofaddressentitiestype.md) <br/> |Especifica una matriz de **elementos AddressEntity.**  <br/> |
|[MeetingSuggestions](meetingsuggestions.md) <br/> |Especifica una matriz de **elementos MeetingSuggestion.**  <br/> |
|[TaskSuggestions](tasksuggestions.md) <br/> |Especifica una matriz de **elementos TaskSuggestion.**  <br/> |
|[EmailAddresses (ArrayOfEmailAddressEntitiesType)](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |Especifica una matriz de entidades de direcciones de correo electrónico.  <br/> |
|[Contacts (ArrayOfContactsType)](contacts-arrayofcontactstype.md) <br/> |Especifica una matriz de contactos.  <br/> |
|[Urls (ArrayOfUrlEntitiesType)](urls-arrayofurlentitiestype.md) <br/> |Especifica una matriz de direcciones URL.  <br/> |
|[PhoneNumbers (ArrayOfPhoneEntitiesType)](phonenumbers-arrayofphoneentitiestype.md) <br/> |Especifica una matriz de números de teléfono.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Item](item.md) <br/> |Representa un elemento genérico en el Exchange almacén.  <br/> |
   
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

