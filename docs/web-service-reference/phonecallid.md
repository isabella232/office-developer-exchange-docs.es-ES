---
title: PhoneCallId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhoneCallId
api_type:
- schema
ms.assetid: 79e31a4c-fc84-4802-8761-470df8d63694
description: El elemento PhoneCallId especifica el identificador de una llamada telefónica. Se requiere este elemento.
ms.openlocfilehash: 1886d9510fe254c016779166efccc9882fd77d2c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836757"
---
# <a name="phonecallid"></a>PhoneCallId

El elemento **PhoneCallId** especifica el identificador de una llamada telefónica. Se requiere este elemento. 
  
```xml
<PhoneCallId Id="" />
```

 **PhoneCallIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|Id  <br/> |Identifica la llamada de teléfono a desconectar. Este atributo es necesario.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[DisconnectPhoneCall](disconnectphonecall.md) <br/> |Representa una solicitud para desconectar la llamada.  <br/> |
|[GetPhoneCallInformation](getphonecallinformation.md) <br/> |Representa una solicitud para obtener información de la llamada de teléfono.  <br/> |
|[PlayOnPhoneResponse (servicios Web de Exchange)](playonphoneresponse-exchange-web-services.md) <br/> |Define una respuesta a una solicitud de PlayOnPhone.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

