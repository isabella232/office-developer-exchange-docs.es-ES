---
title: TokenIssuer (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2d7be675-626c-4173-89e9-e32beef81ad5
description: El elemento TokenIssuer especifica el Uri (SOAP) y el extremo (SOAP) para el servicio de token de seguridad.
ms.openlocfilehash: ea1c93493e4f47a6f2551c24586e54614f4f45e6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527268"
---
# <a name="tokenissuer-soap"></a>TokenIssuer (SOAP)

El **elemento TokenIssuer** especifica el [Uri (SOAP)](uri-soap.md) y el extremo [(SOAP)](endpoint-soap.md) para el servicio de token de seguridad. 
  
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
|[Uri (SOAP)](uri-soap.md) <br/> |Uri del servicio de token de seguridad que emitió el token de seguridad.  <br/> |
|[Endpoint (SOAP)](endpoint-soap.md) <br/> |Uri de extremo del servicio web.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[TokenIssuers (SOAP)](tokenissuers-soap.md) <br/> |Representa una colección de uri de servicio de [token de seguridad (SOAP)](uri-soap.md) y [punto de conexión (SOAP).](endpoint-soap.md)  <br/> |
   
## <a name="remarks"></a>Comentarios

Use el **elemento TokenIssuer** para especificar el servicio de token de seguridad al usar tokens de seguridad. 
  
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

