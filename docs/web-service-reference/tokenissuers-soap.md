---
title: TokenIssuers (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 26c55228-184e-4340-bd80-f86be56f3e7a
description: Los elementos TokenIssuers representan la colección TokenIssuer (SOAP).
ms.openlocfilehash: 68ff3ed515b346a84734596fae6fe127768b4476
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520405"
---
# <a name="tokenissuers-soap"></a>TokenIssuers (SOAP)

Los **elementos TokenIssuers** representan la [colección TokenIssuer (SOAP).](tokenissuer-soap.md) 
  
```XML
<TokenIssuers>
    <TokenIssuer/>
</TokenIssuers>
```

 **TokenIssuers**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[TokenIssuer (SOAP)](tokenissuer-soap.md) <br/> |Especifica el [Uri (SOAP) y](uri-soap.md) el extremo [(SOAP)](endpoint-soap.md) para el servicio de token de seguridad.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md) <br/> |Contiene la [respuesta de la operación GetFederationInformation (SOAP).](getfederationinformation-operation-soap.md)  <br/> |
   
## <a name="remarks"></a>Comentarios

**TokenIssuers** representa una colección de [elementos TokenIssuer (SOAP)](tokenissuer-soap.md) que se usarán en la detección automática. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[Referencia del servicio web de Detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
  
[Elementos XML de detección automática soap para Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

