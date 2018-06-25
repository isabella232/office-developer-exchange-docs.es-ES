---
title: Referencia de servicio web de detección automática para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a01124a8-a8cf-4b80-8625-d7ee05690bca
description: Buscar contenido de referencia para el servicio web de detección automática en Exchange.
ms.openlocfilehash: 48ca4a93c2120079cb675eabbc460bf0e75570b2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763590"
---
# <a name="autodiscover-web-service-reference-for-exchange"></a>Referencia de servicio web de detección automática para Exchange

Buscar contenido de referencia para el servicio web de detección automática en Exchange.
  
El servicio web de detección automática proporciona la información de configuración que la aplicación se usa para crear una conexión a un servidor de Exchange. Puede usar una de las siguientes opciones para conectarse a la detección automática:
  
- Servicio de detección automática SOAP: disponible para los clientes que se conectan a las versiones de Exchange a partir de Exchange 2010, incluido Exchange Online.
    
- "sin formato XML antiguo" servicio de detección automática (POX): disponible para los clientes que se conectan a las versiones de Exchange a partir de Exchange 2007, incluido Exchange Online. 
    
El mensaje SOAP y el servicio Detección automática POX pueden proporcionar la información de configuración que va a usar el cliente para crear una conexión a un servidor de Exchange.
  
> [!NOTE]
> Para las versiones de Exchange 2010 a partir de Exchange, se recomienda que use el servicio Detección automática de SOAP en lugar del servicio de detección automática de POX. El servicio de detección automática de SOAP proporciona solicitudes por lotes de configuración de detección automática y un mayor control sobre qué configuración se devuelve en la respuesta. 
  
Esta sección contiene información de referencia para el servicio Detección automática de SOAP y el servicio de detección automática de POX.
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_InThisSection"> </a>

- [Referencia de servicio web de detección automática de SOAP para Exchange](soap-autodiscover-web-service-reference-for-exchange.md)
    
- [Referencia de servicio web POX de detección automática de Exchange](pox-autodiscover-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a>Vea también

- [Referencia de servicios Web de Exchange](web-services-reference-for-exchange.md)
- [Servicio de detección automática (SOAP)](http://msdn.microsoft.com/library/e24d1a1f-0d20-4bd9-ae4c-9112ecacea78%28Office.15%29.aspx)
- [Servicio de detección automática (POX)](http://msdn.microsoft.com/library/13c54de3-a91c-4424-8732-99dd8f2162ec%28Office.15%29.aspx)
    

