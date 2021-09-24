---
title: FindFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FindFolder
api_type:
- schema
ms.assetid: b8a59740-d978-454c-9629-a10792385ba0
description: El elemento FindFolder define una solicitud para buscar carpetas en un buzón.
ms.openlocfilehash: 431efde28e417efec04f6fa1625a81b3766cb705
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518445"
---
# <a name="findfolder"></a>FindFolder

El **elemento FindFolder** define una solicitud para buscar carpetas en un buzón. 
  
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
|Traversal  <br/> |Define cómo se realiza una búsqueda. Este atributo es obligatorio.  <br/> |
   
#### <a name="traversal-attribute-values"></a>Valores de atributo Traversal

|**Valor**|**Descripción**|
|:-----|:-----|
|Superficial  <br/> |Indica a la operación FindFolder que busque solo la carpeta identificada y que devuelva solo los id. de carpeta para los elementos que no se han eliminado. Esto se denomina un recorrido superficial.  <br/> |
|Deep  <br/> |Indica a la operación FindFolder que busque en todas las carpetas secundarias de la carpeta principal identificada y que devuelva solo los id. de carpeta para los elementos que no se han eliminado. Esto se denomina recorrido profundo.  <br/> |
|SoftDeleted  <br/> |Indica a la operación FindFolder que realice una búsqueda transversal superficial de los elementos eliminados.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |Identifica las propiedades de carpeta que se incluirán en una respuesta FindFolder.  <br/> |
|[IndexedPageFolderView](indexedpagefolderview.md) <br/> |Describe cómo se devuelve la información del elemento paginado en una respuesta FindFolder. Este elemento es opcional.  <br/> |
|[FractionalPageFolderView](fractionalpagefolderview.md) <br/> |Describe dónde se inicia la vista paginada y el número máximo de carpetas devueltas en una solicitud FindFolder. Este elemento es opcional.  <br/> |
|[Restriction](restriction.md) <br/> |Define una restricción o consulta que se usa para filtrar carpetas en una operación FindFolder. Este elemento es opcional.  <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Identifica las carpetas de la operación FindFolder que se buscarán.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo de una solicitud FindFolder se muestra cómo formar una solicitud para buscar todas las carpetas ubicadas en una Bandeja de entrada.
  
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
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación FindFolder](findfolder-operation.md)

