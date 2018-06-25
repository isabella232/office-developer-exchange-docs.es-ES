---
title: ActingAs
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ActingAs
api_type:
- schema
ms.assetid: 3896afff-5c2c-4eaf-8621-c70e0371ea78
description: El elemento ActingAs identifica quién envía como el autor de la llamada.
ms.openlocfilehash: 9c007ed45f85dba265261dd79a6fd846dbd9d2f9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764568"
---
# <a name="actingas"></a>ActingAs

El elemento **ActingAs** identifica quién envía como el autor de la llamada. 
  
```xml
<ActingAs>
   <EmailAddress/>
   <RoutingType/>
</ActingAs>
```

 **EmailAddressType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Define la dirección de Protocolo Simple de transferencia de correo (SMTP) de un usuario de buzón de correo. Este elemento es opcional.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Define la ruta que se usa para el buzón de correo. El valor predeterminado es SMTP. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetServiceConfiguration](getserviceconfiguration.md) <br/> |Define una solicitud **GetServiceConfiguration** .  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento es opcional. Si este elemento no está presente, el usuario autenticado se supone que el remitente. El elemento **ActingAs** debe incluirse para solicitar sugerencias de remitente. Puede devolver un error de **ErrorInvalidArgument** en una respuesta si el elemento **ActingAs** falta, no incluye un tipo de distribución, no incluye una dirección de correo electrónico, contiene una dirección de correo electrónico no válida, no se resuelve a un usuario en Active Directory Servicios de dominio (AD DS), o se resuelve a varios usuarios en AD DS. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

