---
title: TokenIssuers (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 26c55228-184e-4340-bd80-f86be56f3e7a
description: Los elementos de TokenIssuers representa la colección de TokenIssuer (SOAP).
ms.openlocfilehash: b070d85b32d5bce8461ac4e930329f237885bad7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840696"
---
# <a name="tokenissuers-soap"></a>TokenIssuers (SOAP)

Los elementos de **TokenIssuers** representa la colección de [TokenIssuer (SOAP)](tokenissuer-soap.md) . 
  
```XML
<TokenIssuers>
    <TokenIssuer/>
</TokenIssuers>
```

 **TokenIssuers**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[TokenIssuer (SOAP)](tokenissuer-soap.md) <br/> |Especifica el [Uri (SOAP)](uri-soap.md) y el [Extremo (SOAP)](endpoint-soap.md) para el servicio de token de seguridad.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md) <br/> |Contiene la respuesta de la [operación de GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .  <br/> |
   
## <a name="remarks"></a>Comentarios

El **TokenIssuers** representa una colección de elementos de [TokenIssuer (SOAP)](tokenissuer-soap.md) que se usará en la detección automática. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Referencia de servicio web de detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
  
[Elementos de Autodiscover XML SOAP para Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

