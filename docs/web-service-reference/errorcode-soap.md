---
title: ErrorCode (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5e5ec861-0191-4ecb-a906-47ce8ed96381
description: El elemento ErrorCode representa un código de error devuelto por el servicio de detección automática.
ms.openlocfilehash: d66167e51733ffcaa3d62a985d3e03e2ac80b715
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460095"
---
# <a name="errorcode-soap"></a>ErrorCode (SOAP)

El elemento **ErrorCode** representa un código de error devuelto por el servicio de detección automática. 
  
```XML
<ErrorCode/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AutodiscoverResponse (SOAP)](autodiscoverresponse-soap.md) <br/> |Representa el tipo base para todas las respuestas que devuelve el servicio de detección automática.  <br/> |
|[DomainResponse (SOAP)](domainresponse-soap.md) <br/> |Contiene la configuración solicitada para el dominio especificado.  <br/> |
|[GetDomainSettingsResponse (SOAP)](getdomainsettingsresponse-soap.md) <br/> |Contiene la respuesta a una llamada de [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) para un dominio individual.  <br/> |
|[GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md) <br/> |Contiene la respuesta a una solicitud de [operación de GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .  <br/> |
|[Respuesta (SOAP)](response-soap.md) <br/> |Contiene la respuesta a una solicitud de [operación de GetUserSettings (SOAP)](getusersettings-operation-soap.md).  <br/> |
|[UserSettingError (SOAP)](usersettingerror-soap.md) <br/> |Representa un error que se devuelve al recuperar una configuración de usuario.  <br/> |
|[UserResponse (SOAP)](userresponse-soap.md) <br/> |Representa una respuesta a una solicitud de [operación de GetUserSettings (SOAP)](getusersettings-operation-soap.md) para un usuario individual.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el código de error de una respuesta de error de detección automática. En la siguiente tabla se enumeran los valores de texto posibles para el elemento **ErrorCode** . 
  
|**Valor de texto del código de error**|**Descripción**|
|:-----|:-----|
|NoError  <br/> |No hubo ningún error.  <br/> |
|RedirectAddress  <br/> |La persona que llama debe seguir la redirección de la dirección de correo electrónico que ha devuelto la detección automática.  <br/> |
|RedirectUrl  <br/> |La persona que llama debe seguir la redirección URL devuelta por la detección automática.  <br/> |
|InvalidUser  <br/> |El usuario que se pasó en la solicitud no es válido.  <br/> |
|InvalidRequest  <br/> |La solicitud no es válida.  <br/> |
|InvalidSetting  <br/> |Una configuración especificada no es válida.  <br/> |
|SettingIsNotAvailable  <br/> |Una configuración especificada no está disponible.  <br/> |
|ServerBusy  <br/> |El servidor está demasiado ocupado para procesar la solicitud.  <br/> |
|InvalidDomain  <br/> |El dominio solicitado no es válido.  <br/> |
|NotFederated  <br/> |La organización no está federada.  <br/> |
|InternalServerError  <br/> |Hay un error interno del servidor.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
  
[Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)
  
[Operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)

