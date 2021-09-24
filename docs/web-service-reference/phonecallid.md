---
title: PhoneCallId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PhoneCallId
api_type:
- schema
ms.assetid: 79e31a4c-fc84-4802-8761-470df8d63694
description: El elemento PhoneCallId especifica el identificador de una llamada telefónica. Se requiere este elemento.
ms.openlocfilehash: 00b23c8b4023a6fef9c27295c8e023e5324b7026
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528322"
---
# <a name="phonecallid"></a>PhoneCallId

El **elemento PhoneCallId** especifica el identificador de una llamada telefónica. Se requiere este elemento. 
  
```xml
<PhoneCallId Id="" />
```

 **PhoneCallIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|Id  <br/> |Identifica la llamada telefónica que se debe desconectar. Este atributo es obligatorio.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DisconnectPhoneCall](disconnectphonecall.md) <br/> |Representa una solicitud para desconectar una llamada.  <br/> |
|[GetPhoneCallInformation](getphonecallinformation.md) <br/> |Representa una solicitud para obtener información de llamadas telefónicas.  <br/> |
|[PlayOnPhoneResponse (Exchange Web Services)](playonphoneresponse-exchange-web-services.md) <br/> |Define una respuesta a una solicitud de PlayOnPhone.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

