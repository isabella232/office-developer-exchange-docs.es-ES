---
title: Migrar a las tecnologías de Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 946a722f-0892-4a59-9e58-a291bfb6834a
description: Si va a migrar desde una versión anterior de Exchange, use la información de este artículo para averiguar qué tecnologías de desarrollo son compatibles con las versiones actuales del producto y a qué tecnología se debe migrar.
ms.openlocfilehash: d82f1b305fd1cc30e48cddbf9bf2981d3d829a5c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459156"
---
# <a name="migrating-to-exchange-technologies"></a>Migrar a las tecnologías de Exchange

Si va a migrar desde una versión anterior de Exchange, use la información de este artículo para averiguar qué tecnologías de desarrollo son compatibles con las versiones actuales del producto y a qué tecnología se debe migrar.
  
## <a name="determine-if-your-technology-is-available-in-current-versions"></a>Determinar si la tecnología está disponible en las versiones actuales

Use la tabla siguiente para determinar si una tecnología de desarrollo es compatible con Exchange online o Exchange 2019. Si la tecnología no se admite, vea [elegir una tecnología de desarrollo a la que migrar](#bk_choose).

<br/> 

**Tecnologías de desarrollo de Exchange y versiones de producto**

|Tecnológico|Office 365 y Exchange Online|Exchange 2019|Exchange 2016|Exchange 2013|Exchange 2010|Exchange 2007|
|:-----|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
|[Información general sobre la plataforma de las API de Office 365](https://msdn.microsoft.com/library/16fbf0c0-5470-466b-aab8-a0c9074c94e2%28Office.15%29.aspx) <br/> |X  <br/> |X ²  <br/> |X ¹ ²  <br/> ||
|[API administrada EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Servicios Web Exchange (EWS)](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Aplicaciones de correo para Outlook](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |||
|[Modelo de objetos de Outlook (OOM)](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Exchange Management Shell](management/exchange-management-shell.md) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Copia de seguridad y restauración](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|[Agentes de transporte](transport-agents/transport-agents-in-exchange-2013.md) <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |
|Interfaz de servicio de Active Directory (ADSI)  <br/> ||||||X  <br/> |
|Objetos de datos de colaboración para Exchange (CDOEX)  <br/> ||||||X  <br/> |
|Objetos de datos de colaboración para Windows 2000 (CDOSYS)  <br/> ||||||X  <br/> |
|Proveedor OLE DB de Exchange (EXOLEDB)  <br/> ||||||X  <br/> |
|Receptores de eventos del almacén de Exchange  <br/> ||||||X  <br/> |
|Sincronización de cambio incremental (ICS)  <br/> ||||||X  <br/> |
|Protocolo ligero de acceso a directorios (LDAP)  <br/> ||||||X  <br/> |
|[API de mensajería (MAPI)](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx) <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> |X  <br/> | 
|Personalización de Outlook Web App  <br/> ||X  <br/> |X  <br/> |X  <br/> |X  <br/> ||
|Creación y control de versiones distribuidos en Web (WebDAV)  <br/> ||||||X  <br/> |

<a name="bk_choose"> </a>

¹ la API de REST y la API de Graph requieren la actualización acumulativa 3 para Exchange 2016.

² solo los clientes híbridos pueden aprovechar las API de REST para los buzones de Office 365 y locales.

## <a name="choose-a-development-technology-to-migrate-to"></a>Elegir la tecnología de desarrollo que se va a migrar

Si la tecnología que usa la aplicación no es compatible con Exchange online o Exchange 2013, use la siguiente tabla para decidir a qué tecnología migrar.
  
**Rutas de migración de tecnología recomendadas**

|**Tecnológico**|**¿Compatible con Office 365, Exchange Online y Exchange 2019?**|**Migrar a**|**Más información**|
|:-----|:-----|:-----|:-----|
|ADSI  <br/> |Sí, pero sin enfatizar <br/>|[Exchange Management Shell](management/exchange-management-shell.md)<br/> |Ninguna.  <br/> |
|CDOEX  <br/> |No  <br/> |[EWS o API administrada de EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |La API administrada de EWS y EWS pueden obtener acceso al mismo almacén de Exchange que CDOEX proporciona. A diferencia de las aplicaciones cliente compiladas mediante CDOEX, puede ejecutar las aplicaciones de EWS en un equipo local o remoto.  <br/> |
|CDOEXM  <br/> |No <br/> |[Exchange Management Shell](management/exchange-management-shell.md) <br/> |Los comandos del shell de administración de Exchange controlan los servidores de Exchange, los grupos de almacenamiento, las bases de datos y los usuarios más sencillos que las API CDOEXM correspondientes. Además, puede migrar fácilmente sus aplicaciones CDOEXM a comandos del shell de administración de Exchange.  <br/> |
|CDOSYS<br/> |No<br/> |[Agentes de transporte](transport-agents/transport-agents-in-exchange-2013.md)   <br/> |Use agentes de transporte para aplicaciones basadas en notificaciones que funcionen con versiones de Exchange a partir de Exchange 2010.<br/><br/> CDOSYS se incluye en las versiones actuales de Windows. La funcionalidad de CDOSYS está disponible en .NET Framework.  <br/> |
|CDOWF  <br/> |No  <br/> |[Windows Workflow Foundation (WWF)](https://msdn.microsoft.com/library/vstudio/ms735967%28v=vs.90%29.aspx) <br/> |Puede usar WWF para crear aplicaciones de flujo de trabajo avanzadas que funcionen con Exchange 2007.   <br/> |
|ExOLEDB  <br/> |No  <br/> |[EWS o API administrada de EWS](exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md) <br/> |La API administrada de EWS y EWS proporcionan el mismo acceso al almacén de Exchange que ExOLEDB proporciona. A diferencia de las aplicaciones cliente compiladas mediante ExOLEDB, puede ejecutar las aplicaciones de EWS en un equipo local o remoto.  <br/> |
|IC  <br/> |Sí, pero sin enfatizar  <br/> |EWS o API administrada de EWS<br/> |Puede usar la API administrada de EWS o EWS para [suscribirse a notificaciones](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md) y [sincronizar datos de buzones](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md).  <br/> |
|LDAP  <br/> |Sí, pero sin enfatizar  <br/> |[Exchange Management Shell](management/exchange-management-shell.md) <br/> |Ninguna.  <br/> |
|MAPI  <br/> |Sí, pero sin enfatizar  <br/> |Información general sobre la plataforma de las API de Office 365, la API administrada de EWS, EWS <br/> |Aunque MAPI es actualmente una tecnología de desarrollo admitida, tendrá que volver a diseñar las aplicaciones MAPI para usar una tecnología más nueva.<br/><br/>Si la aplicación MAPI está realizando operaciones sencillas de lectura, escritura y actualización en objetos de correo, calendario o contacto y tiene como objetivo Office 365, Exchange 2019 ² o Exchange 2016 ¹ ² puede usar las [API de REST de office 365 para correo, calendarios y contactos](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md).<br/><br/>Si el destino es Exchange local y necesita tener acceso a todas las propiedades a las que puede tener acceso MAPI, puede usar la API administrada de EWS o EWS y las propiedades [extendidas o esquematizado](https://msdn.microsoft.com/library/68623048-060e-4602-b3fa-62617a94cf72%28Office.15%29.aspx).<br/><br/>**Nota**: la clase [ExtendedPropertyDefinition](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) proporciona acceso a MAPI desde la API administrada de EWS y el elemento [ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) proporciona acceso a las propiedades MAPI desde EWS.           |
|Personalización de Outlook Web App  <br/> |No  <br/> |[Aplicaciones de correo](exchange-web-services/mail-apps-for-outlook-and-ews-in-exchange.md) <br/> |Ninguna.  <br/> |
|Almacenar receptores de eventos  <br/> |No  <br/> |EWS o API administrada de EWS <br/> |Puede usar la API administrada de EWS o EWS para [suscribirse a notificaciones](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md) y [sincronizar datos de buzones](exchange-web-services/mailbox-synchronization-and-ews-in-exchange.md).<br/><br/>Las notificaciones de EWS proporcionan el mismo acceso al almacén de Exchange donde se almacenan los receptores de eventos. Puede usar las herramientas de Visual Studio para simplificar el desarrollo de aplicaciones de cliente que reconozcan eventos de almacenamiento que usen EWS.  <br/> |
|Copia de seguridad y restauración de transmisión  <br/> |No  <br/> |[Escritor del servicio de instantáneas de volumen (VSS)](backup-restore/backup-and-restore-for-exchange-2013.md) <br/> |Ninguna.  <br/> |
|WebDAV  <br/> |No  <br/> |Información general sobre la plataforma de API de Office 365, la API administrada de EWS o EWS <br/> |Si la aplicación WebDAV está realizando operaciones sencillas de lectura, escritura y actualización en los objetos de correo, calendario o contacto, y va a dirigirse a Office 365, Exchange 2019 ² o Exchange 2016 ¹ ², puede usar las [API de REST de office 365 para correo, calendarios y contactos](exchange-web-services/office-365-rest-apis-for-mail-calendars-and-contacts.md).<br/><br/>De lo contrario, si el destino es Exchange local y necesita obtener acceso a las mismas propiedades en el almacén de Exchange que WebDAV proporciona, use la API administrada de EWS o EWS.  <br/> |
|Notificaciones WebDAV  <br/> |No  <br/> |EWS o API administrada de EWS<br/> |Puede usar la API administrada de EWS o EWS para [suscribirse a las notificaciones](exchange-web-services/notification-subscriptions-mailbox-events-and-ews-in-exchange.md).  <br/> |
|Formularios Web  <br/> |No  <br/> |[ASP.NET](http://www.asp.net/web-forms) <br/> |Cambie a ASP.NET y actualice las aplicaciones para obtener acceso a la información de buzón de correo y servidor mediante EWS.  <br/> |
|Proveedores de WMI  <br/> |No  <br/> |[Exchange Management Shell](management/exchange-management-shell.md) <br/> |Ninguna.  <br/> |
   
¹ la API de REST y la API de Graph requieren la actualización acumulativa 3 para Exchange 2016.

² solo los clientes híbridos pueden aprovechar las API de REST para los buzones de Office 365 y locales.

## <a name="see-also"></a>Vea también

- [Seleccionar una API o tecnología para desarrollar soluciones de Outlook](https://msdn.microsoft.com/library/01a46083-03d0-4333-920c-01a9f17f68cb%28Office.15%29.aspx)
- [Requisitos de la arquitectura local de la API de REST](https://blogs.technet.microsoft.com/exchange/2016/09/26/on-premises-architectural-requirements-for-the-rest-api/)    
