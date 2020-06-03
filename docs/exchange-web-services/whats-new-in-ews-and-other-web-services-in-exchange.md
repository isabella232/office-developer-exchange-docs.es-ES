---
title: Novedades de EWS y otros servicios Web de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: aff6328f-cff1-42a6-9a4d-ea4d2d0461cf
description: Descubra las novedades de EWS y los servicios Web de Exchange y la API administrada de EWS.
localization_priority: Priority
ms.openlocfilehash: 5e74ad9d4cf5083983c28e477fd50d48e2d7fbb6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529843"
---
# <a name="whats-new-in-ews-and-other-web-services-in-exchange"></a>Novedades de EWS y otros servicios Web de Exchange

Descubra las novedades de EWS y los servicios Web de Exchange y la API administrada de EWS.
  
Los servicios Web de Exchange se han actualizado para incluir nuevas características. 
  
**Tabla 1. Nuevas características de servicio Web en Exchange Online, Exchange 2013 y la API administrada de EWS**

|Característica|Implementado en Exchange Online|Se implementa en Exchange 2013|Se implementa en la API administrada de EWS|
|:-----|:-----:|:-----:|:-----:|
|[Exhibición de documentos electrónicos (eDiscovery)](#eDisc) <br/> |Sí  <br/> |Sí  <br/> |Sí  <br/> |
|[Archivado](#arch) <br/> |Sí  <br/> |Sí  <br/> |Sí  <br/> |
|[Roles](#personas) <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|[Almacén de contactos unificado](#unified) <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|[Directivas de retención](#retentionpolicy) <br/> |Sí  <br/> |Sí  <br/> |Sí  <br/> |
|[Fotos de usuario](#userphoto) <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|[Aplicaciones de correo para la administración de Outlook](#ewsmailapps) <br/> |Sí  <br/> |Sí  <br/> |Sí  <br/> |
|[Proponer una nueva hora de reunión](#propose) <br/> |Sí  <br/> |No  <br/> |No  <br/> |

<a name="eDisc"> </a>

## <a name="ediscovery-in-ews"></a>eDiscovery en EWS

eDiscovery es un servicio Web de consulta federado que permite a las aplicaciones externas, como SharePoint 2013, realizar consultas de datos de Exchange. La detección consta de varias fases, incluidas la identificación y conservación de datos clave, la selección y la revisión de los datos, y la generación de datos en el Tribunal. las consultas de exhibición de documentos electrónicos facilitan el proceso de detección al proporcionar un único flujo de trabajo de detección en Exchange y SharePoint.
  
**Tabla 2. Operaciones de EWS y métodos de API administrada de EWS para trabajar con eDiscovery**

|**Nombre de operación**|**Método de la API administrada de EWS**|**Descripción**|
|:-----|:-----|:-----|
|[Operación GetDiscoverySearchConfiguration](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |[ExchangeService. GetDiscoverySearchConfiguration ()](https://msdn.microsoft.com/library/jj670206%28v=exchg.80%29.aspx) <br/> |Obtiene información de configuración para las suspensiones locales, las búsquedas de detección guardadas y los buzones que están habilitados para la búsqueda de detección.  <br/> |
|[Operación GetHoldOnMailboxes](https://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |[ExchangeService. GetHoldOnMailboxes ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getholdonmailboxes%28v=exchg.80%29.aspx) <br/> |Obtiene el estado de una suspensión basada en consulta, que se establece mediante la operación **SetHoldOnMailboxes** .  <br/> |
|[Operación GetNonIndexableItemDetails](https://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |[ExchangeService. GetNonIndexableItemDetails ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getnonindexableitemdetails%28v=exchg.80%29.aspx) <br/> |Obtiene información detallada sobre los elementos que no se pueden indizar. Esto incluye, entre otros, el identificador de elemento, un código de error, una descripción de error, cuando se realizó un intento de indizar el elemento y información adicional sobre el elemento.  <br/> |
|[Operación GetNonIndexableItemStatistics](https://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |[ExchangeService. GetNonIndexableItemStatistics ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getnonindexableitemstatistics%28v=exchg.80%29.aspx) <br/> |Obtiene el recuento de elementos que no se pueden indizar en un buzón.  <br/> |
|[Operación GetSearchableMailboxes](https://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |[ExchangeService. GetSearchableMailboxes ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getsearchablemailboxes%28v=exchg.80%29.aspx) <br/> |Obtiene una lista de buzones en los que el cliente tiene permiso para buscar o realizar la exhibición de documentos electrónicos en.  <br/> |
|[Operación SearchMailboxes](https://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |[ExchangeService. SearchMailboxes ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.searchmailboxes%28v=exchg.80%29.aspx) <br/> |Busca elementos en buzones específicos que coinciden con las palabras clave de consulta.  <br/> |
|[Operación SetHoldOnMailboxes](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |[ExchangeService. SetHoldOnMailboxes ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx) <br/> |Establece una retención basada en consultas en elementos.  <br/> |

<a name="arch"> </a>

## <a name="archiving-in-ews"></a>Archivado en EWS

Los buzones de archivo son buzones secundarios que están asociados a un usuario. Los buzones de archivo se usan normalmente para administrar los límites de almacenamiento de correo electrónico. Por ejemplo, es posible que los elementos de correo electrónico antiguos se muevan periódicamente de la bandeja de entrada al buzón de archivo. 
  
Exchange presenta dos nuevas operaciones EWS que puede usar para archivar un conjunto de elementos de correo desde un buzón principal. Archivar elementos de la bandeja de entrada de esta manera conserva la jerarquía de carpetas de los elementos. Además, los buzones de archivo ahora se pueden almacenar de forma local en un cliente, o de forma remota, de forma que sea prácticamente opaca para un usuario, mediante una ruta de acceso de carpeta que apunte al contenido del archivo.
  
**Tabla 3. Operaciones de EWS y métodos de API administrada de EWS para trabajar con el archivado**

|**Nombre de operación**|**Método de la API administrada de EWS**|**Descripción**|
|:-----|:-----|:-----|
|[Operación ArchiveItem](https://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |[ExchangeService. ArchiveItems ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.archiveitems%28v=exchg.80%29.aspx) <br/> |Mueve un elemento del buzón de correo principal al buzón de archivo.  <br/> |
|[Operación CreateFolderPath](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |No implementado.  <br/> |Crea una jerarquía de carpetas en un buzón principal o de archivo.  <br/> |

<a name="personas"> </a>

## <a name="personas-in-ews"></a>Roles en EWS

Un *rol* es una colección de datos asociados a una persona. Los datos pueden proceder de uno o varios orígenes y se asocian con el rol por medio de un identificador de vínculo común. Los roles de EWS permiten vincular, buscar, examinar y recuperar información sobre una persona de varios orígenes y organizarla en una única entidad lógica. Los roles se diferencian de los contactos en que un contacto es una colección de datos de un solo origen que está asociado a un individuo; por ejemplo, un contacto personal de Outlook o una entrada de una lista global de direcciones (GAL). 
  
La API administrada de EWS no implementa esta funcionalidad.
  
> [!NOTE]
> El almacén de contactos unificado también expone la funcionalidad de los roles por medio de las operaciones que admiten esa característica. 
  
**Tabla 4. Operaciones de EWS para trabajar con roles**

|**Nombre de operación**|**Descripción**|
|:-----|:-----|
|[Operación FindPeople](https://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) <br/> |Devuelve todos los objetos de rol de una carpeta de contactos especificada o recupera todos los contactos que coinciden con una cadena de consulta especificada.  <br/> |
|[Operación GetPersona](https://msdn.microsoft.com/library/e2146df0-53d0-4caf-9758-b600bbc14b6a%28Office.15%29.aspx) <br/> |Recupera un rol.  <br/> |

<a name="unified"> </a>

## <a name="unified-contact-store-in-ews"></a>Almacén de contactos unificados en EWS

El almacén de contactos unificado es una característica que proporciona una experiencia de contacto coherente entre los productos de Office y actúa como un punto de integración para que las aplicaciones de terceros usen el mismo almacén de contactos. Permite que los usuarios y las aplicaciones almacenen, administren y obtengan acceso a la información de contacto y que estén disponibles globalmente entre Lync, Exchange 2013, Outlook, Outlook Web App y cualquier otra aplicación que implemente el acceso al almacén de contactos unificado. Exchange es el almacén de contactos para la experiencia del almacén de contactos unificado. 
  
La API administrada de EWS no implementa esta funcionalidad.
  
**Tabla 5. Operaciones de EWS para trabajar con el almacén de contactos unificado**

|**Nombre de operación**|**Descripción**|
|:-----|:-----|
|[Operación AddNewImContactToGroup](https://msdn.microsoft.com/library/0cb5525f-faa3-48f1-9551-df55ffc26f46%28Office.15%29.aspx) <br/> |Agrega un nuevo contacto de mensajería instantánea a un grupo. El almacén de contactos unificado puede contener un máximo de 1000 contactos.  <br/> |
|[Operación AddImContactToGroup](https://msdn.microsoft.com/library/376acc42-2684-4596-aca1-82a4a10865c9%28Office.15%29.aspx) <br/> |Agrega un contacto de mi existente a un grupo. El almacén de contactos unificado puede contener un máximo de 1000 contactos.  <br/> |
|[Operación AddImGroup](https://msdn.microsoft.com/library/6df6e504-b7c8-4773-b10f-ffa5defac229%28Office.15%29.aspx) <br/> |Agrega un nuevo grupo de mensajería instantánea. El almacén de contactos unificado puede contener un máximo de 64 grupos.  <br/> |
|[Operación AddNewTelUriContactToGroup](https://msdn.microsoft.com/library/c9688ce8-2465-45bb-8bd2-94b32ed4885c%28Office.15%29.aspx) <br/> |Agrega un nuevo contacto a un grupo basado en el número de teléfono de un contacto.  <br/> |
|[Operación AddDistributionGroupToImList](https://msdn.microsoft.com/library/5aa9bec8-71cf-4a6e-8ec8-b4965b40fd4a%28Office.15%29.aspx) <br/> |Agrega un nuevo grupo de lista de distribución. El almacén de contactos unificado puede contener un máximo de 64 grupos.  <br/> |
|[Operación GetImItemList](https://msdn.microsoft.com/library/e31d14e1-0c1f-4b69-98b7-157d59c13698%28Office.15%29.aspx) <br/> |Recupera una lista de grupos de mensajería instantánea y los roles de contactos de mensajería instantánea.  <br/> |
|[Operación GetImItems](https://msdn.microsoft.com/library/51186691-46d2-4d5c-b8bc-4ee2bb20fbe7%28Office.15%29.aspx) <br/> |Recupera información sobre los grupos de mensajería instantánea y los roles de contactos de mensajería instantánea especificados.  <br/> |
|[Operación RemoveContactFromImList](https://msdn.microsoft.com/library/28ec96c3-45af-48ff-9f17-718a527dc0ad%28Office.15%29.aspx) <br/> |Quita el contacto especificado de todos los grupos de mensajería instantánea.  <br/> |
|[Operación RemoveImContactFromGroup](https://msdn.microsoft.com/library/a190bbec-c71b-4e6a-880b-55854c724d8c%28Office.15%29.aspx) <br/> |Quita un contacto de mensajería instantánea de un grupo.  <br/> |
|[Operación RemoveDistributionGroupFromImList](https://msdn.microsoft.com/library/252bddf2-98b6-4824-b548-2fba2bda5384%28Office.15%29.aspx) <br/> |Quita el grupo de lista de distribución de mensajería instantánea especificado.  <br/> |
|[Operación RemoveImGroup](https://msdn.microsoft.com/library/5e788016-68e0-4a3f-9243-03f6b6c6b389%28Office.15%29.aspx) <br/> |Quita el grupo de mensajería instantánea especificado.  <br/> |
|[Operación SetImGroup](https://msdn.microsoft.com/library/2d48aa07-8152-4c3d-a519-061253e80174%28Office.15%29.aspx) <br/> |Cambia el nombre para mostrar de un grupo.  <br/> |

<a name="retentionpolicy"> </a>
  
## <a name="retention-policies-in-ews"></a>Directivas de retención en EWS

Las directivas de retención son directivas que se usan en Exchange para agrupar una o más etiquetas de retención, para aplicar la configuración de retención a carpetas o elementos individuales, como mensajes de correo de voz y de correo electrónico, y para aplicar la configuración de retención a un buzón.
  
Exchange incluye tres tipos de etiquetas de retención:
  
- Etiquetas de directivas predeterminadas que se aplican a los elementos del buzón que no tienen ningún otro tipo de etiqueta de retención aplicada.
    
- Etiquetas de directiva de la carpeta del sistema que se aplican a las carpetas predeterminadas, como la bandeja de entrada.
    
- Etiquetas personales que un usuario puede aplicar a las carpetas que crean o a elementos individuales.
    
Solo se puede asignar una directiva de retención a un buzón, pero la Directiva puede tener una o más etiquetas de retención de varios tipos vinculados a ella. Las etiquetas de retención se pueden vincular o desvincular desde una directiva de retención en cualquier momento. EWS en Exchange expone una nueva operación, [GetUserRetentionPolicyTags](https://msdn.microsoft.com/library/57c6ff23-5c2c-42ee-824b-5a1b6dafab8c%28Office.15%29.aspx), y la API administrada de EWS implementa un nuevo método, [ExchangeService. GetUserRetentionPolicyTags ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getuserretentionpolicytags%28v=exchg.80%29.aspx), que proporciona una lista de todas las etiquetas vinculadas a una directiva de retención. Puede establecer y recuperar etiquetas de directiva de retención para elementos y carpetas mediante las operaciones **CreateItem**, **CreateFolder**, **UpdateItem**, **UpdateFolder**, **GetItem**y **GetFolder** . 

<a name="userphoto"> </a>

## <a name="requesting-user-photos"></a>Solicitar fotos de usuario

Puede solicitar fotos de usuario del servidor de Exchange mediante una de las dos implementaciones de la [operación GetUserPhoto](https://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx): [Rest](how-to-get-user-photos-by-using-ews-in-exchange.md) o SOAP. El punto de conexión de REST usa una solicitud **Get** estándar de HTTPS para obtener la foto del usuario. El servicio devolverá una foto de usuario almacenada en Exchange o una foto de los servicios de dominio de Active Directory (AD DS). 
  
La API administrada de EWS no implementa esta funcionalidad. Sin embargo, puede usar la API administrada de EWS para devolver fotos de los usuarios que se almacenan en un buzón de correo al obtener la foto adjunta a un contacto.

<a name="blocksender"> </a>

## <a name="block-senders-and-mark-email-as-junk-in-ews"></a>Bloquear remitentes y marcar correo electrónico como correo no deseado en EWS

Ahora puede bloquear a los remitentes y marcar los correos electrónicos como correo no deseado con la nueva [operación MarkAsJunk](https://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) en EWS o el método [ExchangeService. MarkAsJunk ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) en la API administrada de EWS. 

<a name="ewsmailapps"> </a>

## <a name="mail-apps-for-outlook"></a>Aplicaciones de correo para Outlook

EWS ahora incluye compatibilidad con la administración de aplicaciones de correo para Outlook. 
  
**Tabla 6. Operaciones de EWS y métodos de API administrada de EWS para trabajar con aplicaciones de correo para Outlook**

|**Nombre de operación**|**Método de la API administrada de EWS**|**Descripción**|
|:-----|:-----|:-----|
|[Operación DisableApp](https://msdn.microsoft.com/library/211731a3-2470-49af-bda3-1ddfc15a8e46%28Office.15%29.aspx) <br/> |[ExchangeService. DisableApp ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.disableapp%28v=exchg.80%29.aspx) <br/> |Deshabilita una aplicación instalada.  <br/> |
|[Operación GetAppManifests](https://msdn.microsoft.com/library/21a4987c-c24d-4a6e-ace4-e81edcda6303%28Office.15%29.aspx) <br/> |[ExchangeService. GetAppManifests ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getappmanifests%28v=exchg.80%29.aspx) <br/> |Obtiene los manifiestos de aplicación de un buzón.  <br/> |
|[Operación GetAppMarketplaceUrl](https://msdn.microsoft.com/library/2c016fc3-0e13-4624-9a5b-d3e84577a860%28Office.15%29.aspx) <br/> |[ExchangeService. GetAppMarketplaceUrl ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getappmarketplaceurl%28v=exchg.80%29.aspx) <br/> |Obtiene la dirección URL del catálogo de soluciones de aplicaciones.  <br/> |
|[Operación GetClientAccessToken](https://msdn.microsoft.com/library/086876cc-e22c-4e89-89f9-19e78af51217%28Office.15%29.aspx) <br/> |[ExchangeService. GetClientAccessToken ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getclientaccesstoken%28v=exchg.80%29.aspx) <br/> |Obtiene los tokens de acceso de cliente.  <br/> |
|[Operación InstallApp](https://msdn.microsoft.com/library/596eae95-3e78-489a-8bb2-d2dd4a026405%28Office.15%29.aspx) <br/> |[ExchangeService. InstallApp ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.installapp%28v=exchg.80%29.aspx) <br/> |Instala una aplicación para un buzón de correo.  <br/> |
|[Operación UninstallApp](https://msdn.microsoft.com/library/7707aa6a-381d-43f7-a454-54f6343ed127%28Office.15%29.aspx) <br/> |[ExchangeService. UninstallApp](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.uninstallapp%28v=exchg.80%29.aspx) <br/> |Desinstala una aplicación de un buzón.  <br/> |

<a name="propose"> </a>

## <a name="propose-new-meeting-time"></a>Proponer una nueva hora de reunión

La característica proponer nueva hora se introdujo en la versión 15.00.0800.007 de Exchange. Esto permite a los asistentes a la reunión [proponer nuevas horas de reunión](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md) al organizador de la reunión. 
  
La API administrada de EWS no implementa esta funcionalidad.
  
## <a name="see-also"></a>Vea también

- [Explore la API administrada de EWS, EWS y servicios web de Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
- [Aplicaciones de correo para Outlook y EWS en Exchange](mail-apps-for-outlook-and-ews-in-exchange.md)
- [Archivado en EWS en Exchange](archiving-in-ews-in-exchange.md)
- [eDiscovery en EWS en Exchange](ediscovery-in-ews-in-exchange.md)
- [Personas y contactos de EWS en Exchange](people-and-contacts-in-ews-in-exchange.md)
    

