---
title: Versiones de esquema EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d1ab6f9c-ea91-4022-830d-7f7b759e3935
description: Obtenga información sobre la dirección URL de EWS esquema y el diseño de la aplicación para que funcione con él, así como las características que están disponibles con cada versión del esquema y cómo se relaciona con el esquema a la versión de servicio de Exchange.
ms.openlocfilehash: dd8e85547666ba0bf3a1a38775260268594f2a8b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763018"
---
# <a name="ews-schema-versions-in-exchange"></a>Versiones de esquema EWS en Exchange

Obtenga información sobre la dirección URL de EWS esquema y el diseño de la aplicación para que funcione con él, así como las características que están disponibles con cada versión del esquema y cómo se relaciona con el esquema a la versión de servicio de Exchange.
  
El esquema EWS define las estructuras de datos que se pueden enviar a y devueltas por Exchange. Cada nueva versión de Exchange que contiene un cambio significativo a la funcionalidad EWS contendrá un nuevo esquema. EWS y el esquema EWS son ambos con versiones anteriores y en algunos casos, compatible con el reenvío - aplicaciones diseñadas para versiones anteriores de EWS funcionará, en la mayoría de los casos, con las versiones posteriores de EWS, y las aplicaciones que estén destinados a versiones posteriores de EWS funcionará si el mismo la funcionalidad se ha incluido en una versión anterior. En este artículo le ayudará a comprender la función del esquema EWS, cómo funciona el control de versiones de esquema, la relación entre la versión del esquema y la versión de servicio y el diseño de la aplicación para que funcione con el esquema EWS. 
  
## <a name="role-of-the-ews-schema"></a>Rol del esquema EWS

El esquema EWS hace lo siguiente:
  
- Define el conjunto de características que está disponible para un cliente. Un cliente puede obtener la lista de las versiones de esquema compatibles con el [servicio de detección automática](autodiscover-for-exchange.md)SOAP. El cliente, a continuación, puede determinar las características que puede obtener acceso, ya que cada versión del esquema representa un [conjunto de características EWS](ews-schema-versions-in-exchange.md#bk_features). Cada nuevo esquema publicado para EWS contiene las entidades de esquema de la versión anterior además de las definiciones de esquema para cualquier nueva funcionalidad. De este modo, EWS es compatible con las aplicaciones que estén destinados a una versión anterior de EWS.
    
- Proporciona una descripción general del contrato de API. Puede usar este contrato para determinar las estructuras de datos que se pueden enviar a y recibidas de Exchange.
    
- Proporciona un mecanismo de control de versiones para el envío de solicitudes. El servidor de Exchange contiene todas las versiones de esquema EWS compatibles en su directorio virtual. 
    
## <a name="designing-your-application-with-schema-version-in-mind"></a>Diseño de la aplicación con la versión del esquema en mente

Al diseñar su aplicación para que funcione con distintas versiones del esquema EWS, tenga en cuenta los puntos siguientes:
  
- Activar o desactivar la funcionalidad basada en la versión del esquema. Desea asignar la funcionalidad de cliente a la versión del esquema y, en algunos casos, a la versión del servicio. En el ejemplo siguiente, se devolverá que un [PropertySet](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) en función de la versión del esquema y de servicio. 
    
  ```cs
  private static PropertySet InitPropertySetByVersion(ExchangeService service)
  {
      PropertySet props;
      // The schema version to target to access the NormalizedBody property 
      // is Exchange2013 or later. The server version to target to access the 
      // NormalizedBody property on an email is 15 or later, which 
      // equates to Exchange 2013.
      if (service.RequestedServerVersion >= ExchangeVersion.Exchange2013 &amp;&amp;
          service.ServerInfo.MajorVersion >= 15)
      {
          props = new PropertySet(EmailMessageSchema.NormalizedBody);
      }
      else
      {
          props = new PropertySet(EmailMessageSchema.Body);
      }
      return props;
  }
  ```

- Versión de las solicitudes con la versión más antigua del esquema EWS que admite la funcionalidad que desea usar. Esto hará que el cliente aplicables a un número mayor de posibles servidores de Exchange. Esto es menos importante si está desarrollando una aplicación de línea de negocio a sólo los servidores de la organización de destino, pero es muy importante si va a crear una aplicación para un público más amplio de Exchange.
    
## <a name="features-by-schema-version"></a>Características por versión del esquema
<a name="bk_features"> </a>

Se identifican las versiones de esquema que están disponibles para un cliente en el tipo simple de **ExchangeVersionType** que se encuentra en el esquema de types.xsd. El **ExchangeVersionType** se implementa mediante el elemento [RequestServerVersion](http://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx) . El elemento **RequestServerVersion** se envía en todas las solicitudes EWS para indicar al servidor de la versión del esquema de los destinos de cliente. Esto identifica a su vez el conjunto de características que está disponible para el cliente. 
  
**Tabla 1: Características EWS por versión del producto y esquema**

|**Versión del producto**|**Versión del esquema asociado**|**Características**|
|:-----|:-----|:-----|
|Exchange Online  |La versión más reciente del esquema.  |Incluye todas las características de la versión actual de Exchange, además de todas las características nuevas que se agregan para los clientes en línea. |
|Exchange 2013 SP1 |Exchange2013_SP1 | Incluye todas las características de Exchange 2013.<br/><br/>Las siguientes características se introdujeron en Exchange 2013 SP1: <ul><li>[Directiva de retención de buzón de correo](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx) </li><li> [Proponer una nueva hora](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md) </li><li>  Actualizaciones de confirmación de [actualización](http://msdn.microsoft.com/EN-US/library/office/dn600559%28v=exchg.80%29.aspx) y [eliminación de](http://msdn.microsoft.com/EN-US/library/office/dn600557%28v=exchg.80%29.aspx) elementos de lectura  </li><li> Actualización de la [información de IRM](http://msdn.microsoft.com/EN-US/library/office/microsoft.exchange.webservices.data.conversation.hasirm%28v=exchg.80%29.aspx) para las conversaciones  </li></ul> |
|Exchange 2013   |Exchange2013   | Incluye todas las características introducidas en Exchange 2007 y Exchange 2010. <br/><br/>Las siguientes características se introdujeron en Exchange 2013:<ul><li>Archivado  </li><li>  eDiscovery  </li><li>  Personas  </li><li>  Directivas de retención  </li><li>  Almacén de contactos unificados  </li><li>  Fotos de usuario  </li></ul> |
|Exchange 2010 SP2   |Exchange2010_SP2 | Incluye todas las características introducidas en Exchange 2010 SP1. <br/><br/>Las siguientes características se introdujeron en Exchange 2010 SP2:<ul><li>Obtener la expiración de contraseña  </li><li>  Precisión de fecha y hora  </li><li>  Identificadores de propiedad actualizada para los contactos  </li><li>  Nuevos escenarios de suplantación  </li></ul> |
|Exchange 2010 SP1  |Exchange2010_SP1   | Incluye todas las características introducidas en Exchange 2010. <br/><br/>Las siguientes características se introdujeron en Exchange 2010 SP1:<ul><li>Crear, recuperar y modificar las reglas de bandeja de entrada  </li><li>  Acceso mediante programación a buzón de archivo  </li><li>  Acciones de conversaciones  </li><li>  Recorrido de las notificaciones del Firewall  </li><li>  Características de administración mejoradas  </li><li>  Compatibilidad de versión mixta mejorada  </li><li>  Limitación de peticiones de soporte técnico de protección  </li><li>  Control de acceso de la aplicación a EWS  </li><li>  Compatibilidad con la autenticación de certificado de cliente  </li></ul> |
|Exchange 2010  |Exchange2010   | Incluye todas las características introducidas en Exchange 2007 SP1. <br/><br/>Las siguientes características se introdujeron en la versión inicial de Exchange 2010:<ul><li>Lista de distribución privada completa  </li><li>  Objetos de configuración de usuario  </li><li>  Carpeta elementos asociados  </li><li>  Seguimiento de mensajes  </li><li>  Mensajería unificada  </li><li>  Detección automática de SOAP  </li><li>  Compatibilidad mejorada con la zona horaria  </li><li>  Información de disponibilidad de recursos de sala  </li><li>  Búsqueda indizado  </li><li>  Acceso de volcado de archivos  </li><li>  Información de sugerencias de correo electrónico  </li></ul> |
|Exchange 2007 SP1   |Exchange2007_SP1  | Incluye todas las características introducidas en Exchange 2007. <br/><br/>Las siguientes características se introdujeron en Exchange 2007 SP1:<ul><li>Delegar la administración  </li><li>  Permisos de carpeta  </li><li>  Carpetas públicas  </li><li>  Elementos para exponer  </li><li>  Conversión de Id.  </li></ul>|
|Exchange 2007  |Exchange2007 | Las siguientes características se introdujeron en la versión inicial de Exchange 2007:<ul><li>Acceso total a los elementos, carpetas y datos adjuntos (crear, Get, Update, Delete)  </li><li>  Disponibilidad  </li><li>  Fuera de la configuración de Office  </li><li>  Notificaciones  </li><li>  Sincronización  </li><li>  Resolución de nombres  </li><li>  Expansión de distribución (DL) de la lista  </li><li>  B?squeda  </li></ul> |
   
## <a name="relationship-between-the-ews-schema-and-the-service-version"></a>Relación entre el esquema de EWS y la versión de servicio
<a name="bk_features"> </a>

La versión del esquema EWS está relacionada con la versión del servicio de EWS que ejecuta el servidor. El modelo de nomenclatura para el esquema EWS está relacionada con las versiones locales de Exchange. Por ejemplo, la versión inicial de Exchange 2013 tiene una versión de servicio de 15.00.0516.032 y el nombre de esquema **Exchange2013**. Debido a que el esquema se ha actualizado para Exchange 2013, Exchange 2013 y Exchange Online con una versión de servicio de 15.00.0516.032 y versiones posteriores tienen el mismo nombre de la versión para el esquema más reciente. En versiones anteriores de Exchange, el esquema EWS no se actualizó con actualizaciones acumulativas (anteriormente denominado paquetes acumulativos de actualizaciones). Pero, debido a que Exchange se actualiza con más frecuencia para admitir Exchange Online, actualizaciones acumulativas ahora contienen las actualizaciones del esquema de EWS. Los nombres de archivo de esquema y el nombre de la versión de esquema asociado, sólo se actualizan con service Pack o las versiones principales de Exchange local.
  
Mientras que el esquema EWS define el contrato, en algunos casos, la versión de servicio es la única forma para que un cliente determinar cómo debe para interactuar con el servicio. Sólo se pueden determinar los cambios de comportamiento de servicio que no se reflejen en el esquema de la versión de servicio devuelto en todas las respuestas EWS. Por ejemplo, cuando se han vuelto a diseñar [las carpetas públicas](public-folder-access-with-ews-in-exchange.md) en Exchange 2013, las operaciones que se usan para mover y copiar carpetas públicas ha cambiado. Si ha diseñado un cliente para copiar las carpetas públicas en Exchange 2010, necesitará actualizar para usar diferentes operaciones para obtener el mismo resultado en Exchange 2013. 
  
## <a name="how-the-ews-schema-is-updated"></a>¿Cómo se actualiza el esquema EWS
<a name="bk_features"> </a>

Servidores de Exchange que ejecutan versiones de Exchange 2007 a partir de Exchange incluyen el esquema EWS en el directorio virtual que hospeda el servicio EWS. La versión actual del esquema siempre está representada por los archivos types.xsd y messages.xsd. La figura 1 muestra cómo se bifurca el esquema messages.xsd cuando se ha desarrollado una nueva versión del esquema. Antes de agrega la nueva funcionalidad, una copia del esquema messages.xsd original se incluyen y nombre se ha cambiado para representar la versión anterior del esquema. El archivo messages.xsd, a continuación, se actualiza con la descripción del servicio para la nueva versión.
  
**En la figura 1. ¿Cómo se actualiza el esquema EWS**

![Ilustración que muestra cómo se actualiza el esquema de EWS. La última versión del esquema se bifurca y se le cambia el nombre para representar la versión anterior, y el último nombre de archivo representa la versión actual.](media/Ex15_EWS_Schema_Update1.png)
  
Antes de actualiza el esquema EWS para una nueva versión, la versión actual del esquema se bifurca y nombre se ha cambiado con la siguiente convención:
  
`<schemaname>-<majorserverversion><servicepack>.xsd`
  
El nombre del archivo original, a continuación, representa el esquema más reciente. Todas las características nuevas se agregan al esquema más reciente, con la excepción de las actualizaciones y revisiones a las versiones anteriores del esquema. 
  
## <a name="see-also"></a>Vea también

- [Versiones de esquema EWS en Exchange](ews-schema-versions-in-exchange.md) 
- [Detección automática de Exchange](autodiscover-for-exchange.md) 
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    

