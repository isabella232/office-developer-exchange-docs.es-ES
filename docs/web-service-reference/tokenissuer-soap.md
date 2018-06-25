---
title: TokenIssuer (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d7be675-626c-4173-89e9-e32beef81ad5
description: El elemento TokenIssuer especifica el Uri (SOAP) y el extremo (SOAP) para el servicio de token de seguridad.
ms.openlocfilehash: 1c267fc6cbfdadd471c568473cc9aeeafb43ae2d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840684"
---
# <a name="tokenissuer-soap"></a>TokenIssuer (SOAP)

El elemento **TokenIssuer** especifica el [Uri (SOAP)](uri-soap.md) y el [Extremo (SOAP)](endpoint-soap.md) para el servicio de token de seguridad. 
  
```XML
<TokenIssuer>
   <Uri/>
   <Endpoint/>
</TokenIssuer>
```

 **TokenIssuer**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[URI (SOAP)](uri-soap.md) <br/> |El URI del servicio de token de seguridad que ha emitido el token de seguridad.  <br/> |
|[Extremo (SOAP)](endpoint-soap.md) <br/> |El URI del extremo de servicio de web.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[TokenIssuers (SOAP)](tokenissuers-soap.md) <br/> |Representa una colección de servicio de token de seguridad [Uri (SOAP)](uri-soap.md) y el [Extremo (SOAP)](endpoint-soap.md).  <br/> |
   
## <a name="remarks"></a>Comentarios

Use el elemento **TokenIssuer** para especificar el servicio de token de seguridad cuando se usa los tokens de seguridad. 
  
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

