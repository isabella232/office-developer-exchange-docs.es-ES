---
title: Disponibilidad de características de API de servicio web en Exchange y la API administrada ews
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 07d3e6e8-d549-4ad7-baa4-bc531dfb7dd2
description: Obtenga información sobre qué características de EWS y API de servicio web están disponibles en cada versión de Exchange y la API administrada de EWS.
ms.openlocfilehash: 6fc0c40410be543b149885c7b0785a2c6c8828af
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544475"
---
# <a name="web-service-api-feature-availability-in-exchange-and-the-ews-managed-api"></a>Disponibilidad de características de API de servicio web en Exchange y la API administrada ews

Obtenga información sobre qué características de EWS y API de servicio web están disponibles en cada versión de Exchange y la API administrada de EWS.
  
Exchange aplicaciones cliente suelen dirigirse a muchas versiones de Exchange. Por este motivo, es posible que desee diseñar la aplicación de forma que pueda activar y desactivar las características del cliente [EWS](ews-client-design-overview-for-exchange.md#EWSFeatures) en función de la versión de Exchange que hospeda el buzón de los usuarios. En este artículo se proporciona información sobre las características de la API de servicio disponibles en diferentes versiones de Exchange y la API administrada de EWS. Use esta información para diseñar la aplicación para aplicarla ampliamente a los clientes que ejecutan varias versiones de Exchange. 
  
Para obtener información detallada sobre las diferencias entre las versiones de Exchange, revise los archivos de esquema EWS y la documentación [de referencia asociada.](https://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx)
  
## <a name="api-features-by-exchange-version"></a>Características de api por Exchange versión
<a name="bk_apifeatures"> </a>

Las EXCHANGE de servicio web, incluidas EWS y Detección automática, se desarrollan pensando en la compatibilidad con varias versiones. Por lo tanto, una aplicación dirigida Exchange 2007 también funciona con versiones de Exchange a partir de Exchange 2013, incluidos Exchange Online y Exchange Online como parte de Office 365. 
  
La tabla siguiente indica qué características de API están disponibles en cada versión de Exchange y versiones de la API administrada ews a partir de la versión 2.0. Dado que la aplicación puede tener como destino varias versiones de Exchange, le será útil saber qué versiones admiten las características que implementa el cliente. Puede usar el servicio de detección automática para descubrir qué versión de Exchange un cliente está dirigida para un usuario de modo que pueda activar y desactivar las características en función de si están disponibles para los usuarios.
  
**Tabla 1. Disponibilidad de características de servicio web en versiones de Exchange y la API administrada de EWS**

|Característica api|Exchange Online (Office 365)|API administrada EWS|Exchange 2013|Exchange 2010 SP2|Exchange 2010 SP1|Exchange 2010|Exchange 2007 SP1|Exchange 2007|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Resolución de nombres ambiguos  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Aplicaciones para administración Outlook aplicaciones  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[Acceso al buzón de archivo](archiving-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[Detección automática (POX)](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Detección automática (SOAP)](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Respuestas automáticas (OOF)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Disponibilidad  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Disponibilidad (salas)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Transferencia masiva  <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> ||||
|Grupos de contactos  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Administración de conversaciones  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Precisión de DateTime  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|Administración de delegados  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Expansión de listas de distribución  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Acceso al contenedor](deleting-items-by-using-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[eDiscovery](ediscovery-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|Zonas horarias mejoradas  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Permisos de carpeta  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Conversión de identificadores](ews-identifiers-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Administración de la Bandeja de entrada](inbox-management-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[Acceso a elementos y carpetas](folders-and-items-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Eventos de buzón de correo (extracción y inserción)](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Eventos de buzón (streaming)](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Sugerencias de correo  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Expiración de contraseña  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|[Personas](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|Publicar elementos  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Acceso a carpetas públicas](public-folder-access-with-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Directivas de retención  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[Búsqueda (indizada)](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Búsqueda (tienda)](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Sincronización](mailbox-synchronization-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Almacén de contactos unificado](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|[Servicio web de mensajería unificada](https://msdn.microsoft.com/library/83afea8a-c716-41df-9eb2-e1000357afb6%28Office.15%29.aspx) <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Mensajería unificada (basada en EWS)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Objetos de configuración de usuario](persistent-application-settings-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Fotos de usuario](how-to-get-user-photos-by-using-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
   
Encontrará más información sobre las características del servicio web que están disponibles en diferentes versiones de Exchange leyendo sobre las operaciones [EWS,](https://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx)el servicio [de](https://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)detección automática y los métodos [ExchangeService](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice_methods%28v=exchg.80%29.aspx).
  
## <a name="to-learn-more"></a>Para obtener más información
<a name="bk_apifeatures"> </a>

Si desea profundizar para comprender las diferencias específicas entre Exchange versiones, puede hacer cualquiera de las siguientes acciones:
  
- Explore el [esquema EWS para](https://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx) investigar las diferencias entre cada versión de EWS con más detalle. 
    
- Descargar [EWSEditor](http://ewseditor.codeplex.com/). Puede usar EWSEditor para especificar diferentes versiones de esquema de destino y enviar consultas en función de la versión del esquema de destino.
    
## <a name="see-also"></a>Consulte también

- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)   
- [Empezar a trabajar con aplicaciones de cliente de la API administrada de EWS](get-started-with-ews-managed-api-client-applications.md) 
- [Novedades de EWS y otros servicios web en Exchange](whats-new-in-ews-and-other-web-services-in-exchange.md)
    

