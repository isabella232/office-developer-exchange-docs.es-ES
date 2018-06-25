---
title: DistinguishedFolderId (DistinguishedFolderIdNameType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 915b2ee9-8284-4bf6-8995-1fd0785e9e48
description: El elemento DistinguishedFolderId identifica las carpetas que se pueden hacer referencia por su nombre.
ms.openlocfilehash: 1f5b97fc7ee7b93989762c26e4b979a8dfb884be
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764248"
---
# <a name="distinguishedfolderid-distinguishedfolderidnametype"></a>DistinguishedFolderId (DistinguishedFolderIdNameType)

El elemento **DistinguishedFolderId** identifica las carpetas que se pueden hacer referencia por su nombre. 
  
```XML
<DistinguishedFolderId> calendar | contacts | deleteditems | drafts | inbox | journal | notes | outbox | sentitems | tasks | msgfolderroot | publicfoldersroot | root | junkemail | searchfolders | voicemail | recoverableitemsroot | recoverableitemsdeletions | recoverableitemsversions | recoverableitemspurges | archiveroot | archivemsgfolderroot | archivedeleteditems | archiverecoverableitemsroot | archiverecoverableitemsdeletions | archiverecoverableitemsversions | archiverecoverableitemspurges | syncissues | conflicts | localfailures | serverfailures | recipientcache | quickcontacts | conversationhistory | adminauditlogs | todosearch | mycontacts | directory | imcontactlist | peopleconnect</DistinguishedFolderId>
```

 **DistinguishedFolderIdNameType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Especifica una carpeta genérica.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Especifica una carpeta de calendario.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Especifica una carpeta de contactos.  <br/> |
   
## <a name="text-value"></a>Valor de texto

**Valores de texto de elemento DistinguishedFolderId**

|**Valor**|**Descripción**|
|:-----|:-----|
|calendario  <br/> |Indica la dirección URL de la carpeta del calendario.  <br/> |
|contactos  <br/> |Indica la dirección URL de la carpeta Contactos.  <br/> |
|deleteditems  <br/> |Indica la dirección URL de la carpeta Elementos eliminados.  <br/> |
|borradores  <br/> |Indica la dirección URL de la carpeta Borradores.  <br/> |
|Bandeja de entrada  <br/> |Indica la dirección URL de la carpeta Bandeja de entrada.  <br/> |
|diario  <br/> |Indica la dirección URL de la carpeta diario.  <br/> |
|notas  <br/> |Indica la dirección URL de la carpeta notas.  <br/> |
|Bandeja de salida  <br/> |Indica la dirección URL de la carpeta Bandeja de salida.  <br/> |
|elementos enviados  <br/> |Indica la dirección URL de la carpeta Elementos enviados.  <br/> |
|tasks  <br/> |Indica la dirección URL de la carpeta tareas.  <br/> |
|msgfolderroot  <br/> |Indica la dirección URL de la carpeta raíz de mensaje.  <br/> |
|publicfoldersroot  <br/> |Indica la dirección URL de la carpeta raíz de las carpetas públicas.  <br/> |
|root  <br/> |Indica la dirección URL de la carpeta raíz.  <br/> |
|junkemail  <br/> |Indica la dirección URL de la carpeta de correo electrónico no deseado.  <br/> |
|SearchFolders  <br/> |Indica la dirección URL de las carpetas de búsqueda.  <br/> |
|correo de voz  <br/> |Indica la dirección URL de la carpeta de correo de voz.  <br/> |
|recoverableitemsroot  <br/> |Indica la dirección URL de la carpeta raíz de elementos recuperables.  <br/> |
|recoverableitemsdeletions  <br/> |Indica la dirección URL de la carpeta elementos recuperables eliminado.  <br/> |
|recoverableitemsversions  <br/> |Indica la dirección URL de la carpeta de versiones de elemento recuperable.  <br/> |
|recoverableitemspurges  <br/> |Indica la dirección URL de la carpeta elementos recuperables purgados.  <br/> |
|archiveroot  <br/> |Indica la dirección URL de la carpeta raíz de archivo.  <br/> |
|archivemsgfolderroot  <br/> |Indica la dirección URL de la carpeta de raíz de carpeta de mensajes archivados.  <br/> |
|archivedeleteditems  <br/> |Indica la dirección URL de la carpeta Elementos eliminados archivados.  <br/> |
|archiverecoverableitemsroot  <br/> |Indica la dirección URL de la carpeta raíz de los elementos recuperables archivados.  <br/> |
|archiverecoverableitemsdeletions  <br/> |Indica la dirección URL de la carpeta Elementos eliminados recuperables archivados.  <br/> |
|archiverecoverableitemsversions  <br/> |Indica la dirección URL de la carpeta de versiones de los elementos recuperables archivados.  <br/> |
|archiverecoverableitemspurges  <br/> |Indica la dirección URL de la carpeta elementos recuperables purgados archivados.  <br/> |
|syncissues  <br/> |Indica la dirección URL de la carpeta problemas de sincronización.  <br/> |
|conflictos  <br/> |Indica la dirección URL de la carpeta conflictos.  <br/> |
|localfailures  <br/> |Indica la dirección URL de la carpeta errores locales.  <br/> |
|serverfailures  <br/> |Indica la dirección URL de la carpeta de errores del servidor.  <br/> |
|recipientcache  <br/> |Indica la dirección URL de la carpeta de caché del destinatario.  <br/> |
|QuickContacts  <br/> |Indica la dirección URL de la carpeta de contactos rápidos.  <br/> |
|conversationhistory  <br/> |Indica la dirección URL de la carpeta Historial de conversaciones.  <br/> |
|adminauditlogs  <br/> |Indica la dirección URL de la carpeta de registro de auditoría administrativas.  <br/> |
|todosearch  <br/> |Indica la dirección URL de la carpeta de tareas pendientes de la búsqueda.  <br/> |
|mycontacts  <br/> |Indica la dirección URL de la carpeta Mis contactos.  <br/> |
|Active Directory  <br/> |Indica una dirección URL de la carpeta de Active directory.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

