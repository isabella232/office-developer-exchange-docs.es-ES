---
title: AdditionalProperties
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AdditionalProperties
api_type:
- schema
ms.assetid: 7a269aed-dcfd-4c3e-9e14-094e53828101
description: El elemento AdditionalProperties identifica propiedades adicionales para su uso en solicitudes GetItem, UpdateItem, CreateItem, FindItem o FindFolder.
ms.openlocfilehash: 9a6fb98e9a88b1e40bd83559b1836d4122f0f125
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522204"
---
# <a name="additionalproperties"></a>AdditionalProperties

El **elemento AdditionalProperties** identifica propiedades adicionales para su uso en solicitudes [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md)o [FindFolder.](findfolder.md) 
  
```xml
<AdditionalProperties>
   <ExtendedFieldURI/>
   <FieldURI/>
   <IndexedFieldURI/>
</AdditionalProperties>
```

 **NonEmptyArrayOfPathsToElementType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifica las propiedades MAPI extendidas para obtener, establecer o crear.  <br/> |
|[FieldURI](fielduri.md) <br/> |Identifica las propiedades a las que se hace referencia con frecuencia mediante URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifica las propiedades de diccionario a las que se hace referencia con frecuencia mediante URI.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> | Identifica las propiedades de carpeta que se incluirán en una [respuesta GetFolder](getfolder.md), [FindFolder](findfolder.md)o [SyncFolderHierarchy.](syncfolderhierarchy.md)<br/><br/>  Las siguientes son las expresiones XPath de este elemento:<br/><br/>  `/FindFolder/FolderShape` <br/>  `/GetFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifica las propiedades y el contenido del elemento que se incluirán en una respuesta [GetItem](getitem.md), [FindItem](finditem.md)o [SyncFolderItems.](syncfolderitems.md)<br/><br/>  Las siguientes son las expresiones XPath de este elemento:<br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
|[AttachmentShape](attachmentshape.md) <br/> |Identifica propiedades de elemento extendidas adicionales para devolver en una respuesta a una [solicitud GetItem.](getitem.md)<br/><br/> A continuación se muestra la expresión XPath de este elemento:<br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="remarks"></a>Comentarios

No todos los elementos secundarios se pueden usar con [solicitudes GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md)o [FindFolder.](findfolder.md) La propiedad debe ser aplicable a la carpeta o elemento al que se tiene acceso. Use propiedades extendidas para obtener acceso a otras propiedades. Si la propiedad no existe para un elemento determinado, no se emitirá ningún elemento correspondiente en el XML resultante. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente. 
  
Este elemento es opcional.
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo de solicitud se muestra cómo obtener un asunto de elemento mediante el **elemento AdditionalProperties.** 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="ASkAS="/>
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   

