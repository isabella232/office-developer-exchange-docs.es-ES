---
title: Referencia del servicio web de Detección automática para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: a01124a8-a8cf-4b80-8625-d7ee05690bca
description: Busque contenido de referencia para el servicio web de detección automática en Exchange.
ms.openlocfilehash: 3ef8760e077e54bbbe62cf580db53dd8f1931e33
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516107"
---
# <a name="autodiscover-web-service-reference-for-exchange"></a>Referencia del servicio web de Detección automática para Exchange

Busque contenido de referencia para el servicio web de detección automática en Exchange.
  
El servicio web de detección automática proporciona la información de configuración que la aplicación usa para crear una conexión a un Exchange servidor. Puede usar una de las siguientes opciones para conectarse a Detección automática:
  
- Servicio de detección automática SOAP: disponible para clientes que se conectan a versiones de Exchange a partir de Exchange 2010, incluidos Exchange Online.
    
- Servicio de detección automática "XML antiguo sin formato" (POX): disponible para clientes que se conectan a versiones de Exchange a partir de Exchange 2007, incluido Exchange Online. 
    
Tanto EL SOAP como el servicio de detección automática pox pueden proporcionar la información de configuración que el cliente usará para crear una conexión a un servidor Exchange usuario.
  
> [!NOTE]
> Para las versiones de Exchange a partir de Exchange 2010, se recomienda usar el servicio de detección automática SOAP en lugar del servicio de detección automática pox. El servicio de detección automática SOAP proporciona solicitudes de configuración de detección automática por lotes y un control más detallado sobre qué opciones se devuelven en la respuesta. 
  
Esta sección contiene información de referencia para el servicio de detección automática SOAP y el servicio de detección automática POX.
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_InThisSection"> </a>

- [Referencia de servicio web de detección automática SOAP para Exchange](soap-autodiscover-web-service-reference-for-exchange.md)
    
- [Referencia del servicio web de detección automática de POX para Exchange](pox-autodiscover-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a>Vea también

- [Referencia de servicios web para Exchange](web-services-reference-for-exchange.md)
- [Servicio de detección automática (SOAP)](https://msdn.microsoft.com/library/e24d1a1f-0d20-4bd9-ae4c-9112ecacea78%28Office.15%29.aspx)
- [Servicio de detección automática (POX)](https://msdn.microsoft.com/library/13c54de3-a91c-4424-8732-99dd8f2162ec%28Office.15%29.aspx)
    

