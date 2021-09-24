---
title: UpdateItemInRecoverableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c49816b1-dbb5-4716-86c7-30790e86f30e
description: El elemento UpdateItemInRecoverableItems especifica una solicitud para actualizar un elemento en elementos recuperables.
ms.openlocfilehash: 8d3ffdd2d3f60e48514ae1a9d7cb4ca4e1bf06ac
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515022"
---
# <a name="updateiteminrecoverableitems"></a>UpdateItemInRecoverableItems

El **elemento UpdateItemInRecoverableItems** especifica una solicitud para actualizar un elemento en elementos recuperables. 
  
```XML
<UpdateItemInRecoverableItems>
   <ItemId/>
   <Updates/>
   <Attachments/>
   <MakeItemImmutable/>
</UpdateItemInRecoverableItems>
```

 **UpdateItemInRecoverableItemsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[ItemId](itemid.md)  |  [Actualizaciones (elemento)](updates-item.md)  |  [Datos adjuntos](attachments-ex15websvcsotherref.md)  |  [MakeItemImmutable](makeitemimmutable.md)
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

