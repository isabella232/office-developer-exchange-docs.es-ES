---
title: Versiones del esquema EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: d1ab6f9c-ea91-4022-830d-7f7b759e3935
description: Obtenga información sobre el esquema EWS y cómo diseñar la aplicación para que funcione con ella, así como las características que están disponibles con cada versión del esquema y cómo se relaciona el esquema con la versión del servicio de Exchange.
localization_priority: Priority
ms.openlocfilehash: 6afef658e747b11d9aa5fb7d7a88ba8f5c57ac82
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456017"
---
# <a name="ews-schema-versions-in-exchange"></a>Versiones del esquema EWS en Exchange

Obtenga información sobre el esquema EWS y cómo diseñar la aplicación para que funcione con ella, así como las características que están disponibles con cada versión del esquema y cómo se relaciona el esquema con la versión del servicio de Exchange.
  
El esquema EWS define las estructuras de datos que se pueden enviar y devolver por Exchange. Cada nueva versión de Exchange que contenga un cambio significativo en la funcionalidad de EWS contendrá un nuevo esquema. EWS y el esquema EWS están a la inversa y, en algunos casos, el reenvío de aplicaciones compatibles diseñadas para versiones anteriores de EWS funcionará, en la mayoría de los casos, con versiones posteriores de EWS y las aplicaciones destinadas a versiones posteriores de EWS funcionarán si la misma funcionalidad se incluyó en una versión anterior. Este artículo le ayudará a comprender el rol del esquema EWS, cómo funciona el control de versiones del esquema, la relación entre la versión del esquema y la versión del servicio, y cómo diseñar la aplicación para que funcione con el esquema EWS. 
  
## <a name="role-of-the-ews-schema"></a>Rol del esquema EWS

El esquema EWS hace lo siguiente:
  
- Define el conjunto de características que está disponible para un cliente. Un cliente puede obtener la lista de las versiones del esquema admitidas mediante el [servicio Detección automática](autodiscover-for-exchange.md)de SOAP. A continuación, el cliente puede determinar a qué características puede tener acceso, ya que cada versión del esquema representa un [conjunto de características de EWS](ews-schema-versions-in-exchange.md#bk_features). Cada nuevo esquema que se publica para EWS contiene las entidades de esquema de la versión anterior, además de las definiciones de esquema de cualquier nueva funcionalidad. De este modo, EWS admite aplicaciones destinadas a una versión anterior de EWS.
    
- Proporciona una descripción general del contrato de la API. Puede usar este contrato para determinar las estructuras de datos que se pueden enviar y recibir desde Exchange.
    
- Proporciona un mecanismo de control de versiones para enviar solicitudes. El servidor de Exchange contiene todas las versiones de esquema EWS compatibles en su directorio virtual. 
    
## <a name="designing-your-application-with-schema-version-in-mind"></a>Diseño de la aplicación teniendo en cuenta la versión de esquema

Tenga en cuenta los siguientes puntos a la vez que diseña la aplicación para que funcione con diferentes versiones del esquema EWS:
  
- Activa o desactiva la funcionalidad en función de la versión del esquema. Querrá asignar la funcionalidad del cliente a la versión del esquema y, en algunos casos, a la versión del servicio. En el siguiente ejemplo, se devuelve un [PropertySet](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) basado en la versión del esquema y el servicio. 
    
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

- Versión sus solicitudes con la versión más antigua del esquema EWS que admite la funcionalidad que desea usar. Esto hará que el cliente sea aplicable a un número mayor de servidores de Exchange potenciales. Esto es menos importante si está desarrollando una aplicación de línea de negocio solo para dirigirse a los servidores de la organización, pero es muy importante si está creando una aplicación para una audiencia de Exchange más amplia.
    
## <a name="features-by-schema-version"></a>Características por versión de esquema
<a name="bk_features"> </a>

Las versiones del esquema que están disponibles para un cliente se identifican en el tipo simple **ExchangeVersionType** ubicado en el esquema Types. xsd. El elemento [RequestServerVersion](https://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx) implementa **ExchangeVersionType** . El elemento **RequestServerVersion** se envía en todas las solicitudes EWS para indicar al servidor la versión del esquema a la que se destina el cliente. Esto, a su vez, identifica el conjunto de características que está disponible para el cliente. 
  
**Tabla 1: características de EWS por versión de producto y esquema**

|**Versión del producto**|**Versión de esquema asociada**|**Funciones**|
|:-----|:-----|:-----|
|Exchange Online  |La última versión del esquema.  |Incluye todas las características de la versión actual de Exchange además de las nuevas características que se agregan a los clientes en línea. |
|Exchange 2013 SP1 |Exchange2013_SP1 | Incluye todas las características de Exchange 2013.<br/><br/>Las siguientes características se introdujeron en Exchange 2013 SP1: <ul><li>[Directiva de retención de buzones](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx) </li><li> [Proponer nueva hora](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md) </li><li>  Actualizaciones de confirmación de lectura para [Actualizar](https://msdn.microsoft.com/library/office/dn600559%28v=exchg.80%29.aspx) y [eliminar](https://msdn.microsoft.com/library/office/dn600557%28v=exchg.80%29.aspx) elementos  </li><li> Actualización de [información de IRM](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.conversation.hasirm%28v=exchg.80%29.aspx) para conversaciones  </li></ul> |
|Exchange 2013   |Exchange2013   | Incluye todas las características incorporadas en Exchange 2007 y Exchange 2010. <br/><br/>Las siguientes características se introdujeron en Exchange 2013:<ul><li>Archivado  </li><li>  eDiscovery  </li><li>  Roles  </li><li>  Directivas de retención  </li><li>  Almacén de contactos unificado  </li><li>  Fotos de usuario  </li></ul> |
|Exchange 2010 SP2   |Exchange2010_SP2 | Incluye todas las características incorporadas en Exchange 2010 SP1. <br/><br/>Las siguientes características se introdujeron en Exchange 2010 SP2:<ul><li>Obtener expiración de contraseña  </li><li>  Precisión DateTime  </li><li>  Identificadores de propiedad actualizados para contactos  </li><li>  Nuevos escenarios de suplantación  </li></ul> |
|Exchange 2010 SP1  |Exchange2010_SP1   | Incluye todas las características incorporadas en Exchange 2010. <br/><br/>Las siguientes características se introdujeron en Exchange 2010 SP1:<ul><li>Crear, recuperar y modificar reglas de la bandeja de entrada  </li><li>  Acceso mediante programación al buzón de archivo  </li><li>  Acciones de conversaciones  </li><li>  Notificaciones de recorrido de Firewall  </li><li>  Características de administración mejoradas  </li><li>  Compatibilidad de versiones mixtas mejorada  </li><li>  Compatibilidad con la protección de limitación  </li><li>  Control del acceso de la aplicación a EWS  </li><li>  Compatibilidad con la autenticación de certificados de cliente  </li></ul> |
|Exchange 2010  |Exchange2010   | Incluye todas las características incorporadas en Exchange 2007 SP1. <br/><br/>Las siguientes características se introdujeron en la versión de lanzamiento inicial de Exchange 2010:<ul><li>Lista de distribución privada completa  </li><li>  Objetos de configuración de usuario  </li><li>  Elementos asociados a la carpeta  </li><li>  Seguimiento de mensajes  </li><li>  Mensajería unificada  </li><li>  Detección automática de SOAP  </li><li>  Compatibilidad mejorada de la zona horaria  </li><li>  Información de disponibilidad de recursos de sala  </li><li>  Búsqueda indizada  </li><li>  Acceso a la papelera  </li><li>  Información de sugerencias de correo  </li></ul> |
|Exchange 2007 SP1   |Exchange2007_SP1  | Incluye todas las características incorporadas en Exchange 2007. <br/><br/>Las siguientes características se introdujeron en Exchange 2007 SP1:<ul><li>Delegación de la administración  </li><li>  Permisos de carpeta  </li><li>  Carpetas públicas  </li><li>  Elementos para exponer  </li><li>  Conversión de IDENTIFICADOres  </li></ul>|
|Exchange 2007  |Exchange2007 | Las siguientes características se introdujeron en la versión de lanzamiento inicial de Exchange 2007:<ul><li>Acceso completo a elementos, carpetas y datos adjuntos (crear, obtener, actualizar, eliminar)  </li><li>  Disponibilidad  </li><li>  Configuración de fuera de la oficina  </li><li>  Notificaciones  </li><li>  Sincronización  </li><li>  Resolución de nombres  </li><li>  Expansión de la lista de distribución (DL)  </li><li>  Búsqueda  </li></ul> |
   
## <a name="relationship-between-the-ews-schema-and-the-service-version"></a>Relación entre el esquema EWS y la versión del servicio
<a name="bk_features"> </a>

La versión del esquema EWS está relacionada con la versión del servicio EWS que se está ejecutando en el servidor. El patrón de nomenclatura para el esquema EWS está relacionado con las versiones locales de Exchange. Por ejemplo, la versión inicial de Exchange 2013 tiene una versión de servicio de 15.00.0516.032 y el nombre de esquema **Exchange2013**. Debido a que el esquema se actualizó para Exchange 2013, tanto Exchange 2013 como Exchange Online con una versión de servicio de 15.00.0516.032 y versiones posteriores tienen el mismo nombre de versión para el último esquema. En versiones anteriores de Exchange, el esquema EWS no se actualizaba con las actualizaciones acumulativas (anteriormente conocidas como Rollup). Pero como Exchange se actualiza con más frecuencia para admitir Exchange Online, las actualizaciones acumulativas ahora contienen actualizaciones de esquema para EWS. Los nombres de archivo de esquema y el nombre de versión de esquema asociado solo se actualizan con Service Packs o versiones principales de Exchange local.
  
Mientras que el esquema EWS define el contrato, en algunos escenarios, la versión del servicio es la única forma de que un cliente determine cómo debe interactuar con el servicio. Los cambios de comportamiento del servicio que no se reflejan en el esquema solo pueden estar determinados por la versión del servicio devuelta en todas las respuestas de EWS. Por ejemplo, cuando se rediseñaron [carpetas públicas](public-folder-access-with-ews-in-exchange.md) en Exchange 2013, las operaciones que se usan para mover y copiar carpetas públicas han cambiado. Si ha diseñado un cliente para copiar carpetas públicas en Exchange 2010, deberá actualizarla para que use distintas operaciones para obtener el mismo resultado en Exchange 2013. 
  
## <a name="how-the-ews-schema-is-updated"></a>Cómo se actualiza el esquema EWS
<a name="bk_features"> </a>

Los servidores de Exchange que ejecutan versiones de Exchange a partir de Exchange 2007 incluyen el esquema EWS en el directorio virtual que hospeda el servicio EWS. La versión del esquema actual siempre está representada por los archivos Types. xsd y messages. xsd. La figura 1 muestra cómo se bifurca el esquema messages. xsd cuando se desarrolla una nueva versión del esquema. Antes de que se agregue nueva funcionalidad, se incluye una copia del esquema messages. xsd original que se cambia para representar la versión anterior del esquema. A continuación, el archivo messages. xsd se actualiza con la descripción del servicio de la nueva versión.
  
**Figura 1. Cómo se actualiza el esquema EWS**

![Ilustración que muestra cómo se actualiza el esquema de EWS. La última versión del esquema se bifurca y se le cambia el nombre para representar la versión anterior, y el último nombre de archivo representa la versión actual.](media/Ex15_EWS_Schema_Update1.png)
  
Antes de actualizar el esquema EWS para una nueva versión, la versión actual del esquema se bifurca y se cambia de nombre con la Convención siguiente:
  
`<schemaname>-<majorserverversion><servicepack>.xsd`
  
A continuación, el nombre del archivo original representa el último esquema. Todas las nuevas características se agregan al esquema más reciente, con la excepción de las actualizaciones y las correcciones de las versiones anteriores del esquema. 
  
## <a name="see-also"></a>Vea también

- [Versiones del esquema EWS en Exchange](ews-schema-versions-in-exchange.md) 
- [Detección automática en Exchange](autodiscover-for-exchange.md) 
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    

