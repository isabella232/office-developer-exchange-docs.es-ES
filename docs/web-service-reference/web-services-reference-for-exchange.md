---
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6c969133-6036-448b-af39-a3caf9917e98
description: Busque información de referencia para los servicios web de Exchange.
ms.openlocfilehash: 417ade6956ee5e09fe7ad63f09e59f0079d58613
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840979"
---
# <a name="web-services-reference-for-exchange"></a>Referencia de servicios Web de Exchange

Busque información de referencia para los servicios web de Exchange.
  
En esta sección se incluye información de referencia para las API que de destino o que están incluyen en Exchange Online, Exchange Online como parte de Office 365 y las versiones de Exchange a partir de Exchange Server 2007. En esta sección se incluye el siguiente contenido:
  
- [Referencia EWS para Exchange](ews-reference-for-exchange.md) : documentación de referencia de API de contiene para la API de servicios de Web de Exchange (EWS). Ésta es la API principal para la creación de clientes y los servicios que se conectan a Exchange para obtener acceso a la información del buzón. Este contenido incluye información sobre las operaciones que están disponibles en EWS y documentación de referencia XML que proporciona información acerca de la instancia de XML que se envían a y se reciben desde Exchange. 
    
- [Referencia de API administrada de EWS](http://msdn.microsoft.com/library/c6ca36f4-a67c-4e3c-aae7-9ead7b704e15%28Office.15%29.aspx) : documentación de referencia de API de contiene para la API administrada de EWS. La API administrada de EWS es una interfaz simple y completas para desarrollar y ampliación de las aplicaciones que usan EWS. 
    
- [Referencia de servicio web de detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md) : referencia de la API de XML contiene para los servicios de detección automática proporcionados por Exchange. Las APIs Autodiscover proporcionan información de aprovisionamiento a las aplicaciones cliente que les permite detectar automáticamente los extremos de servicio de Exchange. 
    
- [Mensajería unificada de referencia de servicio web para Exchange](unified-messaging-web-service-reference-for-exchange.md) : contiene la referencia de API de XML para el servicio web de mensajería unificada (UM). El servicio web de mensajería unificada proporciona a las aplicaciones cliente tener acceso a la funcionalidad de mensajería unificada de Exchange. Tenga en cuenta que EWS también proporciona funcionalidad de mensajería unificada. 
    
- [EWS genera modelos de objetos para Exchange](http://msdn.microsoft.com/library/67d7d831-9c53-46da-80e4-18f562e71284%28Office.15%29.aspx) : contiene la referencia de API para las clases de proxy generado automáticamente en el espacio de nombres ExchangeWebServices. 
    
    > [!NOTE]
    > Para los clientes que se basan en versiones de .NET Framework a partir con .NET Framework 3.5, se recomienda que utilice la API administrada de EWS para tener acceso a EWS. Para obtener más información, vea [Introducción a las aplicaciones cliente de API administrada de EWS](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx). 
  
Para obtener información acerca de qué conjunto de API usar, vea [información general sobre el diseño de cliente EWS para Exchange](http://msdn.microsoft.com/library/b26f67aa-7c66-4d7d-98b3-746f26ab37f4%28Office.15%29.aspx).
  
La referencia de XML de Exchange se basa en las instancias XML que se envían entre el cliente y el servidor. El código XML se describe en los archivos WSDL y XSD para los servicios de EWS y detección automática de SOAP. El servicio web de mensajería unificada y el servicio Detección automática POX no tienen archivos publicados de WSDL y el esquema que describe su estructura. La referencia XML para los servicios que no tienen archivos de esquema se basa en las instancias XML que se pueden observar y capturadas mientras se intercambian entre el cliente y el servicio.
  
## <a name="see-also"></a>Ver también

- [Explore la API administrada de EWS, EWS y servicios web de Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [Empezar a utilizar servicios web de Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
- [Detección automática de Exchange](../exchange-web-services/autodiscover-for-exchange.md)
    

