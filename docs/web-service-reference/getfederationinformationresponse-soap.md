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
description: El elemento GetFederationInformationResponse contiene la respuesta de la operación (SOAP) GetFederationInformation.
ms.openlocfilehash: 28b002b45968278ad4c7160b4eed29721422646d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764846"
---
# <a name="getfederationinformationresponse-soap"></a>GetFederationInformationResponse (SOAP)

El elemento **GetFederationInformationResponse** contiene la respuesta de la [operación de GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) . 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Representa un código de error devuelto por el servicio Detección automática.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Representa un mensaje en el que está asociado con un código de error devuelto por el servicio Detección automática.  <br/> |
|[ApplicationUri (SOAP)](applicationuri-soap.md) <br/> |Define la ubicación de una aplicación.  <br/> |
|[TokenIssuers (SOAP)](tokenissuers-soap.md) <br/> |Representa una colección de tokens de seguridad, que contienen los extremos y los identificadores del servicio de token de seguridad.  <br/> |
|[Dominios (SOAP)](domains-soap.md) <br/> |Representa los dominios de las configuraciones para la que se devuelven en una operación de la [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) **GetDomainSettings** o los dominios de que la organización ha federados en una [operación de GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) Operación **GetFederationInformation** .  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)

