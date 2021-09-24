---
title: ItemShape
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ItemShape
api_type:
- schema
ms.assetid: c5604161-bbc0-40bc-ad75-ff7e837d745f
description: El elemento ItemShape identifica un conjunto de propiedades que se devolverán en una operación GetItem, una operación FindItem o una respuesta de operación SyncFolderItems.
ms.openlocfilehash: d6cc1efc85a8a22e12f2a3616fe949b72b3bba33
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519403"
---
# <a name="itemshape"></a>ItemShape

El **elemento ItemShape** identifica un conjunto de propiedades que se devolverán en una operación [GetItem](getitem-operation.md), [operación FindItem](finditem-operation.md)o respuesta de operación [SyncFolderItems.](syncfolderitems-operation.md) 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[BaseShape](baseshape.md) <br/> |Identifica la configuración básica de las propiedades que se devolverán en una respuesta de elemento o carpeta.  <br/> |
|[IncludeMimeContent](includemimecontent.md) <br/> |Especifica si el contenido de extensiones de correo de Internet multipropósito (MIME) de un elemento se devuelve en la respuesta.  <br/> |
|[BodyType](bodytype.md) <br/> |Identifica cómo se formatea el texto del cuerpo en la respuesta.  <br/> |
|[ConvertHtmlCodePageToUTF8](converthtmlcodepagetoutf8.md) <br/> |Indica si el cuerpo HTML del elemento se convierte en UTF8.  <br/> |
|[FilterHtmlContent](filterhtmlcontent.md) <br/> |Especifica si el filtrado de contenido HTML está habilitado.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |Identifica propiedades adicionales para devolver en una respuesta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetItem](getitem.md) <br/> |Define una solicitud para recuperar elementos de un buzón de correo en el Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/GetItem` <br/> |
|[FindItem](finditem.md) <br/> |Define una solicitud para buscar todos los elementos contenidos en una carpeta.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/FindItem` <br/> |
|[SyncFolderItems](syncfolderitems.md) <br/> |Define una solicitud para sincronizar elementos en una carpeta Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/SyncFolderItems` <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetItem](getitem-operation.md)
  
[Operación FindItem](finditem-operation.md)
  
[Operación SyncFolderItems](syncfolderitems-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

