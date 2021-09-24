---
title: Solicitud de detección automática POX para Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 75671b1d-f35b-497b-8d8c-706f3f2535fd
description: La solicitud de detección automática contiene una consulta para la configuración de acceso de cliente de un usuario.
ms.openlocfilehash: 8a0960dcff21276baf723512befacc4eca35950f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523870"
---
# <a name="pox-autodiscover-request-for-exchange"></a>Solicitud de detección automática POX para Exchange

La solicitud de detección automática contiene una consulta para la configuración de acceso de cliente de un usuario.
  
## <a name="autodiscover-request-example"></a>Ejemplo de solicitud de detección automática

### <a name="description"></a>Description

En el siguiente ejemplo XML se muestra un cuerpo de solicitud de detección automática.
  
### <a name="code"></a>Código

```XML
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
   <Request>
     <EMailAddress>user@contoso.com</EMailAddress>
     <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
   </Request>
 </Autodiscover>
```

### <a name="request-headers"></a>Encabezados de solicitud

Los siguientes encabezados HTTP son opcionales al enviar solicitudes de detección automática.
  
**Tabla 1. Encabezados de solicitud HTTP**

|**Header**|**Descripción**|
|:-----|:-----|
|X-MapiHttpCapability  <br/> |Si está presente y se establece en "1", indica que el cliente solicita información que se puede usar para conectarse al servidor mediante el protocolo MAPI/HTTP. Este encabezado es aplicable a los clientes que implementan el protocolo MAPI/HTTP.  <br/> |
|X-ClientCanHandle  <br/> |Este encabezado contiene una lista delimitada por comas de funcionalidades que admite el cliente. Los valores posibles se especifican en la tabla 2.  <br/> |
   
**Tabla 2. Valores de encabezado X-ClientCanHandle**

|**Valor X-ClientCanHandle (no tiene mayúsculas de minúsculas)**|**Versión mínima del servidor**|**Descripción**|
|:-----|:-----|:-----|
|Negociar  <br/> |15.00.0995.014  <br/> |Si este valor está presente, el servidor devolverá un valor de "Negociar" en el elemento [AuthPackage (POX)](authpackage-pox.md) si el servidor está configurado para aceptar la autenticación Negotiate. Si este valor no está presente, el servidor no devolverá un valor de "Negotiate" en el **elemento AuthPackage.**  <br/> |
|ExHttpInfo  <br/> |15.00.0995.014  <br/> |Si este valor está presente, el servidor devolverá un elemento [Protocol (POX)](protocol-pox.md) con un elemento [Type (POX)](type-pox.md) establecido en "EXHTTP" si el servidor está configurado para aceptar conexiones RPC/HTTP. Si este valor no está presente, el servidor no devolverá un **elemento Protocol** con un **elemento Type** establecido en "EXHTTP".  <br/> |
   
### <a name="request-elements"></a>Elementos Request

Los siguientes elementos se usan en el cuerpo de la solicitud:
  
- [AutoDiscover (POX)](autodiscover-pox.md)
    
- [Request (POX)](request-pox.md)
    
- [AcceptableResponseSchema (POX)](acceptableresponseschema-pox.md)
    
- [EMailAddress (POX)](emailaddress-pox.md)
    
> [!NOTE]
> El [elemento LegacyDN (POX)](legacydn-pox.md) se puede usar en lugar del elemento [EMailAddress (POX).](emailaddress-pox.md) 
  
### <a name="version-differences"></a>Diferencias de versión

El encabezado X-MapiHttpCapability está disponible en las versiones Office 365, Exchange Online y local de Exchange a partir de la compilación 15.00.0847.032 (Exchange Server 2013 SP1).
  
El encabezado X-ClientCanHandle está disponible en las versiones Office 365, Exchange Online y local de Exchange a partir de la compilación 15.00.0995.014.
  
## <a name="see-also"></a>Ver también



[Respuesta de detección automática de POX para Exchange](pox-autodiscover-response-for-exchange.md)


[Referencia del servicio web de detección automática de POX para Exchange](pox-autodiscover-web-service-reference-for-exchange.md)
  
[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

