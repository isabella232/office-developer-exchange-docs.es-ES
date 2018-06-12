---
title: Funcionalidad EWS en versiones de producto de Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 186c51dc-ec33-4a5d-b739-c9fcb1d4cdd3
description: EWS implementa la nueva funcionalidad en nuevas versiones de productos. Use la información de este artículo para determinar si la versión de Exchange que posea incluye compatibilidad con los datos o las características que necesitan tener acceso a.
ms.openlocfilehash: 6b676781f25eeeb90fd9ab075fbe63198766bd99
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763005"
---
# <a name="ews-functionality-in-exchange-product-versions"></a>Funcionalidad EWS en versiones de producto de Exchange

EWS implementa la nueva funcionalidad en nuevas versiones de productos. Use la información de este artículo para determinar si la versión de Exchange que posea incluye compatibilidad con los datos o las características que necesitan tener acceso a. 
  
En la siguiente tabla se enumera las versiones de Exchange que incluyan EWS y las características principales que se introdujeron en cada versión.
  
## <a name="ews-features-by-product-version"></a>Características EWS por versión del producto

|**Versión del producto**|**Características**|
|:-----|:-----|
|Office 365 y Exchange Online |Incluye todas las características de la versión actual de Exchange, además de todas las características nuevas que se agregan para los clientes en línea.  |
|Exchange 2013 SP1 | Incluye todas las características que se introdujo en Exchange 2013. Las siguientes características se introdujeron en Exchange 2013 SP1:<ul><li>Ahora se pueden suspender las confirmaciones de lectura para las actualizaciones y eliminaciones.</li><li>Puede obtener información de aprobación [moderan transporte](http://msdn.microsoft.com/library/43a89f71-8002-4cb0-b3c8-1c2b2597f227%28Office.15%29.aspx) .</li><li>Las respuestas de votación se puede ver.</li><li>El método [SetHoldOnMailboxes](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx) y [SetHoldOnMailboxes](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) operación aceptan todos los parámetros en un solo objeto.</li><li>las búsquedas de exhibición de documentos electrónicos pueden especificar un idioma para las consultas de búsqueda y un formato específico de referencia cultural para los intervalos de fecha.</li><li>El objeto [StreamingSubscriptionConnection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscriptionconnection%28v=exchg.80%29.aspx) ahora puede tener acceso a los objetos [StreamingSubscription](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.streamingsubscription%28v=exchg.80%29.aspx) .</li><li>Las conversaciones de tengan una opción para indicar si contienen mensajes de correo electrónico que están protegidos por IRM.</li><li>Los asistentes de la reunión puede proponer nuevas horas de inicio y final para las reuniones e incluirlos en su respuesta a la reunión.</li><li>El método de detección automática de SOAP [GetUserSettings](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.getusersettings%28v=exchg.80%29.aspx) ahora devuelve el [GroupingInformation](http://msdn.microsoft.com/EN-US/library/office/dn529149%28v=exchg.150%29.aspx) configuración que se usa mantener la afinidad para una suscripción a varios eventos de buzón de correo.</li></ul> |
|Exchange 2013  | Incluye todas las características introducidas en Exchange 2010 SP2. Las siguientes características se introdujeron en Exchange 2013:  <ul><li>  Archivado</li><li>eDiscovery</li><li>Personas</li><li>Directivas de retención</li><li>Almacén de contactos unificados</li><li>Fotos de usuario</li></ul> |
|Exchange 2010 SP2  | Incluye todas las características introducidas en Exchange 2010 SP1. Las siguientes características se introdujeron en Exchange 2010 SP2:  <ul><li>  Obtener la expiración de contraseña</li><li>Precisión de fecha y hora</li><li>Identificadores de propiedad actualizada para los contactos</li><li>Nuevos escenarios de suplantación</li></ul> |
|Exchange 2010 SP1  | Incluye todas las características introducidas en Exchange 2010. Las siguientes características se introdujeron en Exchange 2010 SP1:  <ul><li>  Crear, recuperar y modificar las reglas de bandeja de entrada</li><li>Acceso mediante programación a buzón de archivo</li><li>Acciones de conversaciones</li><li>Recorrido de las notificaciones del Firewall</li><li>Características de administración mejoradas</li><li>Compatibilidad de versión mixta mejorada</li><li>Limitación de peticiones de soporte técnico de protección</li><li>Control de acceso de la aplicación a EWS</li><li>Compatibilidad con la autenticación de certificado de cliente</li></ul> |
|Exchange 2010  | Incluye todas las características introducidas en Exchange 2007 SP1. Las siguientes características se introdujeron en la versión inicial de Exchange 2010: <ul> <li>  Lista de distribución privada completa</li><li>Objetos de configuración de usuario</li><li>Carpeta elementos asociados</li><li>Seguimiento de mensajes</li><li>Mensajería unificada</li><li>Detección automática de SOAP  </li><li>Compatibilidad mejorada con la zona horaria</li><li>Información de disponibilidad de recursos de sala</li><li>Búsqueda indizado</li><li>Acceso de volcado de archivos</li><li>Información de sugerencias de correo electrónico</li></ul> |
|Exchange 2007 SP1  | Incluye todas las características introducidas en Exchange 2007. Las siguientes características se introdujeron en Exchange 2007 SP1:  <ul><li>  Delegar la administración</li><li>Permisos de carpeta</li><li>Carpetas públicas</li><li>Elementos para exponer</li><li>Conversión de Id.</li></ul> |
|Exchange 2007  | Las siguientes características se introdujeron en la versión inicial de Exchange 2007:  <ul><li>  Acceso total a los elementos, carpetas y datos adjuntos (crear, Get, Update, Delete)</li><li>Disponibilidad</li><li>Fuera de la configuración de Office</li><li>Notificaciones</li><li>Sincronización</li><li>Resolución de nombres</li><li>Expansión de distribución (DL) de la lista</li><li>B?squeda</li></ul> |
   
## <a name="see-also"></a>Ver también

- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)
- [Migrar a las tecnologías de Exchange](../migrating-to-exchange-online-and-exchange-2013-technologies.md)
- [Explore la API administrada de EWS, EWS y servicios web de Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
    

