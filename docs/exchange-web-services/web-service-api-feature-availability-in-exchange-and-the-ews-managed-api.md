---
title: Disponibilidad de características de API de servicio Web en Exchange y la API administrada de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07d3e6e8-d549-4ad7-baa4-bc531dfb7dd2
description: Obtenga información sobre qué características de la API de EWS y del servicio web están disponibles en cada versión de Exchange y la API administrada de EWS.
ms.openlocfilehash: f15cf4784a59c18d1bb9ae20af378baed084acc3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529850"
---
# <a name="web-service-api-feature-availability-in-exchange-and-the-ews-managed-api"></a>Disponibilidad de características de API de servicio Web en Exchange y la API administrada de EWS

Obtenga información sobre qué características de la API de EWS y del servicio web están disponibles en cada versión de Exchange y la API administrada de EWS.
  
Las aplicaciones cliente de Exchange a menudo se dirigen a muchas versiones de Exchange. Por esta razón, es posible que desee diseñar su aplicación de modo que pueda activar y desactivar [las características de cliente de EWS](ews-client-design-overview-for-exchange.md#EWSFeatures) en función de la versión de Exchange que hospeda el buzón de correo de los usuarios. En este artículo se proporciona información sobre las características de API de servicio que están disponibles en las diferentes versiones de Exchange y la API administrada de EWS. Use esta información para diseñar la aplicación para que se aplique en general a los clientes que ejecutan varias versiones de Exchange. 
  
Para obtener información detallada sobre las diferencias entre versiones de Exchange, revise los archivos de esquema EWS y la [documentación de referencia](https://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx)asociada.
  
## <a name="api-features-by-exchange-version"></a>Características de la API de la versión de Exchange
<a name="bk_apifeatures"> </a>

Las API de servicio Web de Exchange, incluidos EWS y detección automática, se desarrollan teniendo en cuenta la compatibilidad con varias versiones. Por lo tanto, una aplicación dirigida a Exchange 2007 también funciona con las versiones de Exchange a partir de Exchange 2013, incluidos Exchange Online y Exchange online como parte de Office 365. 
  
En la tabla siguiente se indican las características de la API disponibles en cada versión de Exchange y las versiones de la API administrada de EWS a partir de la versión 2,0. Como la aplicación puede dirigirse a varias versiones de Exchange, le será útil saber qué versiones son compatibles con las características que implementa el cliente. Puede usar el servicio de detección automática para detectar la versión de destino de Exchange de un usuario para que pueda activar y desactivar las características en función de si están disponibles para los usuarios.
  
**Tabla 1. Disponibilidad de la característica de servicio Web en las versiones de Exchange y la API administrada de EWS**

|Característica de la API|Exchange Online (Office 365)|API administrada EWS|Exchange 2013|Exchange 2010 SP2|Exchange 2010 SP1|Exchange 2010|Exchange 2007 SP1|Exchange 2007|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Resolución de nombres ambiguos  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Administración de aplicaciones para Outlook  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[Acceso al buzón de archivo](archiving-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[Detección automática (POX)](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Detección automática (SOAP)](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Respuestas automáticas (OOF)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Disponibilidad  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Disponibilidad (salas)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Transferencia masiva  <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> ||||
|Grupos de contactos  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Administración de conversaciones  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Precisión DateTime  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|Delegación de la administración  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Expansión de la lista de distribución  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Acceso a la papelera](deleting-items-by-using-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Exhibición de documentos electrónicos (eDiscovery)](ediscovery-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|Zonas horarias mejoradas  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Permisos de carpeta  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Conversión de identificadores](ews-identifiers-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Administración de la Bandeja de entrada](inbox-management-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[Acceso a elementos y carpetas](folders-and-items-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Eventos de buzón de correo (extracción e inserción)](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Eventos de buzón de correo (streaming)](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Compartir  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Expiración de contraseña  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|[Roles](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|Elementos para exponer  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Acceso a carpetas públicas](public-folder-access-with-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Directivas de retención  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[Búsqueda (indizada)](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Buscar (tienda)](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Sincronización](mailbox-synchronization-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Almacén de contactos unificado](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|[Servicio Web de mensajería unificada](https://msdn.microsoft.com/library/83afea8a-c716-41df-9eb2-e1000357afb6%28Office.15%29.aspx) <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Mensajería unificada (basada en EWS)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Objetos de configuración de usuario](persistent-application-settings-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Fotos de usuario](how-to-get-user-photos-by-using-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
   
Puede encontrar más información sobre las características del servicio Web que están disponibles en diferentes versiones de Exchange mediante la lectura de las [operaciones de EWS](https://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx), el servicio de [detección automática](https://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)y los [métodos de ExchangeService](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice_methods%28v=exchg.80%29.aspx).
  
## <a name="to-learn-more"></a>Para obtener más información
<a name="bk_apifeatures"> </a>

Si desea profundizar en la comprensión de las diferencias específicas entre versiones de Exchange, puede realizar una de las siguientes acciones:
  
- Explore el [esquema EWS](https://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx) para investigar las diferencias entre cada versión de EWS con más detalle. 
    
- Descargue [EWSEditor](http://ewseditor.codeplex.com/). Puede usar EWSEditor para especificar diferentes versiones de esquema de destino y enviar consultas basadas en la versión de esquema de destino.
    
## <a name="see-also"></a>Vea también

- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)   
- [Empezar a trabajar con aplicaciones de cliente de la API administrada de EWS](get-started-with-ews-managed-api-client-applications.md) 
- [Novedades de EWS y otros servicios Web de Exchange](whats-new-in-ews-and-other-web-services-in-exchange.md)
    

