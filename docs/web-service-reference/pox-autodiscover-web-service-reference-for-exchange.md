---
title: Referencia del servicio web de detección automática de POX para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 877152f0-f4b1-4f63-b2ce-924f4bdf2d20
description: Busque información de referencia para el servicio de detección automática POX en Exchange.
ms.openlocfilehash: b28ea64a82960a84dee06c5055ee915614f4fde7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516422"
---
# <a name="pox-autodiscover-web-service-reference-for-exchange"></a>Referencia del servicio web de detección automática de POX para Exchange

Busque información de referencia para el servicio de detección automática POX en Exchange.
  
El servicio de detección automática proporciona la información de configuración que la aplicación usa para crear una conexión a un Exchange servidor. Puede usar el servicio de detección automática "XML antiguo sin formato" (POX) para enviar mensajes que solo constan de cargas XML, sin sobres SOAP envolventes, con el fin de localizar la configuración que debe tener una aplicación cliente para conectarse a Exchange.
  
> [!NOTE]
> Para los clientes que tienen como destino las versiones de Exchange a partir de Exchange Server 2010, se recomienda usar el servicio de detección automática SOAP en lugar del servicio de detección automática de POX. Los clientes que Exchange 2007 deben usar el servicio de detección automática de POX. Se recomienda que los clientes que usan el .NET Framework la API administrada ews porque contiene un cliente de detección automática pox sólido y probado. Para obtener más información acerca de la API administrada de EWS, vea [Introducción a las aplicaciones](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx)cliente de la API administrada ews . 
  
En esta sección se proporciona información sobre los elementos XML que se envían entre el cliente y el servidor durante las redirecciones de solicitud de detección automática de POX y la configuración del usuario que se devuelve en una respuesta. La referencia de elemento XML contiene resúmenes de lo que representan los elementos y una descripción de las posibles jerarquías de elementos que usan el elemento. Esta documentación trata las instancias XML que se envían entre el cliente y el servidor. El servicio de detección automática pox no tiene un esquema explícito.
  
Los artículos de esta sección proporcionan ejemplos y descripciones de los mensajes que se usan para recuperar información de configuración de detección automática mediante el servicio de detección automática pox. 
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_InThisSection"> </a>

- [Solicitud de detección automática POX para Exchange](pox-autodiscover-request-for-exchange.md)
    
- [Respuesta de detección automática de POX para Exchange](pox-autodiscover-response-for-exchange.md)
    
- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)
    
## <a name="see-also"></a>Ver también

- [Referencia del servicio web de Detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Detección automática en Exchange](../exchange-web-services/autodiscover-for-exchange.md)   
- [Referencia de servicio web de detección automática SOAP para Exchange](soap-autodiscover-web-service-reference-for-exchange.md)
- [Empezar a usar los servicios web de Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

