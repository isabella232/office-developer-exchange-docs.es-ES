---
title: Referencia de servicio Web de detección automática de POX para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 877152f0-f4b1-4f63-b2ce-924f4bdf2d20
description: Busque información de referencia para el servicio Detección automática de POX en Exchange.
ms.openlocfilehash: 3c0ca368f4427be7759e2db58fb418b4822dea8e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465656"
---
# <a name="pox-autodiscover-web-service-reference-for-exchange"></a>Referencia de servicio Web de detección automática de POX para Exchange

Busque información de referencia para el servicio Detección automática de POX en Exchange.
  
El servicio Detección automática proporciona la información de configuración que la aplicación usa para crear una conexión a un servidor de Exchange. Puede usar el servicio de detección automática "XML anterior" (POX) para enviar mensajes que consten solo de cargas XML, sin ningún envoltorio SOAP envolvente, para localizar la configuración que debe tener una aplicación cliente para conectarse a Exchange.
  
> [!NOTE]
> Para los clientes que tienen como destino versiones de Exchange que comienzan con Exchange Server 2010, se recomienda usar el servicio de detección automática de SOAP en lugar del servicio Detección automática de POX. Los clientes que tienen el destino de Exchange 2007 deben usar el servicio Detección automática de POX. Se recomienda que los clientes que usan .NET Framework usen la API administrada de EWS porque contiene un cliente de detección automática de POX sólido y bien probado. Para obtener más información sobre la API administrada de EWS, vea Introducción [a las aplicaciones cliente de la API administrada de EWS](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx). 
  
En esta sección se proporciona información sobre los elementos XML que se envían entre el cliente y el servidor durante la redirección de la solicitud de detección automática de POX y la configuración de usuario que se devuelve en una respuesta. La referencia del elemento XML contiene resúmenes de lo que representan los elementos y una descripción de las jerarquías de elementos potenciales que usan el elemento. En esta documentación se describen las instancias de XML que se envían entre el cliente y el servidor. El servicio Detección automática de POX no tiene un esquema explícito.
  
En los artículos de esta sección se proporcionan ejemplos y descripciones de los mensajes que se usan para recuperar información de configuración de detección automática mediante el servicio Detección automática de POX. 
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_InThisSection"> </a>

- [Solicitud de detección automática de POX para Exchange](pox-autodiscover-request-for-exchange.md)
    
- [Respuesta de detección automática de POX para Exchange](pox-autodiscover-response-for-exchange.md)
    
- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)
    
## <a name="see-also"></a>Vea también

- [Referencia del servicio web de Detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Detección automática en Exchange](../exchange-web-services/autodiscover-for-exchange.md)   
- [Referencia del servicio Web de detección automática de SOAP para Exchange](soap-autodiscover-web-service-reference-for-exchange.md)
- [Empezar a usar los servicios web de Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

