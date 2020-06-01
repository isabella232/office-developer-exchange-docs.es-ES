---
title: DistinguishedFolderId (DistinguishedFolderIdNameType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 915b2ee9-8284-4bf6-8995-1fd0785e9e48
description: El elemento DistinguishedFolderId identifica las carpetas a las que se puede hacer referencia por su nombre.
ms.openlocfilehash: ac239ec63f78322f6c82ab4be269d6fe4380dd8d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456195"
---
# <a name="distinguishedfolderid-distinguishedfolderidnametype"></a>DistinguishedFolderId (DistinguishedFolderIdNameType)

El elemento **DistinguishedFolderId** identifica las carpetas a las que se puede hacer referencia por su nombre. 
  
```XML
<DistinguishedFolderId> calendar | contacts | deleteditems | drafts | inbox | journal | notes | outbox | sentitems | tasks | msgfolderroot | publicfoldersroot | root | junkemail | searchfolders | voicemail | recoverableitemsroot | recoverableitemsdeletions | recoverableitemsversions | recoverableitemspurges | archiveroot | archivemsgfolderroot | archivedeleteditems | archiverecoverableitemsroot | archiverecoverableitemsdeletions | archiverecoverableitemsversions | archiverecoverableitemspurges | syncissues | conflicts | localfailures | serverfailures | recipientcache | quickcontacts | conversationhistory | adminauditlogs | todosearch | mycontacts | directory | imcontactlist | peopleconnect</DistinguishedFolderId>
```

 **DistinguishedFolderIdNameType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Especifica una carpeta genérica.  <br/> |
|[Hubiera](calendarfolder.md) <br/> |Especifica una carpeta de calendario.  <br/> |
|[Hubiera](contactsfolder.md) <br/> |Especifica una carpeta de contactos.  <br/> |
   
## <a name="text-value"></a>Valor de texto

**Valores de texto del elemento DistinguishedFolderId**

|**Valor**|**Descripción**|
|:-----|:-----|
|calendario  <br/> |Indica la dirección URL de la carpeta de calendario.  <br/> |
|contacts  <br/> |Indica la dirección URL de la carpeta de contactos.  <br/> |
|deleteditems  <br/> |Indica la dirección URL de la carpeta elementos eliminados.  <br/> |
|drafts  <br/> |Indica la dirección URL de la carpeta Borradores.  <br/> |
|inbox  <br/> |Indica la dirección URL de la carpeta Bandeja de entrada.  <br/> |
|Agenda  <br/> |Indica la dirección URL de la carpeta del diario.  <br/> |
|notas  <br/> |Indica la dirección URL de la carpeta notas.  <br/> |
|outbox  <br/> |Indica la dirección URL de la carpeta Bandeja de salida.  <br/> |
|sentitems  <br/> |Indica la dirección URL de la carpeta elementos enviados.  <br/> |
|tasks  <br/> |Indica la dirección URL de la carpeta tareas.  <br/> |
|msgfolderroot  <br/> |Indica la dirección URL de la carpeta raíz del mensaje.  <br/> |
|publicfoldersroot  <br/> |Indica la dirección URL de la carpeta raíz de carpetas públicas.  <br/> |
|root  <br/> |Indica la dirección URL de la carpeta raíz.  <br/> |
|junkemail  <br/> |Indica la dirección URL de la carpeta de correo electrónico no deseado.  <br/> |
|searchfolders  <br/> |Indica la dirección URL de las carpetas de búsqueda.  <br/> |
|correo de voz  <br/> |Indica la dirección URL de la carpeta de correo de voz.  <br/> |
|recoverableitemsroot  <br/> |Indica la dirección URL de la carpeta raíz de elementos recuperables.  <br/> |
|recoverableitemsdeletions  <br/> |Indica la dirección URL de la carpeta elementos recuperables eliminados.  <br/> |
|recoverableitemsversions  <br/> |Indica la dirección URL de la carpeta versiones de elementos recuperables.  <br/> |
|recoverableitemspurges  <br/> |Indica la dirección URL de la carpeta elementos recuperables purgados.  <br/> |
|archiveroot  <br/> |Indica la dirección URL de la carpeta raíz de archivo.  <br/> |
|archivemsgfolderroot  <br/> |Indica la dirección URL de la carpeta raíz de la carpeta de mensajes archivada.  <br/> |
|archivedeleteditems  <br/> |Indica la dirección URL de la carpeta de elementos eliminados archivados.  <br/> |
|archiverecoverableitemsroot  <br/> |Indica la dirección URL de la carpeta raíz de elementos recuperables archivados.  <br/> |
|archiverecoverableitemsdeletions  <br/> |Indica la dirección URL de la carpeta de elementos eliminados recuperables archivados.  <br/> |
|archiverecoverableitemsversions  <br/> |Indica la dirección URL de la carpeta de versiones de elementos recuperables archivados.  <br/> |
|archiverecoverableitemspurges  <br/> |Indica la dirección URL de la carpeta de elementos recuperables depurados archivados.  <br/> |
|syncissues  <br/> |Indica la dirección URL de la carpeta problemas de sincronización.  <br/> |
|conflicts  <br/> |Indica la dirección URL de la carpeta conflictos.  <br/> |
|localfailures  <br/> |Indica la dirección URL de la carpeta errores locales.  <br/> |
|serverfailures  <br/> |Indica la dirección URL de la carpeta errores del servidor.  <br/> |
|recipientcache  <br/> |Indica la dirección URL de la carpeta de la memoria caché de destinatarios.  <br/> |
|QuickContacts  <br/> |Indica la dirección URL de la carpeta de contactos rápidos.  <br/> |
|conversationhistory  <br/> |Indica la dirección URL de la carpeta Historial de conversaciones.  <br/> |
|adminauditlogs  <br/> |Indica la dirección URL de la carpeta de registro de auditoría administrativa.  <br/> |
|todosearch  <br/> |Indica la dirección URL de la carpeta de búsqueda de la tarea.  <br/> |
|mycontacts  <br/> |Indica la dirección URL de la carpeta Mis contactos.  <br/> |
|Active  <br/> |Indica una dirección URL de la carpeta del directorio.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

