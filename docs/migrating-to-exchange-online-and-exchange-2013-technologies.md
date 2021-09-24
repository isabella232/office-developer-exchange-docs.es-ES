---
title: Migrar a las tecnologías de Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 946a722f-0892-4a59-9e58-a291bfb6834a
description: Si está migrando desde una versión anterior de Exchange, use la información de este artículo para averiguar qué tecnologías de desarrollo se admiten en las versiones actuales del producto y a qué tecnología migrar.
ms.openlocfilehash: 3885d6789cedf5de028b64a0658b336bd021b9ee
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527004"
---
# <a name="migrating-to-exchange-technologies"></a>Migrar a las tecnologías de Exchange

Si está migrando desde una versión anterior de Exchange, use la información de este artículo para averiguar qué tecnologías de desarrollo se admiten en las versiones actuales del producto y a qué tecnología migrar.
  
## <a name="determine-if-your-technology-is-available-in-current-versions"></a>Determinar si la tecnología está disponible en versiones actuales

Use la tabla siguiente para determinar si se admite una tecnología de desarrollo Exchange Online o Exchange 2019. Si la tecnología no es compatible, vea [Choose a development technology to migrate to](#bk_choose).

<br/> 

**Exchange tecnologías de desarrollo y versiones de productos**

|Tecnología|Office 365 y Exchange Online|Exchange 2019|Exchange 2016|Exchange 2013|Exchange 2010|Exchange 2007|
|:-----|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|[Información general sobre la plataforma de las API de Office 365](https://msdn.microsoft.com/library/16fbf0c0-5470-466b-aab8-a0c9074c94e2%28Office.15%29.aspx) <br/> |X  <br/> |X²  <br/> |X¹ ²  <br/> ||
|[API administrada EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Servicios Web Exchange (EWS)](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Aplicaciones de correo para Outlook](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Outlook Modelo de objetos (OOM)](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Exchange Management Shell](management/exchange-management-shell.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Copia de seguridad y restauración](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Agentes de transporte](transport-agents/transport-agents-in-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Interfaz de servicio de Active Directory (ADSI)  <br/> ||||||X  <br/> |
|Objetos de datos de colaboración para Exchange (CDOEX)  <br/> ||||||X  <br/> |
|Objetos de datos de colaboración Windows 2000 (CDOSYS)  <br/> ||||||X  <br/> |
|Exchange Proveedor OLE DB (EXOLEDB)  <br/> ||||||X  <br/> |
|Receptores de eventos del almacén de Exchange  <br/> ||||||X  <br/> |
|Sincronización de cambio incremental (ICS)  <br/> ||||||X  <br/> |
|Protocolo ligero de acceso a directorios (LDAP)  <br/> ||||||X  <br/> |
|[API de mensajería (MAPI)](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> | 
|Outlook Web App personalización  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Creación y control de versiones distribuidos web (WebDAV)  <br/> ||||||X  <br/> |

<a name="bk_choose"> </a>

La API y la API Graph ¹REST requieren la actualización acumulativa 3 para Exchange 2016.

² Los clientes híbridos pueden aprovechar las API de REST tanto para Office 365 como para los buzones locales.

## <a name="choose-a-development-technology-to-migrate-to"></a>Elegir una tecnología de desarrollo a la que migrar

Si la tecnología que usa la aplicación no se admite ni se desemfasa en Exchange Online o Exchange 2013, use la tabla siguiente para decidir a qué tecnología migrar.
  
**Rutas de migración de tecnología recomendadas**

|**Tecnología**|**¿Se admite Office 365, Exchange Online y Exchange 2019?**|**Migrar a**|**Más información**|
|:-----|:-----|:-----|:-----|
|ADSI  <br/> |Sí, pero desemphasized <br/>|[Exchange Management Shell](management/exchange-management-shell.md)<br/> |Ninguno.  <br/> |
|CDOEX  <br/> |No  <br/> |[API administrada ews o EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |La API administrada ews y EWS pueden tener acceso al mismo Exchange que CDOEX proporciona. A diferencia de las aplicaciones cliente creadas mediante CDOEX, puede ejecutar aplicaciones EWS en un equipo local o remoto.  <br/> |
|CDOEXM  <br/> |No <br/> |[Exchange Management Shell](management/exchange-management-shell.md) <br/> |Exchange Los comandos del Shell de administración controlan Exchange servidores, grupos de almacenamiento, bases de datos y usuarios más simplemente que las API de CDOEXM correspondientes. Además, puede migrar fácilmente las aplicaciones CDOEXM a Exchange comandos del Shell de administración.  <br/> |
|CDOSYS<br/> |No<br/> |[Agentes de transporte](transport-agents/transport-agents-in-exchange-2013.md)   <br/> |Use agentes de transporte para aplicaciones basadas en notificaciones que funcionen con versiones de Exchange a partir Exchange 2010.<br/><br/> CDOSYS se incluye en las versiones actuales de Windows. La funcionalidad de CDOSYS está disponible en el .NET Framework.  <br/> |
|CDOWF  <br/> |No  <br/> |[Windows Workflow Foundation (WWF)](https://msdn.microsoft.com/library/vstudio/ms735967%28v=vs.90%29.aspx) <br/> |Puede usar WWF para crear aplicaciones de flujo de trabajo avanzadas que funcionen con Exchange 2007.   <br/> |
|ExOLEDB  <br/> |No  <br/> |[API administrada ews o EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |La API administrada ews y EWS proporcionan el mismo acceso al Exchange que proporciona ExOLEDB. A diferencia de las aplicaciones cliente creadas mediante ExOLEDB, puede ejecutar aplicaciones EWS en un equipo local o remoto.  <br/> |
|ICS  <br/> |Sí, pero desemphasized  <br/> |API administrada ews o EWS<br/> |Puede usar la API administrada ews o EWS para [suscribirse](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md) a las notificaciones y [sincronizar los datos del buzón.](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md)  <br/> |
|LDAP  <br/> |Sí, pero desemphasized  <br/> |[Exchange Management Shell](management/exchange-management-shell.md) <br/> |Ninguno.  <br/> |
|MAPI  <br/> |Sí, pero desemphasized  <br/> |Office 365 Introducción a la plataforma de API, API administrada ews, EWS <br/> |Aunque MAPI es actualmente una tecnología de desarrollo compatible, con el tiempo tendrá que rediseñar las aplicaciones MAPI para usar una tecnología más reciente.<br/><br/>Si la aplicación MAPI realiza operaciones sencillas de lectura, escritura y actualización en objetos de correo, calendario o contacto y destinos Office 365, Exchange 2019² o Exchange 2016¹ ², puede usar las API de REST de Office 365 para [correo, calendarios](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md)y contactos.<br/><br/>Si tiene como destino Exchange local y necesita tener acceso a todas las propiedades a las que MAPI puede tener acceso, puede usar la API administrada ews o EWS y las propiedades [esquematizadas](https://msdn.microsoft.com/library/68623048-060e-4602-b3fa-62617a94cf72%28Office.15%29.aspx)o las propiedades extendidas .<br/><br/>**NOTA:** [La clase ExtendedPropertyDefinition](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) proporciona acceso a MAPI desde la API administrada ews y el [elemento ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) proporciona acceso a las propiedades MAPI de EWS.           |
|Outlook Web App personalización  <br/> |No  <br/> |[Aplicaciones de correo](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |Ninguno.  <br/> |
|Receptores de eventos de la Tienda  <br/> |No  <br/> |API administrada ews o EWS <br/> |Puede usar la API administrada ews o EWS para [suscribirse](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md) a las notificaciones y [sincronizar los datos del buzón.](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md)<br/><br/>Las notificaciones de EWS proporcionan el mismo acceso al Exchange que proporcionan los receptores de eventos de almacén. Puede usar herramientas Visual Studio para simplificar el desarrollo de aplicaciones cliente que admiten eventos de almacén que usan EWS.  <br/> |
|Copia de seguridad y restauración de streaming  <br/> |No  <br/> |[Escritor del Servicio de instantáneas de volumen (VSS)](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> |Ninguna.  <br/> |
|WebDAV  <br/> |No  <br/> |Office 365 Introducción a la plataforma de API, API administrada ews o EWS <br/> |Si la aplicación WebDAV realiza operaciones sencillas de lectura, escritura y actualización en objetos de correo, calendario o contacto, y se dirigirá a Office 365, Exchange 2019² o Exchange 2016¹ ², puede usar las API de REST de Office 365 para [correo, calendarios](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md)y contactos .<br/><br/>De lo contrario, si está destinado Exchange local y necesita tener acceso a las mismas propiedades en el almacén de Exchange que WebDAV proporciona, use la API administrada ews o EWS.  <br/> |
|Notificaciones de WebDAV  <br/> |No  <br/> |API administrada ews o EWS<br/> |Puede usar la API administrada ews o EWS para [suscribirse a las notificaciones](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md).  <br/> |
|Formularios web  <br/> |No  <br/> |[ASP.NET](http://www.asp.net/web-forms) <br/> |Cambie a ASP.NET y actualice las aplicaciones para obtener acceso a la información del buzón y del servidor mediante EWS.  <br/> |
|Proveedores WMI  <br/> |No  <br/> |[Exchange Management Shell](management/exchange-management-shell.md) <br/> |Ninguno.  <br/> |
   
La API y la API Graph ¹REST requieren la actualización acumulativa 3 para Exchange 2016.

² Los clientes híbridos pueden aprovechar las API de REST tanto para Office 365 como para los buzones locales.

## <a name="see-also"></a>Ver también

- [Seleccionar una API o tecnología para desarrollar soluciones de Outlook](https://msdn.microsoft.com/library/01a46083-03d0-4333-920c-01a9f17f68cb%28Office.15%29.aspx)
- [Requisitos de la arquitectura local de la API de REST](https://blogs.technet.microsoft.com/exchange/2016/09/26/on-premises-architectural-requirements-for-the-rest-api/)    
