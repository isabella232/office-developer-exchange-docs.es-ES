---
title: Response (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 4c2bcdeb-95ce-4ffa-bd83-118af53b534f
description: El elemento Response contiene la respuesta a una operación GetUserSettings (SOAP), una operación GetDomainSettings (SOAP) o una solicitud de operación GetFederationInformation (SOAP).
ms.openlocfilehash: d42014991db8e93f88b80bed97970f043290cfb1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512362"
---
# <a name="response-soap"></a>Response (SOAP)

El **elemento Response** contiene la respuesta a una operación [GetUserSettings (SOAP),](getusersettings-operation-soap.md)una operación [GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)o una solicitud de operación [GetFederationInformation (SOAP).](getfederationinformation-operation-soap.md) 
  
```XML
<Response>
   <ErrorCode/>
   <ErrorMessage/>
   <UserResponses/>
</Response>
```

 **GetUserSettingsResponse**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Representa un código de error devuelto por el servicio de detección automática.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Representa un mensaje asociado a un código de error devuelto por el servicio de detección automática.  <br/> |
|[UserResponses (SOAP)](userresponses-soap.md) <br/> |Contiene las opciones de configuración de cada usuario solicitado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetUserSettingsResponseMessage (SOAP)](getusersettingsresponsemessage-soap.md) <br/> |Define una respuesta a [GetUserSettingsRequest (SOAP)](getusersettingsrequest-soap.md) <br/> |
|[GetDomainSettingsResponseMessage (SOAP)](getdomainsettingsresponsemessage-soap.md) <br/> |Define una respuesta a [un objeto GetDomainSettingsRequest (SOAP).](getdomainsettingsrequest-soap.md)  <br/> |
|[GetFederationInformationResponseMessage (SOAP)](getfederationinformationresponsemessage-soap.md) <br/> |Define una respuesta a [un objeto GetFederationInformationRequest (SOAP).](getfederationinformationrequest-soap.md)  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)


[Referencia del servicio web de Detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
  
[Elementos XML de detección automática soap para Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

