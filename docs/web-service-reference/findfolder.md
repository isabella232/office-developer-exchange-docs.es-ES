---
title: FindFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindFolder
api_type:
- schema
ms.assetid: b8a59740-d978-454c-9629-a10792385ba0
description: El elemento FindFolder define una solicitud para buscar carpetas en un buzón.
ms.openlocfilehash: 248047206a661afe723543e52c51b57847148423
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462580"
---
# <a name="findfolder"></a>FindFolder

El elemento **FindFolder** define una solicitud para buscar carpetas en un buzón. 
  
```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <IndexedPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <FractionalPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

**FindFolderType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|Transversal  <br/> |Define cómo se realiza una búsqueda. Este atributo es obligatorio.  <br/> |
   
#### <a name="traversal-attribute-values"></a>Valores de atributo de recorrido

|**Valor**|**Descripción**|
|:-----|:-----|
|Profunda  <br/> |Indica a la operación FindFolder que busque sólo en la carpeta identificada y que devuelva sólo los identificadores de la carpeta para los elementos que no se han eliminado. Esto se denomina recorrido superficial.  <br/> |
|Gran  <br/> |Indica a la operación FindFolder que busque en todas las carpetas secundarias de la carpeta principal identificada y que devuelva sólo los identificadores de carpeta de los elementos que no se han eliminado. Esto se denomina recorrido profundo.  <br/> |
|SoftDeleted  <br/> |Indica a la operación FindFolder que realice una búsqueda de recorrido superficial para los elementos eliminados.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |Identifica las propiedades de carpeta que se deben incluir en una respuesta FindFolder.  <br/> |
|[IndexedPageFolderView](indexedpagefolderview.md) <br/> |Describe cómo se devuelve la información de elementos paginados en una respuesta FindFolder. Este elemento es opcional.  <br/> |
|[FractionalPageFolderView](fractionalpagefolderview.md) <br/> |Describe dónde se inicia la vista paginada y el número máximo de carpetas que se devuelven en una solicitud FindFolder. Este elemento es opcional.  <br/> |
|[Restriction](restriction.md) <br/> |Define una restricción o consulta que se usa para filtrar las carpetas en una operación FindFolder. Este elemento es opcional.  <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Identifica las carpetas para la operación FindFolder que se va a buscar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="example"></a>Ejemplo

El siguiente ejemplo de una solicitud FindFolder muestra cómo crear una solicitud para buscar todas las carpetas que se encuentran en una bandeja de entrada.
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación FindFolder](findfolder-operation.md)

