---
title: Solicitud de detección automática POX para Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 75671b1d-f35b-497b-8d8c-706f3f2535fd
description: La solicitud de detección automática contiene una consulta para la configuración de acceso de cliente de un usuario.
ms.openlocfilehash: 48d6c30946e75936ed93a6f4507d8a8d3ae47d40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836865"
---
# <a name="pox-autodiscover-request-for-exchange"></a>Solicitud de detección automática POX para Exchange

La solicitud de detección automática contiene una consulta para la configuración de acceso de cliente de un usuario.
  
## <a name="autodiscover-request-example"></a>Ejemplo de solicitud de detección automática

### <a name="description"></a>Descripción

En el ejemplo de XML siguiente se muestra un cuerpo de la solicitud de detección automática.
  
### <a name="code"></a>Código

```XML
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
   <Request>
     <EMailAddress>user@contoso.com</EMailAddress>
     <AcceptableResponseSchema>http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
   </Request>
 </Autodiscover>
```

### <a name="request-headers"></a>Encabezados de solicitud

Los encabezados HTTP siguientes son opcionales al enviar solicitudes de detección automática.
  
**La tabla 1. Encabezados de solicitud HTTP**

|**Header**|**Descripción**|
|:-----|:-----|
|X-MapiHttpCapability  <br/> |Si está presente y establecido en "1", indica que el cliente está solicitando información que puede usar para conectarse al servidor mediante el protocolo HTTP/MAPI. Este encabezado es aplicable a los clientes que implementan el protocolo HTTP/MAPI.  <br/> |
|X-ClientCanHandle  <br/> |Este encabezado contiene una lista delimitada por comas de las capacidades que admite el cliente. Los valores posibles se especifican en la tabla 2.  <br/> |
   
**Tabla 2. Valores de encabezado X-ClientCanHandle**

|**Valor de X-ClientCanHandle (entre mayúsculas y minúsculas)**|**Versión de servidor mínimo**|**Descripción**|
|:-----|:-----|:-----|
|Negociar  <br/> |15.00.0995.014  <br/> |Si este valor está presente, el servidor devolverá un valor de "Negotiate" en el elemento [AuthPackage (POX)](authpackage-pox.md) si el servidor está configurado para aceptar la autenticación Negotiate. Si este valor no está presente, el servidor no devolverá un valor de "Negotiate" en el elemento **AuthPackage** .  <br/> |
|ExHttpInfo  <br/> |15.00.0995.014  <br/> |Si este valor está presente, el servidor devolverá un elemento de [Protocolo (POX)](protocol-pox.md) con un elemento de [Tipo (POX)](type-pox.md) se establece en "EXHTTP" si el servidor está configurado para aceptar conexiones RPC/HTTP. Si este valor no está presente, el servidor no devolverá un elemento de **protocolo** con un elemento de **tipo** establecido en "EXHTTP".  <br/> |
   
### <a name="request-elements"></a>Elementos de solicitud

En el cuerpo de la solicitud se usan los siguientes elementos:
  
- [Detección automática (POX)](autodiscover-pox.md)
    
- [Solicitud (POX)](request-pox.md)
    
- [AcceptableResponseSchema (POX)](acceptableresponseschema-pox.md)
    
- [EMailAddress (POX)](emailaddress-pox.md)
    
> [!NOTE]
> El elemento [LegacyDN (POX)](legacydn-pox.md) puede utilizarse en lugar del elemento [EMailAddress (POX)](emailaddress-pox.md) . 
  
### <a name="version-differences"></a>Diferencias de versión

El encabezado X-MapiHttpCapability está disponible en Office 365, Exchange Online, locales y en las versiones de Exchange comenzando por creación 15.00.0847.032 (Exchange Server 2013 SP1).
  
El encabezado X-ClientCanHandle está disponible en Office 365, Exchange Online, locales y en versiones de Exchange inicio con compilación 15.00.0995.014.
  
## <a name="see-also"></a>Ver también



[Respuesta de detección automática POX para Exchange](pox-autodiscover-response-for-exchange.md)


[Referencia de servicio web POX de detección automática de Exchange](pox-autodiscover-web-service-reference-for-exchange.md)
  
[Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

