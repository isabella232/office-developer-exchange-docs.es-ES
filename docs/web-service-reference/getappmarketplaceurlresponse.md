---
title: GetAppMarketplaceUrlResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc3368ec-78c2-4f8d-8394-4891e90dafd2
description: El elemento GetAppMarketplaceUrlResponse especifica la respuesta a una solicitud de GetAppMarketplaceUrl.
ms.openlocfilehash: 553ebfc4615280c77d4a1ef9e5db3e5d10a0f2a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764750"
---
# <a name="getappmarketplaceurlresponse"></a>GetAppMarketplaceUrlResponse

El elemento **GetAppMarketplaceUrlResponse** especifica la respuesta a una solicitud de **GetAppMarketplaceUrl** . 
  
```XML
<GetAppMarketplaceUrlResponse ResponseClass=" Success | Warning | Error ">
    <AppMarketplaceUrl/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetAppMarketplaceUrlResponse>
```

 **GetAppMarketplaceUrlResponseMessageType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|ResponseClass  <br/> |Indica la clase de la respuesta.  <br/> |
   
#### <a name="responseclass"></a>ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|Correcto  <br/> |Indica éxito.  <br/> |
|Advertencia  <br/> |Indica una advertencia.  <br/> |
|Error  <br/> |Indica un error.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[AppMarketplaceUrl](appmarketplaceurl.md) <br/> |Especifica la dirección URL de la aplicación.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no utilizado y reservado para uso futuro.  <br/> |
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información de la respuesta de error adicionales.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona información de estado acerca de la solicitud.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.  <br/> |
   
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

