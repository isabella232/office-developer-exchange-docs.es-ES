---
title: ItemShape
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemShape
api_type:
- schema
ms.assetid: c5604161-bbc0-40bc-ad75-ff7e837d745f
description: El elemento ItemShape identifica un conjunto de propiedades que se devolverán en una operación GetItem, la operación FindItem o la respuesta de operación SyncFolderItems.
ms.openlocfilehash: ffb666ee331b55a4f04cad076c705e4bec980e03
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458127"
---
# <a name="itemshape"></a>ItemShape

El elemento **ItemShape** identifica un conjunto de propiedades que se devolverán en una [operación GetItem](getitem-operation.md), la [operación FindItem](finditem-operation.md)o la respuesta de [operación SyncFolderItems](syncfolderitems-operation.md) . 
  
```XML
<ItemShape>
   <BaseShape/>
   <IncludeMimeContent/>
   <BodyType/>
   <FilterHtmlContent/>
   <ConvertHtmlCodePageToUTF8/>
   <AdditionalProperties/>
</ItemShape>
```

 **ItemResponseShapeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[BaseShape](baseshape.md) <br/> |Identifica la configuración básica de las propiedades que se devolverán en una respuesta de elemento o carpeta.  <br/> |
|[IncludeMimeContent](includemimecontent.md) <br/> |Especifica si se devuelve el contenido de extensiones multipropósito de correo Internet (MIME) de un elemento en la respuesta.  <br/> |
|[BodyType](bodytype.md) <br/> |Identifica cómo se aplica formato al texto del cuerpo en la respuesta.  <br/> |
|[ConvertHtmlCodePageToUTF8](converthtmlcodepagetoutf8.md) <br/> |Indica si el cuerpo HTML del elemento se convierte en UTF8.  <br/> |
|[FilterHtmlContent](filterhtmlcontent.md) <br/> |Especifica si está habilitado el filtrado de contenido HTML.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |Identifica las propiedades adicionales que se devolverán en una respuesta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetItem](getitem.md) <br/> |Define una solicitud para recuperar elementos de un buzón de correo en el almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/GetItem` <br/> |
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar todos los elementos que se encuentran en una carpeta.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/FindItem` <br/> |
|[SyncFolderItems](syncfolderitems.md) <br/> |Define una solicitud para sincronizar elementos en una carpeta de almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/SyncFolderItems` <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetItem](getitem-operation.md)
  
[Operación FindItem](finditem-operation.md)
  
[Operación SyncFolderItems](syncfolderitems-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

