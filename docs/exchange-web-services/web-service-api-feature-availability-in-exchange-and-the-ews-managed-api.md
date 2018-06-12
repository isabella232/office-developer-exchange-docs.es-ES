---
title: Disponibilidad de característica del servicio Web de API de Exchange y la API administrada de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 07d3e6e8-d549-4ad7-baa4-bc531dfb7dd2
description: Obtenga información acerca de qué EWS y el servicio web están disponibles en cada versión de Exchange y la API administrada de EWS características de la API.
ms.openlocfilehash: d19ab062c8d418e373e8268b1ab039e5436e71bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763308"
---
# <a name="web-service-api-feature-availability-in-exchange-and-the-ews-managed-api"></a>Disponibilidad de característica del servicio Web de API de Exchange y la API administrada de EWS

Obtenga información acerca de qué EWS y el servicio web están disponibles en cada versión de Exchange y la API administrada de EWS características de la API.
  
Las aplicaciones de cliente de Exchange de destino a menudo muchas versiones de Exchange. Por este motivo, es posible que desee diseñar su aplicación de tal forma que se puede activar [las características de cliente EWS](ews-client-design-overview-for-exchange.md#EWSFeatures) y desactivar en función de la versión de Exchange que hospeda el buzón de correo de los usuarios. En este artículo se proporciona información acerca de qué características de la API de servicio están disponibles en las diferentes versiones de Exchange y la API administrada de EWS. Use esta información para diseñar su aplicación para que se aplican ampliamente a los clientes que ejecutan varias versiones de Exchange. 
  
Para obtener información detallada acerca de las diferencias entre las versiones de Exchange, revise los archivos de esquema EWS y la [documentación de referencia de](http://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx)la asociada.
  
## <a name="api-features-by-exchange-version"></a>Características de la API por versión de Exchange
<a name="bk_apifeatures"> </a>

El servicio web de Exchange API, incluidos EWS y detección automática, se desarrollan con la compatibilidad de versión múltiples en mente. Por lo tanto, una aplicación que se dirige a Exchange 2007 también funciona con las versiones de Exchange a partir de Exchange 2013, incluido Exchange Online y Exchange Online como parte de Office 365. 
  
En la siguiente tabla se indica qué características de la API están disponibles en cada versión de Exchange y las versiones de la API administrada de EWS empezando con la versión 2.0. Debido a que es posible que la aplicación como destino varias versiones de Exchange, será útil saber qué versiones admiten las características que implementa su cliente. Puede usar el servicio Detección automática para detectar la versión de Exchange se dirige a un cliente de un usuario para que puede activar y desactivar características dependiendo de si están disponibles para los usuarios.
  
**La tabla 1. Disponibilidad de funciones de servicio de Web en las versiones de Exchange y la API administrada de EWS**

|Característica de API|Exchange Online (Office 365)|API administrada EWS|Exchange 2013|Exchange 2010 SP2|Exchange 2010 SP1|Exchange 2010|Exchange 2007 SP1|Exchange 2007|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Resolución de nombres ambiguos  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Aplicaciones para la administración de Outlook  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[Acceso al buzón de archivo](archiving-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[Detección automática (POX)](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Detección automática (SOAP)](autodiscover-for-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Respuestas automáticas (OOF)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Disponibilidad  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Disponibilidad (salones)  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Transferencia masiva  <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> ||||
|Grupos de contactos  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Administración de conversaciones  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Precisión de fecha y hora  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|Delegar la administración  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Expansión de la lista de distribución  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Acceso de volcado de archivos](deleting-items-by-using-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[exhibición de documentos electrónicos](ediscovery-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|Zonas horarias mejoradas  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|Permisos de carpeta  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Conversión de identificador](ews-identifiers-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Administración de la Bandeja de entrada](inbox-management-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|[Acceso a elementos y carpetas](folders-and-items-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Eventos de buzón de correo (extracción e inserción)](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Eventos de buzón de correo (transmisión por secuencias)](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Sugerencias de correo electrónico  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||||
|Expiración de contraseña  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||||
|[Roles](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|Elementos para exponer  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|[Acceso a carpetas públicas](public-folder-access-with-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Directivas de retención  <br/> |X  <br/> |X  <br/> |X  <br/> ||||||
|[Búsqueda (indizado)](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Búsqueda (almacén)](search-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Sincronización](mailbox-synchronization-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Almacén de contactos unificados](people-and-contacts-in-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
|[Servicio Web de mensajería unificada](http://msdn.microsoft.com/library/83afea8a-c716-41df-9eb2-e1000357afb6%28Office.15%29.aspx) <br/> |X  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|(Basada en EWS) de mensajería unificada  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Objetos de configuración de usuario](persistent-application-settings-in-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Fotos de usuario](how-to-get-user-photos-by-using-ews-in-exchange.md) <br/> |X  <br/> ||X  <br/> ||||||
   
Puede encontrar más información acerca de la web de las características de servicio que están disponibles en las diferentes versiones de Exchange por lectura acerca de las [operaciones de EWS](http://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx), el [servicio de detección automática](http://msdn.microsoft.com/library/a01124a8-a8cf-4b80-8625-d7ee05690bca%28Office.15%29.aspx)y los [métodos de ExchangeService](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice_methods%28v=exchg.80%29.aspx).
  
## <a name="to-learn-more"></a>Para obtener más información
<a name="bk_apifeatures"> </a>

Si desea ir más allá para entender las diferencias entre las versiones de Exchange específicas, puede hacer cualquiera de las siguientes opciones:
  
- Explore el [esquema EWS](http://msdn.microsoft.com/library/6c969133-6036-448b-af39-a3caf9917e98%28Office.15%29.aspx) para investigar las diferencias entre cada versión de EWS con más detalle. 
    
- Descargar [EWSEditor](http://ewseditor.codeplex.com/). Puede usar EWSEditor para especificar las versiones de esquema de destino diferente y enviar consultas basadas en la versión del esquema de destino.
    
## <a name="see-also"></a>Ver también

- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)   
- [Empezar a trabajar con aplicaciones de cliente de la API administrada de EWS](get-started-with-ews-managed-api-client-applications.md) 
- [Novedades de EWS y otros servicios web de Exchange](whats-new-in-ews-and-other-web-services-in-exchange.md)
    

