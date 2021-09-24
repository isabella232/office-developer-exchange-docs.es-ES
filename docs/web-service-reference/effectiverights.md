---
title: EffectiveRights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- EffectiveRights
api_type:
- schema
ms.assetid: bf5278eb-3a1a-4d27-9d16-b8be043bb023
description: El elemento EffectiveRights contiene los derechos del cliente en función de la configuración de permisos del elemento o carpeta. Este elemento es de solo lectura.
ms.openlocfilehash: a3207a9971065d3b69b6a0b7056fa8012425fd5b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514714"
---
# <a name="effectiverights"></a>EffectiveRights

El **elemento EffectiveRights** contiene los derechos del cliente en función de la configuración de permisos del elemento o carpeta. Este elemento es de solo lectura. 
  
```XML
<EffectiveRights>
   <CreateAssociated/>
   <CreateContents/>
   <CreateHierarchy/>
   <Delete/>
   <Modify/>
   <Read/>
   <ViewPrivateItems/>
</EffectiveRights>
```

 **EffectiveRightsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CreateAssociated](createassociated.md) <br/> |Indica si un cliente puede crear una tabla de contenido asociada. Esta propiedad solo se usa en objetos de carpeta.  <br/> |
|[CreateContents](createcontents.md) <br/> |Indica si un cliente puede crear una tabla de contenido. Esta propiedad solo se usa en objetos de carpeta.  <br/> |
|[CreateHierarchy](createhierarchy.md) <br/> |Indica si un cliente puede crear una tabla de jerarquía. Esta propiedad solo se usa en objetos de carpeta.  <br/> |
|[Eliminar](delete.md) <br/> |Indica si un cliente puede eliminar una carpeta o un elemento.  <br/> |
|[Modify](modify.md) <br/> |Indica si un cliente puede modificar una carpeta o un elemento.  <br/> |
|[Lectura](read.md) <br/> |Indica si un cliente puede leer una carpeta o un elemento.  <br/> |
|[ViewPrivateItems](viewprivateitems.md) <br/> |Indica si se puede ver un elemento privado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Representa una carpeta de un buzón.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Representa una carpeta de tareas en un buzón.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Representa una carpeta de contactos en un buzón.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Representa una carpeta de calendario en un buzón.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda en un buzón.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
|[Contact](contact.md) <br/> |Representa un Exchange de contacto.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento Exchange genérico.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el Exchange local.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el Exchange almacén.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta de reunión en Exchange almacén.  <br/> |
|[Mensaje](message-ex15websvcsotherref.md) <br/> |Representa un Exchange de correo electrónico.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea en el Exchange almacén.  <br/> |
|[PostItem](postitem.md) <br/> |Representa un elemento de publicación en el Exchange almacén.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

**EffectiveRights** se admite en las respuestas GetFolder, GetItem, FindFolder, FindItem, SyncFolderHierarchy y SyncFolderItems. La **propiedad EffectiveRights** se expone en la **forma AllProperties** para carpetas y elementos. 
  
Esta **propiedad EffectiveRights** proporciona acceso a la misma información que se proporciona en la **PR_ACCESS mapi.** 
  
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
- [Configuración Folder-Level permisos](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

