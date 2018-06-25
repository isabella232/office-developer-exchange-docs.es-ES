---
title: Migración a tecnologías de Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 946a722f-0892-4a59-9e58-a291bfb6834a
description: Si realiza la migración desde una versión anterior de Exchange, use la información de este artículo para averiguar qué tecnologías de desarrollo son compatibles con las versiones actuales de producto y qué tecnología para migrar a.
ms.openlocfilehash: 82362b7bcdb79d6ca43603335d51a8bd8c1df239
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763342"
---
# <a name="migrating-to-exchange-technologies"></a>Migración a tecnologías de Exchange

Si realiza la migración desde una versión anterior de Exchange, use la información de este artículo para averiguar qué tecnologías de desarrollo son compatibles con las versiones actuales de producto y qué tecnología para migrar a.
  
## <a name="determine-if-your-technology-is-available-in-current-versions"></a>Determinar si la tecnología está disponible en las versiones actuales

Use la tabla siguiente para determinar si una tecnología de desarrollo es compatible en Exchange Online o Exchange 2013. Si no se admite la tecnología, vea [Elegir una tecnología de desarrollo para migrar a](#bk_choose).

<br/> 

**Versiones de productos y tecnologías de desarrollo de Exchange**

|Tecnología|Office 365 y Exchange Online|Exchange 2013|Exchange 2010|Exchange 2007|
|:-----|:-----:|:-----:|:-----:|:-----:|
|[Introducción a la plataforma de API de Office 365](http://msdn.microsoft.com/library/16fbf0c0-5470-466b-aab8-a0c9074c94e2%28Office.15%29.aspx) <br/> |X  <br/> ||||
|[API administrada EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Servicios Web Exchange (EWS)](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Aplicaciones de correo para Outlook](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |||
|[Modelo de objetos de Outlook (OOM)](http://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Shell de administración de Exchange](management/exchange-management-shell.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Copia de seguridad y restauración](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |
|[Agentes de transporte](transport-agents/transport-agents-in-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |
|Interfaz de servicios de Active Directory (ADSI)  <br/> ||||X  <br/> |
|Objetos de datos de colaboración para Exchange (CDOEX)  <br/> ||||X  <br/> |
|Objetos de datos de colaboración para Windows 2000 (CDOSYS)  <br/> ||||X  <br/> |
|Proveedor de Exchange OLE DB (EXOLEDB)  <br/> ||||X  <br/> |
|Receptores de eventos del almacén de Exchange  <br/> ||||X  <br/> |
|Sincronización de cambio incremental (ICS)  <br/> ||||X  <br/> |
|Protocolo ligero de acceso a directorios (LDAP)  <br/> ||||X  <br/> |
|[API de mensajería (MAPI)](http://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Personalización de Outlook Web App  <br/> |||X  <br/> ||
|Web distribuida Authoring and Versioning (WebDAV)  <br/> ||||X  <br/> |

<a name="bk_choose"> </a>

## <a name="choose-a-development-technology-to-migrate-to"></a>Elección de una tecnología de desarrollo para migrar a

Si la tecnología de que la aplicación utiliza no es compatible o deemphasized en Exchange Online o Exchange 2013, use la tabla siguiente para decidir qué tecnología para migrar a.
  
**Rutas de acceso de migración de tecnología recomendada**

|**Tecnología**|**¿Se admite en Office 365, Exchange Online y Exchange 2013?**|**Migrar a**|**Obtener más información**|
|:-----|:-----|:-----|:-----|
|ADSI  <br/> |Sí, pero deemphasized <br/>|[Shell de administración de Exchange](management/exchange-management-shell.md)<br/> |Ninguno.  <br/> |
|CDOEX  <br/> |No  <br/> |[Administrada de EWS API o EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |La API administrada de EWS y EWS puede tener acceso el mismo almacén de Exchange que proporciona CDOEX. A diferencia de las aplicaciones de cliente creadas mediante CDOEX, puede ejecutar aplicaciones de EWS en un equipo local o remoto.  <br/> |
|CDOEXM  <br/> |No <br/> |[Shell de administración de Exchange](management/exchange-management-shell.md) <br/> |Comandos de Shell de administración de Exchange controlan servidores, grupos de almacenamiento, las bases de datos y los usuarios de Exchange más simple que las API de CDOEXM correspondiente. Además, puede migrar fácilmente sus aplicaciones CDOEXM para comandos de Shell de administración de Exchange.  <br/> |
|CDOSYS<br/> |No<br/> |[Agentes de transporte](transport-agents/transport-agents-in-exchange-2013.md)   <br/> |Use los agentes de transporte para aplicaciones basadas en la notificación que funcionan con las versiones de Exchange a partir de Exchange 2010.<br/><br/> CDOSYS se incluye en las versiones actuales de Windows. La funcionalidad de CDOSYS está disponible en .NET Framework.  <br/> |
|CDOWF  <br/> |No  <br/> |[Windows Workflow Foundation (WWF)](http://msdn.microsoft.com/en-us/library/vstudio/ms735967%28v=vs.90%29.aspx) <br/> |Puede usar WWF para crear aplicaciones de flujo de trabajo avanzado que funcionan con Exchange 2007.   <br/> |
|ExOLEDB  <br/> |No  <br/> |[Administrada de EWS API o EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |La API administrada de EWS y EWS proporcione el mismo acceso al almacén de Exchange que proporciona ExOLEDB. A diferencia de las aplicaciones cliente creadas mediante el uso de ExOLEDB, puede ejecutar aplicaciones de EWS en un equipo local o remoto.  <br/> |
|ICS  <br/> |Sí, pero deemphasized  <br/> |Administrada de EWS API o EWS<br/> |Puede usar la API administrada de EWS o EWS para [suscribirse a las notificaciones](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md) y [sincronizar los datos de buzón de correo](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md).  <br/> |
|LDAP  <br/> |Sí, pero deemphasized  <br/> |[Shell de administración de Exchange](management/exchange-management-shell.md) <br/> |Ninguno.  <br/> |
|MAPI  <br/> |Sí, pero deemphasized  <br/> |API plataforma Introducción a Office 365, API administrada de EWS, EWS <br/> |Aunque MAPI actualmente es una tecnología de desarrollo compatibles, finalmente tendrá que volver a diseñar las aplicaciones MAPI para usar una tecnología más reciente.<br/><br/>Si está realizando la aplicación MAPI simple operaciones de lectura, escritura y actualización de correo, calendario, o los objetos de contacto y los objetivos de Office 365, puede usar las [API de REST de Office 365 para correo, los calendarios y contactos](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md).<br/><br/>Si la identificación de Exchange local y debe tener acceso a todas las propiedades que puede tener acceso MAPI, puede usar la API administrada de EWS o EWS y [encuentra esquematizado propiedades o propiedades extendidas](http://msdn.microsoft.com/library/68623048-060e-4602-b3fa-62617a94cf72%28Office.15%29.aspx).<br/><br/>**Nota**: la clase [ExtendedPropertyDefinition](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) proporciona acceso a MAPI desde la API administrada de EWS y el elemento [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) proporciona acceso a las propiedades MAPI de EWS.           |
|Personalización de Outlook Web App  <br/> |No  <br/> |[Aplicaciones de correo](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |Ninguno.  <br/> |
|Receptores de eventos de almacén  <br/> |No  <br/> |Administrada de EWS API o EWS <br/> |Puede usar la API administrada de EWS o EWS para [suscribirse a las notificaciones](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md) y [sincronizar los datos de buzón de correo](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md).<br/><br/>Las notificaciones de EWS proporcionan el mismo acceso al almacén de Exchange que proporcionan receptores de eventos del almacén. Puede usar las herramientas de Visual Studio para simplificar el desarrollo de aplicaciones de cliente de eventos de almacenamiento que usan EWS.  <br/> |
|Transmisión por secuencias de copia de seguridad y restauración  <br/> |No  <br/> |[Escritor de Volume Shadow Copy Service (VSS)](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> |Ninguno.  <br/> |
|WebDAV  <br/> |No  <br/> |API plataforma Introducción a Office 365, API administrada de EWS o EWS <br/> |Si está realizando la aplicación WebDAV simple operaciones de lectura, escritura y actualización en correo, calendario o en los objetos de contacto, y se dirige a Office 365, use las [API de REST de Office 365 para correo, los calendarios y contactos](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md).<br/><br/>De lo contrario, si la identificación de Exchange local y necesita tener acceso a las mismas propiedades en el almacén de Exchange que WebDAV proporciona, utilice la API administrada de EWS o EWS.  <br/> |
|Notificaciones WebDAV  <br/> |No  <br/> |Administrada de EWS API o EWS<br/> |Puede usar la API administrada de EWS o EWS para [suscribirse a las notificaciones](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md).  <br/> |
|Formularios Web forms  <br/> |No  <br/> |[ASP.NET](http://www.asp.net/web-forms) <br/> |Cambie a ASP.NET y actualizar las aplicaciones para tener acceso a información de buzón de correo y el servidor mediante el uso de EWS.  <br/> |
|Proveedores de WMI  <br/> |No  <br/> |[Shell de administración de Exchange](management/exchange-management-shell.md) <br/> |Ninguno.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Seleccionar una API o tecnología para desarrollar soluciones para Outlook](http://msdn.microsoft.com/library/01a46083-03d0-4333-920c-01a9f17f68cb%28Office.15%29.aspx)
    

