---
title: Referencia de servicio web POX de detección automática de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 877152f0-f4b1-4f63-b2ce-924f4bdf2d20
description: Busque información de referencia para el servicio Detección automática POX en Exchange.
ms.openlocfilehash: a8797fe714fd23049094c3ec2475b93fec4282c0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836867"
---
# <a name="pox-autodiscover-web-service-reference-for-exchange"></a>Referencia de servicio web POX de detección automática de Exchange

Busque información de referencia para el servicio Detección automática POX en Exchange.
  
El servicio Detección automática proporciona la información de configuración que la aplicación se usa para crear una conexión a un servidor de Exchange. Puede usar el "XML sin formato antiguo" servicio de detección automática (POX) para enviar mensajes que sólo consisten en cargas XML, sin los sobres SOAP envolventes, con el fin de buscar la configuración de una aplicación de cliente debe tener para poder conectarse a Exchange.
  
> [!NOTE]
> Para los clientes que estén destinados a las versiones de Exchange Server 2010 a partir de Exchange, se recomienda que use el servicio Detección automática de SOAP en lugar del servicio de detección automática de POX. Los clientes que estén destinados a Exchange 2007 deben usar el servicio Detección automática POX. Se recomienda que los clientes que utilicen .NET Framework usan la API administrada de EWS porque contiene a un cliente de detección automática de POX robusto y probado. Para obtener más información acerca de la API administrada de EWS, vea [Introducción a las aplicaciones cliente de API administrada de EWS](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx). 
  
En esta sección se proporciona información acerca de los elementos XML que se envían entre el cliente y el servidor durante el redireccionamiento de la solicitud de detección automática POX y la configuración del usuario que se devuelve en una respuesta. La referencia de elemento XML contiene resúmenes de los elementos que representan y una descripción de las posibles jerarquías de elemento que usa el elemento. Esta documentación describen las instancias XML que se envían entre el cliente y el servidor. El servicio Detección automática POX no tiene un esquema explícito.
  
Los artículos de esta sección proporcionan ejemplos y descripciones de los mensajes que se usan para recuperar información de configuración de detección automática mediante el servicio de detección automática de POX. 
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_InThisSection"> </a>

- [Solicitud de detección automática POX para Exchange](pox-autodiscover-request-for-exchange.md)
    
- [Respuesta de detección automática POX para Exchange](pox-autodiscover-response-for-exchange.md)
    
- [Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)
    
## <a name="see-also"></a>Ver también

- [Referencia de servicio web de detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Detección automática de Exchange](../exchange-web-services/autodiscover-for-exchange.md)   
- [Referencia de servicio web de detección automática de SOAP para Exchange](soap-autodiscover-web-service-reference-for-exchange.md)
- [Empezar a utilizar servicios web de Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

