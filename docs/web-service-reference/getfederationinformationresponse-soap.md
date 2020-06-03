---
title: GetFederationInformationResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2033c14f-dcc8-43c2-9fd9-a51946ec7055
description: El elemento GetFederationInformationResponse contiene la respuesta de operación GetFederationInformation (SOAP).
ms.openlocfilehash: c9e65a2b1759946b8493b3c730f08df6fe353fd8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460046"
---
# <a name="getfederationinformationresponse-soap"></a>GetFederationInformationResponse (SOAP)

El elemento **GetFederationInformationResponse** contiene la respuesta de [operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) . 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Representa un código de error devuelto por el servicio de detección automática.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Representa un mensaje que está asociado con un código de error devuelto por el servicio de detección automática.  <br/> |
|[ApplicationUri (SOAP)](applicationuri-soap.md) <br/> |Define la ubicación de una aplicación.  <br/> |
|[TokenIssuers (SOAP)](tokenissuers-soap.md) <br/> |Representa una colección de tokens de seguridad, que contiene identificadores de servicio de token de seguridad y puntos de conexión.  <br/> |
|[Dominios (SOAP)](domains-soap.md) <br/> |Representa los dominios de las configuraciones que se devuelven en una operación de [GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) **GetDomainSettings** o los dominios que la organización ha federado en una operación de [GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) **GetFederationInformation** .  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguna.
  
## <a name="text-value"></a>Valor de texto

Ninguna.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)

