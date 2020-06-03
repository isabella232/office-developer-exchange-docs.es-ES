---
title: TokenIssuer (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d7be675-626c-4173-89e9-e32beef81ad5
description: El elemento TokenIssuer especifica el URI (SOAP) y el extremo (SOAP) para el servicio de token de seguridad.
ms.openlocfilehash: e9c0b4140de26c7ff05daf4e863b3e8a17fedc62
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526329"
---
# <a name="tokenissuer-soap"></a>TokenIssuer (SOAP)

El elemento **TokenIssuer** especifica el [URI (SOAP)](uri-soap.md) y el [extremo (SOAP)](endpoint-soap.md) para el servicio de token de seguridad. 
  
```XML
<TokenIssuer>
   <Uri/>
   <Endpoint/>
</TokenIssuer>
```

 **TokenIssuer**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[URI (SOAP)](uri-soap.md) <br/> |URI del servicio de token de seguridad que emitió el token de seguridad.  <br/> |
|[Extremo (SOAP)](endpoint-soap.md) <br/> |URI del extremo del servicio Web.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[TokenIssuers (SOAP)](tokenissuers-soap.md) <br/> |Representa una colección de URI de servicio de token de seguridad [(SOAP)](uri-soap.md) y de [extremo (SOAP)](endpoint-soap.md).  <br/> |
   
## <a name="remarks"></a>Comentarios

Use el elemento **TokenIssuer** para especificar el servicio de token de seguridad al usar tokens de seguridad. 
  
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

