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
description: El elemento ItemShape identifica un conjunto de propiedades para devolver en una operación GetItem, operación FindItem o SyncFolderItems respuesta de la operación.
ms.openlocfilehash: 95174a85a8fa05cb2612e1289d46c8db32b6e052
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836191"
---
# <a name="itemshape"></a>ItemShape

El elemento **ItemShape** identifica un conjunto de propiedades para devolver una respuesta [GetItem operation](getitem-operation.md), [operación FindItem](finditem-operation.md)o [SyncFolderItems](syncfolderitems-operation.md) . 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[BaseShape](baseshape.md) <br/> |Identifica la configuración básica de propiedades para devolver una respuesta de elemento o carpeta.  <br/> |
|[IncludeMimeContent](includemimecontent.md) <br/> |Especifica si el contenido de extensiones multipropósito de correo Internet (MIME) de un elemento se devuelve en la respuesta.  <br/> |
|[BodyType](bodytype.md) <br/> |Identifica cómo se da el formato de texto del cuerpo en la respuesta.  <br/> |
|[ConvertHtmlCodePageToUTF8](converthtmlcodepagetoutf8.md) <br/> |Indica si el cuerpo HTML del elemento se convierte en UTF8.  <br/> |
|[FilterHtmlContent](filterhtmlcontent.md) <br/> |Especifica si está habilitado el filtrado de contenido HTML.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |Identifica las propiedades adicionales para devolver en una respuesta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetItem](getitem.md) <br/> |Define una solicitud para recuperar elementos de un buzón en el almacén de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/GetItem` <br/> |
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar todos los elementos que están contenidos en una carpeta.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/FindItem` <br/> |
|[SyncFolderItems](syncfolderitems.md) <br/> |Define una solicitud para sincronizar los elementos en una carpeta de almacén de Exchange.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/SyncFolderItems` <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetItem](getitem-operation.md)
  
[Operación FindItem](finditem-operation.md)
  
[Operación SyncFolderItems](syncfolderitems-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

