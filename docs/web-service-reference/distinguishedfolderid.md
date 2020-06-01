---
title: DistinguishedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DistinguishedFolderId
api_type:
- schema
ms.assetid: 50018162-2941-4227-8a5b-d6b4686bb32f
description: El elemento DistinguishedFolderId identifica las carpetas a las que se puede hacer referencia por su nombre. Si no usa este elemento, debe usar el elemento FolderId para identificar una carpeta.
ms.openlocfilehash: be883cbca00910b24e4c45ba047803e5a5024566
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462699"
---
# <a name="distinguishedfolderid"></a>DistinguishedFolderId

El elemento **DistinguishedFolderId** identifica las carpetas a las que se puede hacer referencia por su nombre. Si no usa este elemento, debe usar el elemento [FolderId](folderid.md) para identificar una carpeta. 
  
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
|**ChangeKey** <br/> |Contiene una cadena que identifica una versión de una carpeta identificada por el atributo **ID** . Este atributo es opcional. Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.  <br/> |
   
#### <a name="id-attribute-values"></a>Valores del atributo ID

|**Valor**|**Descripción**|
|:-----|:-----|
|calendario  <br/> |Representa la carpeta calendario.  <br/> |
|contacts  <br/> |Representa la carpeta contactos.  <br/> |
|deleteditems  <br/> |Representa la carpeta elementos eliminados.  <br/> |
|drafts  <br/> |Representa la carpeta Borradores.  <br/> |
|inbox  <br/> |Representa la carpeta Bandeja de entrada.  <br/> |
|Agenda  <br/> |Representa la carpeta diario.  <br/> |
|notas  <br/> |Representa la carpeta notas.  <br/> |
|outbox  <br/> |Representa la carpeta Bandeja de salida.  <br/> |
|sentitems  <br/> |Representa la carpeta elementos enviados.  <br/> |
|tasks  <br/> |Representa la carpeta tareas.  <br/> |
|msgfolderroot  <br/> |Representa la raíz de la carpeta de mensajes.  <br/> |
|root  <br/> |Representa la raíz del buzón.  <br/> |
|junkemail  <br/> |Representa la carpeta de correo no deseado.  <br/> |
|searchfolders  <br/> |Representa la carpeta carpetas de búsqueda.  <br/> |
|correo de voz  <br/> |Representa la carpeta de correo de voz.  <br/> |
|recoverableitemsroot  <br/> |Representa la carpeta raíz del contenedor.  <br/> |
|recoverableitemsdeletions  <br/> |Representa la carpeta eliminaciones de contenedor.  <br/> |
|recoverableitemsversions  <br/> |Representa la carpeta versiones del contenedor.  <br/> |
|recoverableitemspurges  <br/> |Representa la carpeta de depuraciones de contenedor.  <br/> |
|archiveroot  <br/> |Representa la carpeta de archivo raíz.  <br/> |
|archivemsgfolderroot  <br/> |Representa la carpeta de mensajes del archivo raíz.  <br/> |
|archivedeleteditems  <br/> |Representa la carpeta archivar elementos eliminados.  <br/> |
|archiveinbox  <br/> |Representa la carpeta Bandeja de entrada de archivo. Las versiones de Exchange que comienzan con el número de compilación 15.00.0913.09 incluyen este valor.  <br/> |
|archiverecoverableitemsroot  <br/> |Representa la carpeta raíz de elementos recuperables de archivo.  <br/> |
|archiverecoverableitemsdeletions  <br/> |Representa la carpeta de eliminaciones de elementos recuperables de archivo.  <br/> |
|archiverecoverableitemsversions  <br/> |Representa la carpeta de versiones de elementos recuperables de archivo.  <br/> |
|archiverecoverableitemspurges  <br/> |Representa la carpeta archivos de depuración de elementos recuperables de archivo.  <br/> |
|syncissues  <br/> |Representa la carpeta problemas de sincronización.  <br/> |
|conflicts  <br/> |Representa la carpeta conflictos.  <br/> |
|localfailures  <br/> |Representa la carpeta errores locales.  <br/> |
|serverfailures  <br/> |Representa la carpeta errores del servidor.  <br/> |
|recipientcache  <br/> |Representa la carpeta de caché de destinatarios.  <br/> |
|QuickContacts  <br/> |Representa la carpeta contactos rápidos.  <br/> |
|conversationhistory  <br/> |Representa la carpeta Historial de conversaciones.  <br/> |
|adminauditlogs  <br/> |Representa la carpeta registros de auditoría de administrador.  <br/> |
|todosearch  <br/> |Representa la carpeta de búsqueda todo.  <br/> |
|mycontacts  <br/> |Representa la carpeta Mis contactos.  <br/> |
|Active  <br/> |Representa la carpeta del directorio.  <br/> |
|imcontactlist  <br/> |Representa la carpeta de la lista de contactos de mensajería instantánea.  <br/> |
|peopleconnect  <br/> |Representa la carpeta personas Connect.  <br/> |
|Favoritos  <br/> |Representa la carpeta favoritos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Buzón](mailbox.md) <br/> |Identifica una dirección SMTP principal. No se permiten direcciones proxy.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |Indica la carpeta que está destinada a las acciones de conversación que usan carpetas.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Indica la carpeta de destino para las acciones de copiar y mover la conversación.  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> | Identifica la carpeta en la que se crea una nueva carpeta o elemento.  <br/><br/>Las siguientes son las expresiones XPath de este elemento:<br/><br/>  `/CreateItem/ParentFolderId` <br/><br/>`/CreateFolder/ParentFolderId` <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Identifica las carpetas para buscar la [operación FindItem](finditem-operation.md) y la [operación FindFolder](findfolder-operation.md).  <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |Representa la colección de carpetas en las que se va a buscar para determinar el contenido de una carpeta de búsqueda.  <br/> |
|[FolderIds](folderids.md) <br/> |Contiene una matriz de identificadores de carpeta que se usan para identificar las carpetas que se van a copiar, mover, obtener, eliminar o supervisar las notificaciones de eventos.  <br/> |
|[FolderChange](folderchange.md) <br/> |Representa una colección de cambios que se van a realizar en una sola carpeta.  <br/> <br/>La siguiente es la expresión XPath a este elemento:<br/><br/>`/UpdateFolder/FolderChanges/FolderChange`<br/> |
|[ToFolderId](tofolderid.md) <br/> | Representa la carpeta de destino de un elemento o carpeta que se ha copiado o movido.<br/><br/>Las siguientes son las expresiones XPath de este elemento:<br/><br/>`/MoveFolder/ToFolderId`<br/><br/>`/CopyFolder/ToFolderId`<br/><br/>`/MoveItem/ToFolderId`<br/><br/>`/CopyItem/ToFolderId` <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> | Identifica la carpeta de destino para las operaciones que actualizan, envían y crean elementos en el almacén de Exchange.<br/><br/>Las siguientes son las expresiones XPath de este elemento:<br/><br/>`/CreateItem/SavedItemFolderId`<br/><br/>`/UpdateItem/SavedItemFolderId`<br/><br/>`/SendItem/SavedItemFolderId` <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Representa la carpeta que contiene los elementos que se van a sincronizar.  <br/> |
|[UserConfigurationName](userconfigurationname.md) <br/> |Representa el nombre de un objeto de configuración de usuario. El nombre del objeto de configuración de usuario es el identificador de un objeto de configuración de usuario.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Representa el identificador de la carpeta en la que se copiarán los elementos de correo electrónico.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Representa el identificador de la carpeta a la que se moverán los elementos de correo electrónico.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Una **DistinguishedFolderId** se resuelve como un **FolderId**. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)
- [Creación de carpetas (servicios Web de Exchange)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

