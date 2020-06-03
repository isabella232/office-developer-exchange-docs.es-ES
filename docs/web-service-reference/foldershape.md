---
title: FolderShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderShape
api_type:
- schema
ms.assetid: 244f4f46-a33d-4764-92e3-1bddb4dc6a49
description: El elemento FolderShape identifica las propiedades de carpeta que se deben incluir en una respuesta GetFolder, FindFolder o SyncFolderHierarchy.
ms.openlocfilehash: f841fcc4570604c474387dfa24ec07c9d2784f62
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461348"
---
# <a name="foldershape"></a>FolderShape

El elemento **FolderShape** identifica las propiedades de carpeta que se deben incluir en una respuesta [GetFolder](getfolder.md), [FindFolder](findfolder.md)o [SyncFolderHierarchy](syncfolderhierarchy.md) . 
  
```xml
<FolderShape>
   <BaseShape/>
   <AdditionalProperties/>
</FolderShape>
```

 **FolderResponseShapeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[BaseShape](baseshape.md) <br/> |Identifica la configuración básica de las propiedades que se van a devolver en una respuesta.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |Identifica las propiedades adicionales que se devolverán en una respuesta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Define una solicitud para identificar las carpetas en un buzón.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/FindFolder` <br/> |
|[GetFolder](getfolder.md) <br/> |Define una solicitud para obtener una carpeta del almacén de Exchange.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/GetFolder` <br/> |
|[SyncFolderHierarchy](syncfolderhierarchy.md) <br/> |Define una solicitud para sincronizar una jerarquía de carpetas en un cliente.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/SyncFolderHierarchy` <br/> |
   
## <a name="remarks"></a>Comentarios

El elemento **FolderShape** es un elemento secundario necesario del elemento [FindFolder](findfolder.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="example"></a>Ejemplo

El siguiente ejemplo de una solicitud muestra cómo buscar todas las carpetas que se encuentran en el primer nivel de la carpeta Bandeja de entrada.
  
```
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



[FindFolder](findfolder.md)

