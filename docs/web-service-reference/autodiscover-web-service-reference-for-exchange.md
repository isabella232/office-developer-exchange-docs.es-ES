---
title: Referencia del servicio web de Detección automática para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a01124a8-a8cf-4b80-8625-d7ee05690bca
description: Busque contenido de referencia para el servicio Web de detección automática en Exchange.
ms.openlocfilehash: ce7f2bbd662a5e61959c7e3c6748f0cf40cc4fb3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466874"
---
# <a name="autodiscover-web-service-reference-for-exchange"></a>Referencia del servicio web de Detección automática para Exchange

Busque contenido de referencia para el servicio Web de detección automática en Exchange.
  
El servicio Web de detección automática proporciona la información de configuración que la aplicación usa para crear una conexión a un servidor de Exchange. Puede usar una de las siguientes opciones para conectarse a detección automática:
  
- Servicio Detección automática de SOAP: disponible para los clientes que se conectan a las versiones de Exchange a partir de Exchange 2010, incluido Exchange Online.
    
- el servicio Detección automática "XML antiguo" (POX), disponible para los clientes que se conectan a las versiones de Exchange a partir de Exchange 2007, incluido Exchange Online. 
    
El servicio Detección automática de POX y SOAP puede proporcionar la información de configuración que el cliente usará para crear una conexión a un servidor de Exchange.
  
> [!NOTE]
> Para las versiones de Exchange a partir de Exchange 2010, se recomienda usar el servicio Detección automática de SOAP en lugar del servicio Detección automática de POX. El servicio Detección automática de SOAP proporciona solicitudes de configuración de detección automática por lotes y un control más granular sobre la configuración que se devuelve en la respuesta. 
  
Esta sección contiene información de referencia para el servicio Detección automática de SOAP y el servicio Detección automática de POX.
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_InThisSection"> </a>

- [Referencia del servicio Web de detección automática de SOAP para Exchange](soap-autodiscover-web-service-reference-for-exchange.md)
    
- [Referencia de servicio Web de detección automática de POX para Exchange](pox-autodiscover-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a>Vea también

- [Referencia de servicios web para Exchange](web-services-reference-for-exchange.md)
- [Servicio Detección automática (SOAP)](https://msdn.microsoft.com/library/e24d1a1f-0d20-4bd9-ae4c-9112ecacea78%28Office.15%29.aspx)
- [Servicio Detección automática (POX)](https://msdn.microsoft.com/library/13c54de3-a91c-4424-8732-99dd8f2162ec%28Office.15%29.aspx)
    

