---
title: TokenIssuers (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 26c55228-184e-4340-bd80-f86be56f3e7a
description: Los elementos TokenIssuers representan la colección TokenIssuer (SOAP).
ms.openlocfilehash: 352487ad3fd9c1ee7de756a109fb98a49d0cdcd7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457077"
---
# <a name="tokenissuers-soap"></a>TokenIssuers (SOAP)

Los elementos **TokenIssuers** representan la colección [TokenIssuer (SOAP)](tokenissuer-soap.md) . 
  
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
|[TokenIssuer (SOAP)](tokenissuer-soap.md) <br/> |Especifica el [URI (SOAP)](uri-soap.md) y el [extremo (SOAP)](endpoint-soap.md) para el servicio de token de seguridad.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetFederationInformationResponse (SOAP)](getfederationinformationresponse-soap.md) <br/> |Contiene la respuesta de [operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md) .  <br/> |
   
## <a name="remarks"></a>Comentarios

**TokenIssuers** representa una colección de elementos [TokenIssuer (SOAP)](tokenissuer-soap.md) que se usarán en la detección automática. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Referencia del servicio web de Detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
  
[Elementos XML de detección automática de SOAP para Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

