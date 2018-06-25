---
title: AdditionalProperties
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AdditionalProperties
api_type:
- schema
ms.assetid: 7a269aed-dcfd-4c3e-9e14-094e53828101
description: El elemento AdditionalProperties identifica propiedades adicionales para su uso en GetItem, UpdateItem, CreateItem, FindItem o solicitudes FindFolder.
ms.openlocfilehash: 64e4f1ee6b24cf8015b7893dc4a904ca8b32d58e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763404"
---
# <a name="additionalproperties"></a>AdditionalProperties

El elemento **AdditionalProperties** identifica propiedades adicionales para su uso en [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md)o solicitudes [FindFolder](findfolder.md) . 
  
```xml
<AdditionalProperties>
   <ExtendedFieldURI/>
   <FieldURI/>
   <IndexedFieldURI/>
</AdditionalProperties>
```

 **NonEmptyArrayOfPathsToElementType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifica las propiedades extendidas de MAPI para obtener, establecer o crear.  <br/> |
|[FieldURI](fielduri.md) <br/> |Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifica las propiedades de diccionario con frecuencia que se hace referencia mediante un identificador URI.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> | Identifica las propiedades de carpeta para incluir en una respuesta [GetFolder](getfolder.md), [FindFolder](findfolder.md)o [SyncFolderHierarchy](syncfolderhierarchy.md) .<br/><br/>  Los siguientes son las expresiones de XPath para este elemento:<br/><br/>  `/FindFolder/FolderShape` <br/>  `/GetFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifica las propiedades de elemento y el contenido que desea incluir en una respuesta [GetItem](getitem.md), [FindItem](finditem.md)o [SyncFolderItems](syncfolderitems.md) .<br/><br/>  Los siguientes son las expresiones de XPath para este elemento:<br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
|[AttachmentShape](attachmentshape.md) <br/> |Identifica las propiedades adicionales total del artículo para devolver en una respuesta a una solicitud de [GetItem](getitem.md) .<br/><br/> La siguiente es la expresión de XPath para este elemento:<br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="remarks"></a>Comentarios

No todos los elementos secundarios pueden usarse con [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md)o solicitudes [FindFolder](findfolder.md) . La propiedad debe ser aplicable a la carpeta o elemento que se tiene acceso. Utilice las propiedades extendidas para tener acceso a otras propiedades. Si la propiedad no existe para un elemento determinado, no se emitirá ningún elemento correspondiente en el XML resultante. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente. 
  
Este elemento es opcional.
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo de solicitud muestra cómo obtener a un asunto del elemento mediante el elemento **AdditionalProperties** . 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   

