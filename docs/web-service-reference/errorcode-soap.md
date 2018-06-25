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
description: El elemento ErrorCode representa un código de error devuelto por el servicio Detección automática.
ms.openlocfilehash: 2dd91cec4645325c02bc8588af0ee0547909b945
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764436"
---
# <a name="errorcode-soap"></a>ErrorCode (SOAP)

El elemento **ErrorCode** representa un código de error devuelto por el servicio Detección automática. 
  
```XML
<ErrorCode/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[AutodiscoverResponse (SOAP)](autodiscoverresponse-soap.md) <br/> |Representa el tipo base para todas las respuestas que son devueltos por el servicio de detección automática.  <br/> |
|[DomainResponse (SOAP)](domainresponse-soap.md) <br/> |Contiene la configuración solicitada para el dominio especificado.  <br/> |
|[GetDomainSettingsResponse (SOAP)](getdomainsettingsresponse-soap.md) <br/> |Contiene la respuesta a una llamada de la [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) para un dominio individual.  <br/> |
|[GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md) <br/> |Contiene la respuesta a una solicitud de [operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .  <br/> |
|[Respuesta (SOAP)](response-soap.md) <br/> |Contiene la respuesta a una solicitud de [operación GetUserSettings (SOAP)](getusersettings-operation-soap.md).  <br/> |
|[UserSettingError (SOAP)](usersettingerror-soap.md) <br/> |Representa un error que se devuelve al recuperar una configuración de usuario.  <br/> |
|[UserResponse (SOAP)](userresponse-soap.md) <br/> |Representa una respuesta a una solicitud de [operación GetUserSettings (SOAP)](getusersettings-operation-soap.md) para un usuario individual.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el código de error para una respuesta de error de detección automática. En la siguiente tabla se enumera los posibles valores de texto para el elemento de **código de error** . 
  
|**Valor de texto del código de error**|**Descripción**|
|:-----|:-----|
|NoError  <br/> |Se ha producido ningún error.  <br/> |
|RedirectAddress  <br/> |El autor de la llamada debe seguir la redirección de dirección de correo electrónico que se ha devuelto por la detección automática.  <br/> |
|RedirectUrl  <br/> |El autor de la llamada debe seguir la redirección de dirección URL que se ha devuelto por la detección automática.  <br/> |
|InvalidUser  <br/> |El usuario que se pasó en la solicitud no es válido.  <br/> |
|InvalidRequest  <br/> |La solicitud no es válida.  <br/> |
|InvalidSetting  <br/> |Una opción de configuración especificado no es válido.  <br/> |
|SettingIsNotAvailable  <br/> |Una opción de configuración especificado no está disponible.  <br/> |
|ServerBusy  <br/> |El servidor está demasiado ocupado para procesar la solicitud.  <br/> |
|InvalidDomain  <br/> |El dominio solicitado no es válido.  <br/> |
|NotFederated  <br/> |La organización no está federada.  <br/> |
|InternalServerError  <br/> |Hay un error interno del servidor.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
  
[Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)
  
[Operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)

