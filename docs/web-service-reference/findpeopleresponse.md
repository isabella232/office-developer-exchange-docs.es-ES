---
title: FindPeopleResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 95f016a9-002f-4be3-abd6-f5e3528afd44
description: El elemento FindPeopleResponse especifica la respuesta a una solicitud de FindPeople.
ms.openlocfilehash: 4f2c2f6069a515d5153ea488b35182d8b35f029f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764649"
---
# <a name="findpeopleresponse"></a>FindPeopleResponse

El elemento **FindPeopleResponse** especifica la respuesta a una solicitud de **FindPeople** . 
  
```XML
<FindPeopleResponse ResponseClass=" Success | Warning | Error ">
    <People/>
    <TotalNumberOfPeopleInView/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</FindPeopleResponse>
```

 **FindPeopleResponseMessageType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|ResponseClass  <br/> |Especifica la clase de respuesta.  <br/> |
   
#### <a name="responseclass"></a>ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|Correcto  <br/> |Indica éxito.  <br/> |
|Advertencia  <br/> |Indica una advertencia.  <br/> |
|Error  <br/> |Indica un error.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Personas](people.md) <br/> |Especifica una matriz de datos de rol devueltos como resultado de una solicitud de **FindPeople** .  <br/> |
|[TotalNumberOfPeopleInView](totalnumberofpeopleinview.md) <br/> |Especifica el número total de roles almacenados en un servidor que se devuelven por una solicitud de **FindPeople** .  <br/> |
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona información de estado acerca de la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no utilizado y reservado para uso futuro.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información de la respuesta de error adicionales.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Especifica una matriz de los mensajes de respuesta.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

