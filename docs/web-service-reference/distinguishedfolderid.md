---
title: DistinguishedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DistinguishedFolderId
api_type:
- schema
ms.assetid: 50018162-2941-4227-8a5b-d6b4686bb32f
description: El elemento DistinguishedFolderId identifica las carpetas a las que se puede hacer referencia por su nombre. Si no usa este elemento, debe usar el elemento FolderId para identificar una carpeta.
ms.openlocfilehash: 309db925bb783c435320aeb283915ece39da2271
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522001"
---
# <a name="distinguishedfolderid"></a>DistinguishedFolderId

El **elemento DistinguishedFolderId** identifica las carpetas a las que se puede hacer referencia por su nombre. Si no usa este elemento, debe usar el [elemento FolderId](folderid.md) para identificar una carpeta. 
  
```XML
<DistinguishedFolderId Id="" ChangeKey="">
   <Mailbox/>
</DistinguishedFolderId>
```

 **DistinguishedFolderIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Id** <br/> |Contiene una cadena que identifica una carpeta predeterminada. Este atributo es obligatorio.  <br/> |
|**ChangeKey** <br/> |Contiene una cadena que identifica una versión de una carpeta identificada por el **atributo Id.** Este atributo es opcional. Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.  <br/> |
   
#### <a name="id-attribute-values"></a>Valores de atributo Id

|**Valor**|**Descripción**|
|:-----|:-----|
|calendar  <br/> |Representa la carpeta Calendario.  <br/> |
|contacts  <br/> |Representa la carpeta Contactos.  <br/> |
|deleteditems  <br/> |Representa la carpeta Elementos eliminados.  <br/> |
|drafts  <br/> |Representa la carpeta Borradores.  <br/> |
|inbox  <br/> |Representa la carpeta Bandeja de entrada.  <br/> |
|diario  <br/> |Representa la carpeta Journal.  <br/> |
|notas  <br/> |Representa la carpeta Notas.  <br/> |
|outbox  <br/> |Representa la carpeta Bandeja de salida.  <br/> |
|sentitems  <br/> |Representa la carpeta Elementos enviados.  <br/> |
|tasks  <br/> |Representa la carpeta Tareas.  <br/> |
|msgfolderroot  <br/> |Representa la raíz de la carpeta de mensajes.  <br/> |
|root  <br/> |Representa la raíz del buzón.  <br/> |
|junkemail  <br/> |Representa la carpeta Correo no deseado.  <br/> |
|searchfolders  <br/> |Representa la carpeta Carpetas de búsqueda.  <br/> |
|correo de voz  <br/> |Representa la carpeta Correo de voz.  <br/> |
|recoverableitemsroot  <br/> |Representa la carpeta raíz del contenedor.  <br/> |
|recoverableitemsdeletions  <br/> |Representa la carpeta eliminaciones del contenedor.  <br/> |
|recoverableitemsversions  <br/> |Representa la carpeta de versiones del contenedor.  <br/> |
|recoverableitemspurges  <br/> |Representa la carpeta purga del contenedor.  <br/> |
|archiveroot  <br/> |Representa la carpeta de archivo raíz.  <br/> |
|archivemsgfolderroot  <br/> |Representa la carpeta de mensajes de archivo raíz.  <br/> |
|archivedeleteditems  <br/> |Representa la carpeta de elementos eliminados de archivo.  <br/> |
|archiveinbox  <br/> |Representa la carpeta Bandeja de entrada de archivo. Las versiones Exchange a partir del número de compilación 15.00.0913.09 incluyen este valor.  <br/> |
|archiverecoverableitemsroot  <br/> |Representa la carpeta raíz de elementos recuperables de archivo.  <br/> |
|archiverecoverableitemsdeletions  <br/> |Representa la carpeta eliminaciones de elementos recuperables de archivo.  <br/> |
|archiverecoverableitemsversions  <br/> |Representa la carpeta de versiones de elementos recuperables de archivo.  <br/> |
|archiverecoverableitemspurges  <br/> |Representa la carpeta purgar elementos recuperables de archivo.  <br/> |
|syncissues  <br/> |Representa la carpeta de problemas de sincronización.  <br/> |
|conflicts  <br/> |Representa la carpeta de conflictos.  <br/> |
|localfailures  <br/> |Representa la carpeta de errores locales.  <br/> |
|serverfailures  <br/> |Representa la carpeta de errores del servidor.  <br/> |
|recipientcache  <br/> |Representa la carpeta de caché de destinatarios.  <br/> |
|quickcontacts  <br/> |Representa la carpeta de contactos rápidos.  <br/> |
|conversationhistory  <br/> |Representa la carpeta historial de conversaciones.  <br/> |
|adminauditlogs  <br/> |Representa la carpeta registros de auditoría de administración.  <br/> |
|todosearch  <br/> |Representa la carpeta de búsqueda todo.  <br/> |
|mycontacts  <br/> |Representa la carpeta Mis contactos.  <br/> |
|directorio  <br/> |Representa la carpeta de directorio.  <br/> |
|imcontactlist  <br/> |Representa la carpeta de lista de contactos de mensajería instantánea.  <br/> |
|peopleconnect  <br/> |Representa la carpeta de conexión de personas.  <br/> |
|favoritos  <br/> |Representa la carpeta Favoritos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Buzón](mailbox.md) <br/> |Identifica una dirección SMTP principal. Las direcciones proxy no están permitidas.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |Indica la carpeta destinada a las acciones de conversación que usan carpetas.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Indica la carpeta de destino para copiar y mover acciones de conversación.  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> | Identifica la carpeta en la que se crea una nueva carpeta o elemento.  <br/><br/>Las siguientes son las expresiones XPath de este elemento:<br/><br/>  `/CreateItem/ParentFolderId` <br/><br/>`/CreateFolder/ParentFolderId` <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Identifica las carpetas para buscar la [operación FindItem](finditem-operation.md) y la [operación FindFolder](findfolder-operation.md).  <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |Representa la colección de carpetas que se buscarán para determinar el contenido de una carpeta de búsqueda.  <br/> |
|[FolderIds](folderids.md) <br/> |Contiene una matriz de identificadores de carpeta que se usan para identificar carpetas para copiar, mover, obtener, eliminar o supervisar las notificaciones de eventos.  <br/> |
|[FolderChange](folderchange.md) <br/> |Representa una colección de cambios que se deben realizar en una sola carpeta.  <br/> <br/>A continuación se muestra la expresión XPath de este elemento:<br/><br/>`/UpdateFolder/FolderChanges/FolderChange`<br/> |
|[ToFolderId](tofolderid.md) <br/> | Representa la carpeta de destino de un elemento o carpeta copiados o movidos.<br/><br/>Las siguientes son las expresiones XPath de este elemento:<br/><br/>`/MoveFolder/ToFolderId`<br/><br/>`/CopyFolder/ToFolderId`<br/><br/>`/MoveItem/ToFolderId`<br/><br/>`/CopyItem/ToFolderId` <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> | Identifica la carpeta de destino para las operaciones que actualizan, envían y crean elementos en el Exchange almacén.<br/><br/>Las siguientes son las expresiones XPath de este elemento:<br/><br/>`/CreateItem/SavedItemFolderId`<br/><br/>`/UpdateItem/SavedItemFolderId`<br/><br/>`/SendItem/SavedItemFolderId` <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Representa la carpeta que contiene los elementos que se deben sincronizar.  <br/> |
|[UserConfigurationName](userconfigurationname.md) <br/> |Representa el nombre de un objeto de configuración de usuario. El nombre del objeto de configuración de usuario es el identificador de un objeto de configuración de usuario.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Representa el identificador de la carpeta en la que se copiarán los elementos de correo electrónico.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Representa el identificador de la carpeta a la que se van a mover los elementos de correo electrónico.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Un **DistinguishedFolderId** se resuelve en **un FolderId**. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)
- [Creación de carpetas (Exchange Web Services)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

