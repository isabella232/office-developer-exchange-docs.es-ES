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
description: El elemento DistinguishedFolderId identifica las carpetas que se pueden hacer referencia por su nombre. Si no usa este elemento, debe usar el elemento FolderId para identificar una carpeta.
ms.openlocfilehash: 834166be3d882fa8c0533cfcc2999600430b82ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764250"
---
# <a name="distinguishedfolderid"></a>DistinguishedFolderId

El elemento **DistinguishedFolderId** identifica las carpetas que se pueden hacer referencia por su nombre. Si no usa este elemento, debe usar el elemento [FolderId](folderid.md) para identificar una carpeta. 
  
```XML
<DistinguishedFolderId Id="" ChangeKey="">
   <Mailbox/>
</DistinguishedFolderId>
```

 **DistinguishedFolderIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**Id** <br/> |Contiene una cadena que identifica una carpeta predeterminada. Este atributo es necesario.  <br/> |
|**ChangeKey** <br/> |Contiene una cadena que identifica una versión de una carpeta que se identifica con el atributo **Id** . Este atributo es opcional. Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.  <br/> |
   
#### <a name="id-attribute-values"></a>Valores del atributo ID

|**Valor**|**Descripción**|
|:-----|:-----|
|calendario  <br/> |Representa la carpeta Calendario.  <br/> |
|contactos  <br/> |Representa la carpeta Contactos.  <br/> |
|deleteditems  <br/> |Representa la carpeta Elementos eliminados.  <br/> |
|borradores  <br/> |Representa la carpeta Borradores.  <br/> |
|Bandeja de entrada  <br/> |Representa la carpeta Bandeja de entrada.  <br/> |
|diario  <br/> |Representa la carpeta diario.  <br/> |
|notas  <br/> |Representa la carpeta notas.  <br/> |
|Bandeja de salida  <br/> |Representa la carpeta Bandeja de salida.  <br/> |
|elementos enviados  <br/> |Representa la carpeta Elementos enviados.  <br/> |
|tasks  <br/> |Representa la carpeta tareas.  <br/> |
|msgfolderroot  <br/> |Representa la raíz de la carpeta de mensaje.  <br/> |
|root  <br/> |Representa la raíz del buzón.  <br/> |
|junkemail  <br/> |Representa la carpeta de correo electrónico no deseado.  <br/> |
|SearchFolders  <br/> |Representa la carpeta de las carpetas de búsqueda.  <br/> |
|correo de voz  <br/> |Representa la carpeta de correo de voz.  <br/> |
|recoverableitemsroot  <br/> |Representa el contenedor de carpeta raíz.  <br/> |
|recoverableitemsdeletions  <br/> |Representa el contenedor de carpeta de eliminaciones.  <br/> |
|recoverableitemsversions  <br/> |Representa el contenedor de carpeta de versiones.  <br/> |
|recoverableitemspurges  <br/> |Representa el volcado de archivos purga de la carpeta.  <br/> |
|archiveroot  <br/> |Representa la carpeta raíz del archivo.  <br/> |
|archivemsgfolderroot  <br/> |Representa la carpeta raíz archivar los mensajes.  <br/> |
|archivedeleteditems  <br/> |Representa la carpeta de elementos eliminado del archivo.  <br/> |
|archiveinbox  <br/> |Representa el archivo de la carpeta Bandeja de entrada. Las versiones de Exchange, comenzando por el número de compilación 15.00.0913.09 incluyen este valor.  <br/> |
|archiverecoverableitemsroot  <br/> |Representa la carpeta raíz para archivar elementos recuperables.  <br/> |
|archiverecoverableitemsdeletions  <br/> |Representa la carpeta para archivar elementos recuperables eliminaciones.  <br/> |
|archiverecoverableitemsversions  <br/> |Representa la carpeta de versiones de los elementos recuperables de archivo.  <br/> |
|archiverecoverableitemspurges  <br/> |Representa la carpeta para archivar elementos recuperables purga.  <br/> |
|syncissues  <br/> |Representa la carpeta problemas de sincronización.  <br/> |
|conflictos  <br/> |Representa la carpeta conflictos.  <br/> |
|localfailures  <br/> |Representa la carpeta errores locales.  <br/> |
|serverfailures  <br/> |Representa la carpeta de errores del servidor.  <br/> |
|recipientcache  <br/> |Representa la carpeta de caché del destinatario.  <br/> |
|QuickContacts  <br/> |Representa la carpeta Contactos rápidos.  <br/> |
|conversationhistory  <br/> |Representa la carpeta Historial de conversaciones.  <br/> |
|adminauditlogs  <br/> |Representa la carpeta de registros de auditoría de administrador.  <br/> |
|todosearch  <br/> |Representa la carpeta de búsqueda de tareas pendientes.  <br/> |
|mycontacts  <br/> |Representa la carpeta Mis contactos.  <br/> |
|Active Directory  <br/> |Representa la carpeta de Active directory.  <br/> |
|imcontactlist  <br/> |Representa la carpeta de la lista de contactos de mensajería instantánea.  <br/> |
|peopleconnect  <br/> |Representa las personas conectar carpeta.  <br/> |
|favoritos  <br/> |Representa la carpeta Favoritos.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Buzón de correo](mailbox.md) <br/> |Identifica una dirección SMTP principal. No se permiten las direcciones proxy.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |Indica la carpeta que está destinada a las acciones de conversación que utilizan carpetas.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Indica la carpeta de destino para copiar y mover acciones de conversación.  <br/> |
|[ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> | Identifica la carpeta en la que se crea una nueva carpeta o elemento.  <br/><br/>Los siguientes son las expresiones de XPath para este elemento:<br/><br/>  `/CreateItem/ParentFolderId` <br/><br/>`/CreateFolder/ParentFolderId` <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Identifica las carpetas de búsqueda de la [operación FindItem](finditem-operation.md) y la [operación FindFolder](findfolder-operation.md).  <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |Representa la colección de carpetas que se buscarán para determinar el contenido de una carpeta de búsqueda.  <br/> |
|[FolderIds](folderids.md) <br/> |Contiene una matriz de identificadores de carpeta que se usa para identificar las carpetas para copiar, mover, obtener, eliminar o supervisar para las notificaciones de eventos.  <br/> |
|[FolderChange](folderchange.md) <br/> |Representa una colección de los cambios que se debe realizar en una sola carpeta.  <br/> <br/>La siguiente es la expresión de XPath para este elemento:<br/><br/>`/UpdateFolder/FolderChanges/FolderChange`<br/> |
|[ToFolderId](tofolderid.md) <br/> | Representa la carpeta de destino para un elemento que se ha movido o copiado o una carpeta.<br/><br/>Los siguientes son las expresiones de XPath para este elemento:<br/><br/>`/MoveFolder/ToFolderId`<br/><br/>`/CopyFolder/ToFolderId`<br/><br/>`/MoveItem/ToFolderId`<br/><br/>`/CopyItem/ToFolderId` <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> | Identifica la carpeta de destino para las operaciones que actualizar, enviar y crear elementos en el almacén de Exchange.<br/><br/>Los siguientes son las expresiones de XPath para este elemento:<br/><br/>`/CreateItem/SavedItemFolderId`<br/><br/>`/UpdateItem/SavedItemFolderId`<br/><br/>`/SendItem/SavedItemFolderId` <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Representa la carpeta que contiene los elementos para sincronizar.  <br/> |
|[UserConfigurationName](userconfigurationname.md) <br/> |Representa el nombre de un objeto de configuración de usuario. El nombre del objeto de configuración de usuario es el identificador de un objeto de configuración de usuario.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Representa el identificador de la carpeta de ese correo electrónico elementos se copiarán a.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Representa el identificador de la carpeta de ese correo electrónico que se moverán los elementos a.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Observaciones

Una **DistinguishedFolderId** se resuelve en un **FolderId**. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)
- [Creación de carpetas (servicios Web de Exchange)](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

