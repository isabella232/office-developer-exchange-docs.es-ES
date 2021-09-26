---
title: UpdateItemInRecoverableItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 96259756-322e-4c24-ac76-0cd9c32e0d6d
description: El elemento UpdateItemInRecoverableItemsResponseMessage especifica la respuesta a una solicitud UpdateItemInRecoverableItems.
ms.openlocfilehash: 10112245b27acd736d7985b5cd46944486c7e006
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542781"
---
# <a name="updateiteminrecoverableitemsresponsemessage"></a>UpdateItemInRecoverableItemsResponseMessage

El **elemento UpdateItemInRecoverableItemsResponseMessage** especifica la respuesta a una solicitud **UpdateItemInRecoverableItems.** 
  
```XML
<UpdateItemInRecoverableItemsResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKet/>
   <MessageXml/>
   <Items/>
   <Attachments/>
   <ConflictResults/>
</UpdateItemInRecoverableItemsResponseMessage>
```

 **UpdateItemInRecoverableItemsResponseMessageType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

[MessageText](messagetext.md)  |  [ResponseCode](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [MessageXml](messagexml.md)  |  [Elementos](items.md)  |  [Datos adjuntos](attachments-ex15websvcsotherref.md)  |  [ConflictResults](conflictresults.md)
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|Nombre del esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |Message.xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

