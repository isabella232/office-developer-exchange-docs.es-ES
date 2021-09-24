---
title: GetFederationInformationResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 2033c14f-dcc8-43c2-9fd9-a51946ec7055
description: El elemento GetFederationInformationResponse contiene la respuesta de la operación GetFederationInformation (SOAP).
ms.openlocfilehash: 20d00f047acae6c9eba1347ae7e8110656fefb4b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529882"
---
# <a name="getfederationinformationresponse-soap"></a>GetFederationInformationResponse (SOAP)

El **elemento GetFederationInformationResponse** contiene la respuesta de la operación [GetFederationInformation (SOAP).](getfederationinformation-operation-soap.md) 
  
```XML
<GetFederationInformationResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <TokenIssuers/>
   <ApplicationUri/>
   <Domains/>
</GetFederationInformationResponse>
```

 **GetFederationInformationResponse**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Representa un código de error devuelto por el servicio de detección automática.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Representa un mensaje asociado a un código de error devuelto por el servicio de detección automática.  <br/> |
|[ApplicationUri (SOAP)](applicationuri-soap.md) <br/> |Define la ubicación de una aplicación.  <br/> |
|[TokenIssuers (SOAP)](tokenissuers-soap.md) <br/> |Representa una colección de tokens de seguridad, que contienen identificadores de servicio de token de seguridad y puntos de conexión.  <br/> |
|[Domains (SOAP)](domains-soap.md) <br/> |Representa los dominios cuyas configuraciones se devuelven en una operación [GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) **GetDomainSettings** o los dominios que la organización ha federado en una operación [GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) **GetFederationInformation.**  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
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



[Operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)

