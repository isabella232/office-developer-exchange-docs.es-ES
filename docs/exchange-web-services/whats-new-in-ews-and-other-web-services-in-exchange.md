---
title: Novedades de EWS y otros servicios web de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: aff6328f-cff1-42a6-9a4d-ea4d2d0461cf
description: Averigüe cuáles son las novedades en EWS y los servicios web de Exchange y la API administrada de EWS.
ms.openlocfilehash: 9e848babc96707152be767f42b561a587fc6cff0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763313"
---
# <a name="whats-new-in-ews-and-other-web-services-in-exchange"></a>Novedades de EWS y otros servicios web de Exchange

Averigüe cuáles son las novedades en EWS y los servicios web de Exchange y la API administrada de EWS.
  
Servicios Web de Exchange se han actualizado para incluir las nuevas características. 
  
**La tabla 1. Servicio web nuevas características en Exchange Online, Exchange 2013 y la API administrada de EWS**

|Característica|Implementado en Exchange Online|Implementado en Exchange 2013|Implementado en la API administrada de EWS|
|:-----|:-----:|:-----:|:-----:|
|[exhibición de documentos electrónicos](#eDisc) <br/> |Sí  <br/> |Sí  <br/> |Sí  <br/> |
|[Archivado](#arch) <br/> |Sí  <br/> |Sí  <br/> |Sí  <br/> |
|[Roles](#personas) <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|[Almacén de contactos unificados](#unified) <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|[Directivas de retención](#retentionpolicy) <br/> |Sí  <br/> |Sí  <br/> |Sí  <br/> |
|[Fotos de usuario](#userphoto) <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|[Aplicaciones de correo para la administración de Outlook](#ewsmailapps) <br/> |Sí  <br/> |Sí  <br/> |Sí  <br/> |
|[Proponer una nueva hora de reunión](#propose) <br/> |Sí  <br/> |No  <br/> |No  <br/> |

<a name="eDisc"> </a>

## <a name="ediscovery-in-ews"></a>exhibición de documentos electrónicos en EWS

exhibición de documentos electrónicos es un servicio web de consulta federada que permite a las aplicaciones externas, como SharePoint 2013 realizar consultas de datos de Exchange. Detección consta de varias fases, incluida la identificación y preservar los datos clave, selección hacia abajo y revisar los datos y producir datos en Tribunal. las consultas de exhibición de documentos electrónicos facilitan el proceso de detección, ya que proporciona un flujo de trabajo de detección único a través de Exchange y SharePoint.
  
**Tabla 2. Las operaciones de EWS y métodos de la API administrada de EWS para trabajar con la exhibición de documentos electrónicos**

|**Nombre de la operación**|**Método de la API administrada de EWS**|**Descripción**|
|:-----|:-----|:-----|
|[Operación GetDiscoverySearchConfiguration](http://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |[ExchangeService.GetDiscoverySearchConfiguration()](http://msdn.microsoft.com/en-us/library/jj670206%28v=exchg.80%29.aspx) <br/> |Obtiene la información de configuración de las suspensiones en contexto, guarda las búsquedas de detección y los buzones de correo que están habilitados para la búsqueda de detección.  <br/> |
|[Operación GetHoldOnMailboxes](http://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |[ExchangeService.GetHoldOnMailboxes()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getholdonmailboxes%28v=exchg.80%29.aspx) <br/> |Obtiene el estado de una suspensión basada en consultas, que se establece mediante la operación **SetHoldOnMailboxes** .  <br/> |
|[Operación GetNonIndexableItemDetails](http://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |[ExchangeService.GetNonIndexableItemDetails()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getnonindexableitemdetails%28v=exchg.80%29.aspx) <br/> |Obtiene los detalles sobre los elementos que no se pueden indizar. Esto incluye, pero no se limita a, el identificador de elemento, un código de error, una descripción del error, cuando se ha intentado el elemento y obtener información adicional acerca del elemento de índice.  <br/> |
|[Operación GetNonIndexableItemStatistics](http://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |[ExchangeService.GetNonIndexableItemStatistics()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getnonindexableitemstatistics%28v=exchg.80%29.aspx) <br/> |Obtiene el recuento de elementos que no se pueden indizar en un buzón de correo.  <br/> |
|[Operación GetSearchableMailboxes](http://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |[ExchangeService.GetSearchableMailboxes()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getsearchablemailboxes%28v=exchg.80%29.aspx) <br/> |Obtiene una lista de buzones de correo que el cliente tiene permiso para buscar o realizar la exhibición de documentos electrónicos en.  <br/> |
|[Operación SearchMailboxes](http://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |[ExchangeService.SearchMailboxes()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.searchmailboxes%28v=exchg.80%29.aspx) <br/> |Busca elementos en los buzones de correo específicos que coinciden con palabras clave de consulta.  <br/> |
|[Operación SetHoldOnMailboxes](http://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |[ExchangeService.SetHoldOnMailboxes()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.setholdonmailboxes%28v=exchg.80%29.aspx) <br/> |Mantenga conjuntos basada en una consulta en los elementos.  <br/> |

<a name="arch"> </a>

## <a name="archiving-in-ews"></a>Archivado en EWS

Buzones de archivo son buzones secundarios que están asociados con un usuario. Buzones de archivo se suelen usar para administrar los límites de almacenamiento de correo electrónico. Por ejemplo, los elementos de correo electrónico más antiguos es posible que periódicamente moverse desde la Bandeja de entrada para el buzón de archivo. 
  
Exchange presenta dos nuevas operaciones de EWS que puede usar para archivar un conjunto de elementos de correo desde un buzón principal. Archivar los elementos de la Bandeja de entrada de este modo, conserva a la jerarquía de carpetas de los elementos. Además, ahora se pueden almacenar buzones de archivo localmente en un cliente, o de forma remota, de una manera que sea opaca a un usuario, principalmente mediante el uso de una ruta de acceso de carpeta para que apunte al contenido del archivo.
  
**Tabla 3. Las operaciones de EWS y métodos de la API administrada de EWS para trabajar con el archivado**

|**Nombre de la operación**|**Método de la API administrada de EWS**|**Descripción**|
|:-----|:-----|:-----|
|[Operación ArchiveItem](http://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |[ExchangeService.ArchiveItems()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.archiveitems%28v=exchg.80%29.aspx) <br/> |Mueve un elemento desde el buzón principal para el buzón de archivo.  <br/> |
|[Operación CreateFolderPath](http://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |No se ha implementado.  <br/> |Crea una jerarquía de carpetas en un principal o buzón de archivo.  <br/> |

<a name="personas"> </a>

## <a name="personas-in-ews"></a>Roles de EWS

Un *rol* es una colección de datos que está asociados a un individuo. Los datos pueden proceder de uno o más orígenes y está asociados con el rol por medio de un identificador de vínculo comunes. Roles en EWS permiten vincular, buscar, examinar y recuperar información acerca de una persona de varios orígenes y organizar dicha información en una única entidad lógica. Roles difieren de los contactos en que un contacto es una colección de datos de un origen único que está asociado a un individuo; Por ejemplo, un contacto personal de Outlook o una entrada en una lista global de direcciones (GAL). 
  
La API administrada de EWS no implementa esta funcionalidad.
  
> [!NOTE]
> El almacén de contactos unificados también expone la funcionalidad de rol por medio de las operaciones que admitan esta característica. 
  
**Tabla 4. Operaciones de EWS para trabajar con roles**

|**Nombre de la operación**|**Descripción**|
|:-----|:-----|
|[Operación FindPeople](http://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) <br/> |Devuelve todos los objetos de rol desde una carpeta de contactos especificada o recupera todos los contactos que coinciden con una cadena de consulta especificada.  <br/> |
|[Operación GetPersona](http://msdn.microsoft.com/library/e2146df0-53d0-4caf-9758-b600bbc14b6a%28Office.15%29.aspx) <br/> |Recupera un rol.  <br/> |

<a name="unified"> </a>

## <a name="unified-contact-store-in-ews"></a>Almacén de contactos unificados en EWS

El almacén de contactos unificados es una característica que proporciona una experiencia coherente de contacto a través de productos de Office y actúa como un punto de integración de aplicaciones de terceros para usar el mismo almacén de contactos. Permite a los usuarios y las aplicaciones almacenar, administrar y tener acceso a información de contacto y hacer que esté disponible globalmente entre Lync, Exchange 2013, Outlook, Outlook Web App y cualquier otra aplicación que implementa el acceso para el almacén de contactos unificados. Exchange es el almacén de contactos para la experiencia del almacén de contactos unificados. 
  
La API administrada de EWS no implementa esta funcionalidad.
  
**Tabla 5. Operaciones de EWS para trabajar con el almacén de contactos unificados**

|**Nombre de la operación**|**Descripción**|
|:-----|:-----|
|[Operación AddNewImContactToGroup](http://msdn.microsoft.com/library/0cb5525f-faa3-48f1-9551-df55ffc26f46%28Office.15%29.aspx) <br/> |Agrega un nuevo contacto de mensajería instantánea a un grupo. El almacén de contactos unificados puede contener un máximo de 1000 contactos.  <br/> |
|[Operación AddImContactToGroup](http://msdn.microsoft.com/library/376acc42-2684-4596-aca1-82a4a10865c9%28Office.15%29.aspx) <br/> |Agrega un contacto de mensajería instantánea existente a un grupo. El almacén de contactos unificados puede contener un máximo de 1000 contactos.  <br/> |
|[Operación AddImGroup](http://msdn.microsoft.com/library/6df6e504-b7c8-4773-b10f-ffa5defac229%28Office.15%29.aspx) <br/> |Agrega un nuevo grupo de mensajería instantánea. El almacén de contactos unificados puede contener un máximo de 64 grupos.  <br/> |
|[Operación AddNewTelUriContactToGroup](http://msdn.microsoft.com/library/c9688ce8-2465-45bb-8bd2-94b32ed4885c%28Office.15%29.aspx) <br/> |Agrega un nuevo contacto a un grupo basado en el número de teléfono de un contacto.  <br/> |
|[Operación AddDistributionGroupToImList](http://msdn.microsoft.com/library/5aa9bec8-71cf-4a6e-8ec8-b4965b40fd4a%28Office.15%29.aspx) <br/> |Agrega un nuevo grupo de la lista de distribución. El almacén de contactos unificados puede contener un máximo de 64 grupos.  <br/> |
|[Operación GetImItemList](http://msdn.microsoft.com/library/e31d14e1-0c1f-4b69-98b7-157d59c13698%28Office.15%29.aspx) <br/> |Recupera una lista de grupos de mensajería instantánea y personas de contacto de mensajería instantánea.  <br/> |
|[Operación GetImItems](http://msdn.microsoft.com/library/51186691-46d2-4d5c-b8bc-4ee2bb20fbe7%28Office.15%29.aspx) <br/> |Recupera información acerca de los grupos de mensajería instantánea especificados y los roles de contacto de mensajería instantánea.  <br/> |
|[Operación RemoveContactFromImList](http://msdn.microsoft.com/library/28ec96c3-45af-48ff-9f17-718a527dc0ad%28Office.15%29.aspx) <br/> |Quita todos los grupos de mensajería instantánea del contacto especificado.  <br/> |
|[Operación RemoveImContactFromGroup](http://msdn.microsoft.com/library/a190bbec-c71b-4e6a-880b-55854c724d8c%28Office.15%29.aspx) <br/> |Quita un contacto de mensajería instantánea de un grupo.  <br/> |
|[Operación RemoveDistributionGroupFromImList](http://msdn.microsoft.com/library/252bddf2-98b6-4824-b548-2fba2bda5384%28Office.15%29.aspx) <br/> |Quita el grupo especificado de la lista de distribución de mensajería instantánea.  <br/> |
|[Operación RemoveImGroup](http://msdn.microsoft.com/library/5e788016-68e0-4a3f-9243-03f6b6c6b389%28Office.15%29.aspx) <br/> |Quita el grupo de mensajería instantánea especificado.  <br/> |
|[Operación SetImGroup](http://msdn.microsoft.com/library/2d48aa07-8152-4c3d-a519-061253e80174%28Office.15%29.aspx) <br/> |Cambia el nombre para mostrar de un grupo.  <br/> |

<a name="retentionpolicy"> </a>
  
## <a name="retention-policies-in-ews"></a>Directivas de retención de EWS

Las directivas de retención son las que se usan en Exchange al grupo de uno o más etiquetas de retención, para aplicar la configuración de retención a las carpetas o individuales por ejemplo, los elementos como los mensajes de correo de voz y correo electrónico y para aplicar la configuración de retención a un buzón de correo.
  
Exchange incluye tres tipos de etiquetas de retención:
  
- Etiquetas de directivas predeterminadas que se aplican a los elementos de buzón de correo que no tienen ningún otro tipo de etiqueta de retención aplicada.
    
- Etiquetas de directiva para la carpeta del sistema que se aplican a las carpetas de forma predeterminada como la Bandeja de entrada.
    
- Etiquetas personales que un usuario puede aplicar a las carpetas que se crean o a los elementos individuales.
    
Directiva de solo retención se puede asignar a un buzón de correo, pero la directiva puede tener uno o más etiquetas de retención de diversos tipos de vinculados a ella. Etiquetas de retención se pueden vincular a o desvincula de una directiva de retención en cualquier momento. Dirección URL de EWS en Exchange expone una nueva operación, [GetUserRetentionPolicyTags](http://msdn.microsoft.com/library/57c6ff23-5c2c-42ee-824b-5a1b6dafab8c%28Office.15%29.aspx), y la API administrada de EWS implementa un método nuevo, [ExchangeService.GetUserRetentionPolicyTags()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getuserretentionpolicytags%28v=exchg.80%29.aspx), que proporciona una lista de todas las etiquetas que están vinculados a una directiva de retención. Puede establecer y recuperar las etiquetas de directiva de retención de elementos y carpetas mediante el **método CreateItem**, **CreateFolder**, **UpdateItem**, **UpdateFolder**, **GetItem**y operaciones **GetFolder** . 

<a name="userphoto"> </a>

## <a name="requesting-user-photos"></a>Solicitar fotografías de usuario

Puede solicitar fotografías de usuario desde el servidor de Exchange mediante el uso de una de las dos implementaciones de la [operación de GetUserPhoto](http://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx): [REST](how-to-get-user-photos-by-using-ews-in-exchange.md) o SOAP. El extremo de REST usa una solicitud HTTPS **obtener** estándar para obtener la foto de usuario. El servicio ya sea devolverá una foto de usuario almacenada en Exchange o una foto de los servicios de dominio de Active Directory (AD DS). 
  
La API administrada de EWS no implementa esta funcionalidad. Sin embargo, puede usar la API administrada de EWS para devolver fotografías de usuario que se almacenan en un buzón de correo mediante la obtención de la foto que está unida a un contacto.

<a name="blocksender"> </a>

## <a name="block-senders-and-mark-email-as-junk-in-ews"></a>Bloquear los remitentes y marcar el correo electrónico como correo no deseado en EWS

Ahora puede bloquear los remitentes y marcar el correo electrónico como correo no deseado mediante el uso de la nueva [operación MarkAsJunk](http://msdn.microsoft.com/library/1f71f04d-56a9-4fee-a4e7-d1034438329e%28Office.15%29.aspx) en EWS o el método [ExchangeService.MarkAsJunk()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.markasjunk%28v=exchg.80%29.aspx) en la API administrada de EWS. 

<a name="ewsmailapps"> </a>

## <a name="mail-apps-for-outlook"></a>Aplicaciones de correo para Outlook

EWS ahora incluye compatibilidad para la administración de aplicaciones de correo para Outlook. 
  
**Tabla 6. Las operaciones de EWS y métodos de la API administrada de EWS para trabajar con aplicaciones de correo para Outlook**

|**Nombre de la operación**|**Método de la API administrada de EWS**|**Descripción**|
|:-----|:-----|:-----|
|[Operación DisableApp](http://msdn.microsoft.com/library/211731a3-2470-49af-bda3-1ddfc15a8e46%28Office.15%29.aspx) <br/> |[ExchangeService.DisableApp()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.disableapp%28v=exchg.80%29.aspx) <br/> |Deshabilita una aplicación instalada.  <br/> |
|[Operación GetAppManifests](http://msdn.microsoft.com/library/21a4987c-c24d-4a6e-ace4-e81edcda6303%28Office.15%29.aspx) <br/> |[ExchangeService.GetAppManifests()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getappmanifests%28v=exchg.80%29.aspx) <br/> |Obtiene los manifiestos de aplicación para un buzón de correo.  <br/> |
|[Operación GetAppMarketplaceUrl](http://msdn.microsoft.com/library/2c016fc3-0e13-4624-9a5b-d3e84577a860%28Office.15%29.aspx) <br/> |[ExchangeService.GetAppMarketplaceUrl()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getappmarketplaceurl%28v=exchg.80%29.aspx) <br/> |Obtiene la dirección URL de catálogo de soluciones de aplicación.  <br/> |
|[Operación GetClientAccessToken](http://msdn.microsoft.com/library/086876cc-e22c-4e89-89f9-19e78af51217%28Office.15%29.aspx) <br/> |[ExchangeService.GetClientAccessToken()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getclientaccesstoken%28v=exchg.80%29.aspx) <br/> |Obtiene los tokens de acceso de cliente.  <br/> |
|[Operación InstallApp](http://msdn.microsoft.com/library/596eae95-3e78-489a-8bb2-d2dd4a026405%28Office.15%29.aspx) <br/> |[ExchangeService.InstallApp()](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.installapp%28v=exchg.80%29.aspx) <br/> |Instala una aplicación para un buzón de correo.  <br/> |
|[Operación UninstallApp](http://msdn.microsoft.com/library/7707aa6a-381d-43f7-a454-54f6343ed127%28Office.15%29.aspx) <br/> |[ExchangeService.UninstallApp](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.uninstallapp%28v=exchg.80%29.aspx) <br/> |Desinstala una aplicación de un buzón de correo.  <br/> |

<a name="propose"> </a>

## <a name="propose-new-meeting-time"></a>Proponer una nueva hora de reunión

La nueva característica de tiempo proponer se introdujo en la versión 15.00.0800.007 de Exchange. Esto permite a los asistentes de la reunión [proponer nuevas horas de reunión](how-to-propose-a-new-meeting-time-by-using-ews-in-exchange.md) al organizador de la reunión. 
  
La API administrada de EWS no implementa esta funcionalidad.
  
## <a name="see-also"></a>Ver también

- [Explore la API administrada de EWS, EWS y servicios web de Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)  
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
- [Aplicaciones de correo de Outlook y EWS en Exchange](mail-apps-for-outlook-and-ews-in-exchange.md)
- [Archivado en EWS en Exchange](archiving-in-ews-in-exchange.md)
- [exhibición de documentos electrónicos en EWS en Exchange](ediscovery-in-ews-in-exchange.md)
- [Las personas y los contactos de EWS en Exchange](people-and-contacts-in-ews-in-exchange.md)
    

