---
title: EffectiveRights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EffectiveRights
api_type:
- schema
ms.assetid: bf5278eb-3a1a-4d27-9d16-b8be043bb023
description: El elemento EffectiveRights contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta. Este elemento es de sólo lectura.
ms.openlocfilehash: 3055eb73056750508b48ead29136b56e7ce97ee9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459247"
---
# <a name="effectiverights"></a>EffectiveRights

El elemento **EffectiveRights** contiene los derechos del cliente en función de la configuración de los permisos del elemento o carpeta. Este elemento es de sólo lectura. 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CreateAssociated](createassociated.md) <br/> |Indica si un cliente puede crear una tabla de contenido asociada. Esta propiedad solo se usa en objetos Folder.  <br/> |
|[CreateContents](createcontents.md) <br/> |Indica si un cliente puede crear una tabla de contenido. Esta propiedad solo se usa en objetos Folder.  <br/> |
|[CreateHierarchy](createhierarchy.md) <br/> |Indica si un cliente puede crear una tabla de jerarquías. Esta propiedad solo se usa en objetos Folder.  <br/> |
|[Eliminar](delete.md) <br/> |Indica si un cliente puede eliminar una carpeta o un elemento.  <br/> |
|[Modify](modify.md) <br/> |Indica si un cliente puede modificar una carpeta o un elemento.  <br/> |
|[Read](read.md) <br/> |Indica si un cliente puede leer una carpeta o un elemento.  <br/> |
|[ViewPrivateItems](viewprivateitems.md) <br/> |Indica si se puede ver un elemento privado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Representa una carpeta en un buzón.  <br/> |
|[Hubiera](tasksfolder.md) <br/> |Representa una carpeta de tareas en un buzón.  <br/> |
|[Hubiera](contactsfolder.md) <br/> |Representa una carpeta de contactos en un buzón.  <br/> |
|[Hubiera](calendarfolder.md) <br/> |Representa una carpeta de calendario en un buzón.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Representa una carpeta de búsqueda en un buzón.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Representa un elemento de calendario de Exchange.  <br/> |
|[Contacto](contact.md) <br/> |Representa un elemento de contacto de Exchange.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Representa una lista de distribución.  <br/> |
|[Elemento](item.md) <br/> |Representa un elemento de Exchange genérico.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Representa una cancelación de reunión en el almacén de Exchange.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Representa una reunión en el almacén de Exchange.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una convocatoria de reunión en el almacén de Exchange.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Representa una respuesta a una reunión en el almacén de Exchange.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Representa un mensaje de correo electrónico de Exchange.  <br/> |
|[Tarea](task.md) <br/> |Representa una tarea del almacén de Exchange.  <br/> |
|[PostItem](postitem.md) <br/> |Representa un elemento post en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

**EffectiveRights** se admite en las respuestas GetFolder, GetItem, FindFolder, FindItem, SyncFolderHierarchy y SyncFolderItems. La propiedad **EffectiveRights** se expone en la forma **AllProperties** para carpetas y elementos. 
  
Esta propiedad **EffectiveRights** proporciona acceso a la misma información que se proporciona en la propiedad **MAPI PR_ACCESS** . 
  
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
- [Configuración de permisos de nivel de carpeta](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

