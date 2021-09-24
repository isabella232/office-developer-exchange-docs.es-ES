---
title: Función EWS en versiones de producto de Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 186c51dc-ec33-4a5d-b739-c9fcb1d4cdd3
description: EWS implementa nuevas funciones en las nuevas versiones de productos. Use la información de este artículo para determinar si la versión de Exchange de destino incluye compatibilidad con los datos o características a los que necesita tener acceso.
ms.openlocfilehash: bccd0e84fc28f8a7366f0463e555cceec71aa181
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512291"
---
# <a name="ews-functionality-in-exchange-product-versions"></a>Función EWS en versiones de producto de Exchange

EWS implementa nuevas funciones en las nuevas versiones de productos. Use la información de este artículo para determinar si la versión de Exchange de destino incluye compatibilidad con los datos o características a los que necesita tener acceso. 
  
En la tabla siguiente se enumeran las versiones de Exchange que incluyen EWS y las características principales que se introdujeron en cada versión.
  
## <a name="ews-features-by-product-version"></a>Características de EWS por versión de producto

|**Versión del producto**|**Funciones**|
|:-----|:-----|
|Office 365 y Exchange Online |Incluye todas las características de la versión actual de Exchange además de las nuevas características que se agregan para clientes en línea.  |
|Exchange 2013 SP1 | Incluye todas las características introducidas en Exchange 2013. Las siguientes características se introdujeron en Exchange 2013 SP1:<ul><li>Las confirmaciones de lectura ahora se pueden suspender para actualizaciones y eliminaciones.</li><li>Puede obtener información [de aprobación de transporte](https://msdn.microsoft.com/library/43a89f71-8002-4cb0-b3c8-1c2b2597f227%28Office.15%29.aspx) moderado.</li><li>Se pueden ver las respuestas de votación.</li><li>El [método SetHoldOnMailboxes](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx) y [la operación SetHoldOnMailboxes](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) aceptan todos los parámetros de un solo objeto.</li><li>Las búsquedas de exhibición de documentos electrónicos pueden especificar un idioma para las consultas de búsqueda y un formato específico de la referencia cultural para los intervalos de fechas.</li><li>El [objeto StreamingSubscriptionConnection](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection%28v=exchg.80%29.aspx) ahora puede tener acceso a los [objetos StreamingSubscription.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.streamingsubscription%28v=exchg.80%29.aspx)</li><li>Las conversaciones tienen una configuración para indicar si contienen mensajes de correo electrónico protegidos por IRM.</li><li>Los asistentes a la reunión pueden proponer nuevas horas de inicio y finalización para las reuniones e incluirlas en su respuesta a la reunión.</li><li>El método [GetUserSettings](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx) de detección automática SOAP ahora devuelve la configuración [GroupingInformation](https://msdn.microsoft.com/library/office/dn529149%28v=exchg.150%29.aspx) que se usa para mantener la afinidad de una suscripción a varios eventos de buzón de correo.</li></ul> |
|Exchange 2013  | Incluye todas las características introducidas en Exchange 2010 SP2. Las siguientes características se introdujeron en Exchange 2013:  <ul><li>  Archivado</li><li>eDiscovery</li><li>Personas</li><li>Directivas de retención</li><li>Almacén de contactos unificado</li><li>Fotos de usuario</li></ul> |
|Exchange 2010 SP2  | Incluye todas las características introducidas en Exchange 2010 SP1. Las siguientes características se introdujeron en Exchange 2010 SP2:  <ul><li>  Obtener expiración de contraseña</li><li>Precisión de DateTime</li><li>Identificadores de propiedad actualizados para contactos</li><li>Nuevos escenarios de suplantación</li></ul> |
|Exchange 2010 SP1  | Incluye todas las características introducidas en Exchange 2010. Las siguientes características se introdujeron en Exchange 2010 SP1:  <ul><li>  Crear, recuperar y modificar reglas de la Bandeja de entrada</li><li>Acceso mediante programación al buzón de archivo</li><li>Acciones de conversaciones</li><li>Notificaciones de recorrido de firewall</li><li>Características de administración mejoradas</li><li>Compatibilidad con versiones mixtas mejoradas</li><li>Compatibilidad con protección de limitación</li><li>Control del acceso de aplicaciones a EWS</li><li>Compatibilidad con autenticación de certificados de cliente</li></ul> |
|Exchange 2010  | Incluye todas las características introducidas en Exchange 2007 SP1. Las siguientes características se introdujeron en la versión de lanzamiento inicial de Exchange 2010: <ul> <li>  Lista de distribución privada completa</li><li>Objetos de configuración de usuario</li><li>Elementos asociados a carpetas</li><li>Seguimiento de mensajes</li><li>Mensajería unificada</li><li>Detección automática de SOAP  </li><li>Compatibilidad con zona horaria mejorada</li><li>Información de disponibilidad de recursos de sala</li><li>Búsqueda indizada</li><li>Acceso al contenedor</li><li>Información sobre correo electrónico</li></ul> |
|Exchange 2007 SP1  | Incluye todas las características introducidas en Exchange 2007. Las siguientes características se introdujeron en Exchange 2007 SP1:  <ul><li>  Administración de delegados</li><li>Permisos de carpeta</li><li>Carpetas públicas</li><li>Publicar elementos</li><li>Conversión de id.</li></ul> |
|Exchange 2007  | Las siguientes características se introdujeron en la versión de lanzamiento inicial de Exchange 2007:  <ul><li>  Acceso total a elementos, carpetas y datos adjuntos (Crear, Obtener, Actualizar, Eliminar)</li><li>Disponibilidad</li><li>Configuración fuera de Office configuración</li><li>Notificaciones</li><li>Sincronización</li><li>Resolución de nombres</li><li>Expansión de la lista de distribución (DL)</li><li>Búsqueda</li></ul> |
   
## <a name="see-also"></a>Vea también

- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)
- [Migrar a las tecnologías de Exchange](../migrating-to-exchange-online-and-exchange-2013-technologies.md)
- [Explorar la API administrada de EWS, EWS y servicios web en Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
    

