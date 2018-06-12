---
title: GetItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: 769df8eb-9c72-48b5-a49f-82c6b86bc5fc
description: El elemento GetItem define una solicitud para obtener un elemento de un buzón en el almacén de Exchange.
ms.openlocfilehash: 39db141bad62c34bec5ae6a937ba94c2d1288090
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764896"
---
# <a name="getitem"></a>GetItem

El elemento **GetItem** define una solicitud para obtener un elemento de un buzón en el almacén de Exchange. 
  
```xml
<GetItem>
   <ItemShape/>
   <ItemIds/>
</GetItem>
```

 **GetItemType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |Identifica las propiedades de elemento y el contenido que desea incluir en una respuesta **GetItem** .  <br/> |
|[ItemId](itemids.md) <br/> |Contiene las identidades únicas de los elementos, elementos de aparición y elementos maestros periódicos que se usan para obtener los elementos desde el almacén de Exchange. Estos elementos representan los contactos, tareas, los mensajes, elementos de calendario, convocatorias de reunión y otros elementos válidos en un buzón de correo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetItem](getitem-operation.md)

