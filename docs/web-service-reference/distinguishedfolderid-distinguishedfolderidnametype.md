---
title: DistinguishedFolderId (DistinguishedFolderIdNameType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 915b2ee9-8284-4bf6-8995-1fd0785e9e48
description: El elemento DistinguishedFolderId identifica las carpetas a las que se puede hacer referencia por su nombre.
ms.openlocfilehash: 23d1dead5a97fe8b2ceb29235f4b784f667d2ee1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526443"
---
# <a name="distinguishedfolderid-distinguishedfolderidnametype"></a>DistinguishedFolderId (DistinguishedFolderIdNameType)

El **elemento DistinguishedFolderId** identifica las carpetas a las que se puede hacer referencia por su nombre. 
  
```XML
<DistinguishedFolderId> calendar | contacts | deleteditems | drafts | inbox | journal | notes | outbox | sentitems | tasks | msgfolderroot | publicfoldersroot | root | junkemail | searchfolders | voicemail | recoverableitemsroot | recoverableitemsdeletions | recoverableitemsversions | recoverableitemspurges | archiveroot | archivemsgfolderroot | archivedeleteditems | archiverecoverableitemsroot | archiverecoverableitemsdeletions | archiverecoverableitemsversions | archiverecoverableitemspurges | syncissues | conflicts | localfailures | serverfailures | recipientcache | quickcontacts | conversationhistory | adminauditlogs | todosearch | mycontacts | directory | imcontactlist | peopleconnect</DistinguishedFolderId>
```

 **DistinguishedFolderIdNameType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Especifica una carpeta genérica.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Especifica una carpeta de calendario.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Especifica una carpeta de contactos.  <br/> |
   
## <a name="text-value"></a>Valor de texto

**Valores de texto del elemento DistinguishedFolderId**

|**Valor**|**Descripción**|
|:-----|:-----|
|calendar  <br/> |Indica la dirección URL de la carpeta de calendario.  <br/> |
|contacts  <br/> |Indica la dirección URL de la carpeta de contactos.  <br/> |
|deleteditems  <br/> |Indica la dirección URL de la carpeta de elementos eliminados.  <br/> |
|drafts  <br/> |Indica la dirección URL de la carpeta borradores.  <br/> |
|inbox  <br/> |Indica la dirección URL de la carpeta de la bandeja de entrada.  <br/> |
|diario  <br/> |Indica la dirección URL de la carpeta del diario.  <br/> |
|notas  <br/> |Indica la dirección URL de la carpeta de notas.  <br/> |
|outbox  <br/> |Indica la dirección URL de la carpeta de la bandeja de salida.  <br/> |
|sentitems  <br/> |Indica la dirección URL de la carpeta de elementos enviados.  <br/> |
|tasks  <br/> |Indica la dirección URL de la carpeta tareas.  <br/> |
|msgfolderroot  <br/> |Indica la dirección URL de la carpeta raíz del mensaje.  <br/> |
|publicfoldersroot  <br/> |Indica la dirección URL de la carpeta raíz de carpetas públicas.  <br/> |
|root  <br/> |Indica la dirección URL de la carpeta raíz.  <br/> |
|junkemail  <br/> |Indica la dirección URL de la carpeta de correo no deseado.  <br/> |
|searchfolders  <br/> |Indica la dirección URL de las carpetas de búsqueda.  <br/> |
|correo de voz  <br/> |Indica la dirección URL de la carpeta de correo de voz.  <br/> |
|recoverableitemsroot  <br/> |Indica la dirección URL de la carpeta raíz de elementos recuperables.  <br/> |
|recoverableitemsdeletions  <br/> |Indica la dirección URL de la carpeta elementos recuperables eliminados.  <br/> |
|recoverableitemsversions  <br/> |Indica la dirección URL de la carpeta versiones de elementos recuperables.  <br/> |
|recoverableitemspurges  <br/> |Indica la dirección URL de la carpeta de elementos recuperables purgados.  <br/> |
|archiveroot  <br/> |Indica la dirección URL de la carpeta raíz de archivo.  <br/> |
|archivemsgfolderroot  <br/> |Indica la dirección URL de la carpeta raíz del mensaje archivado.  <br/> |
|archivedeleteditems  <br/> |Indica la dirección URL de la carpeta de elementos eliminados archivados.  <br/> |
|archiverecoverableitemsroot  <br/> |Indica la dirección URL de la carpeta raíz de elementos recuperables archivados.  <br/> |
|archiverecoverableitemsdeletions  <br/> |Indica la dirección URL de la carpeta de elementos eliminados recuperables archivados.  <br/> |
|archiverecoverableitemsversions  <br/> |Indica la dirección URL de la carpeta de versiones de elementos recuperables archivados.  <br/> |
|archiverecoverableitemspurges  <br/> |Indica la dirección URL de la carpeta de elementos recuperables purgados archivados.  <br/> |
|syncissues  <br/> |Indica la dirección URL de la carpeta de problemas de sincronización.  <br/> |
|conflicts  <br/> |Indica la dirección URL de la carpeta de conflictos.  <br/> |
|localfailures  <br/> |Indica la dirección URL de la carpeta de errores locales.  <br/> |
|serverfailures  <br/> |Indica la dirección URL de la carpeta de errores del servidor.  <br/> |
|recipientcache  <br/> |Indica la dirección URL de la carpeta de caché de destinatarios.  <br/> |
|quickcontacts  <br/> |Indica la dirección URL de la carpeta de contactos rápidos.  <br/> |
|conversationhistory  <br/> |Indica la dirección URL de la carpeta del historial de conversaciones.  <br/> |
|adminauditlogs  <br/> |Indica la dirección URL de la carpeta de registro de auditoría administrativa.  <br/> |
|todosearch  <br/> |Indica la dirección URL de la carpeta de búsqueda.  <br/> |
|mycontacts  <br/> |Indica la dirección URL de la carpeta mis contactos.  <br/> |
|directorio  <br/> |Indica una dirección URL de la carpeta de directorio.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

