---
title: FolderShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FolderShape
api_type:
- schema
ms.assetid: 244f4f46-a33d-4764-92e3-1bddb4dc6a49
description: El elemento FolderShape identifica las propiedades de carpeta que se incluirán en una respuesta GetFolder, FindFolder o SyncFolderHierarchy.
ms.openlocfilehash: 530c9f25f17a3eba8549535bf7be37038a58c921
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518361"
---
# <a name="foldershape"></a>FolderShape

El **elemento FolderShape** identifica las propiedades de carpeta que se incluirán en una respuesta [GetFolder](getfolder.md), [FindFolder](findfolder.md)o [SyncFolderHierarchy.](syncfolderhierarchy.md) 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[BaseShape](baseshape.md) <br/> |Identifica la configuración básica de las propiedades que se devolverán en una respuesta.  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |Identifica propiedades adicionales para devolver en una respuesta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |Define una solicitud para identificar carpetas de un buzón.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/FindFolder` <br/> |
|[GetFolder](getfolder.md) <br/> |Define una solicitud para obtener una carpeta del Exchange almacén.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/GetFolder` <br/> |
|[SyncFolderHierarchy](syncfolderhierarchy.md) <br/> |Define una solicitud para sincronizar una jerarquía de carpetas en un cliente.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/SyncFolderHierarchy` <br/> |
   
## <a name="remarks"></a>Comentarios

El **elemento FolderShape** es un elemento secundario necesario del [elemento FindFolder.](findfolder.md) 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo de una solicitud se muestra cómo buscar todas las carpetas ubicadas en el primer nivel de la carpeta Bandeja de entrada.
  
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
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[FindFolder](findfolder.md)

