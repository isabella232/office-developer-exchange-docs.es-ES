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
description: El elemento FindFolder define una solicitud para buscar las carpetas en un buzón de correo.
ms.openlocfilehash: d41283547c443e38e2e87379a7224df9c89f901d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764617"
---
# <a name="findfolder"></a>FindFolder

El elemento **FindFolder** define una solicitud para buscar las carpetas en un buzón de correo. 
  
```xml
<FindFolder Traversal="Shallow/Deep/SoftDeleted">
   <FolderShape/>
   <IndexedPageFolderView/>
   <Restriction/>
   <ParentFolderIds/>
</FindFolder>
```

 **FindFolderType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|Cruce seguro del  <br/> |Define cómo se realiza una búsqueda. Este atributo es necesario.  <br/> |
   
#### <a name="traversal-attribute-values"></a>Valores de atributo recorrido

|**Valor**|**Descripción**|
|:-----|:-----|
|Superficial  <br/> |Indica a la operación de FindFolder para buscar sólo la carpeta identificada y devolver sólo la carpeta identificadores para los elementos que no se han eliminado. Esto se denomina un recorrido superficial.  <br/> |
|Profunda  <br/> |Indica a la operación de FindFolder para buscar en todas las carpetas secundarias de la carpeta principal identificado y devolver sólo la carpeta identificadores para los elementos que no se han eliminado. Esto se denomina un recorrido profundo.  <br/> |
|SoftDeleted  <br/> |Indica a la operación FindFolder para realizar una búsqueda de recorrido superficial de los elementos eliminados.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |Identifica las propiedades de carpeta para incluir en una respuesta FindFolder.  <br/> |
|[IndexedPageFolderView](indexedpagefolderview.md) <br/> |Describe cómo paginada elemento de información se devuelve en una respuesta FindFolder. Este elemento es opcional.  <br/> |
|[FractionalPageFolderView](fractionalpagefolderview.md) <br/> |Describe donde se inicia la vista de página y devuelve el número máximo de carpetas en una solicitud FindFolder. Este elemento es opcional.  <br/> |
|[Restriction](restriction.md) <br/> |Define una restricción o una consulta que se usa para filtrar las carpetas en una operación FindFolder. Este elemento es opcional.  <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Identifica las carpetas para la operación FindFolder buscar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="example"></a>Ejemplo

El siguiente ejemplo de una solicitud de FindFolder muestra cómo formar una solicitud para buscar todas las carpetas que se encuentra en una bandeja de entrada.
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindFolder](findfolder-operation.md)

