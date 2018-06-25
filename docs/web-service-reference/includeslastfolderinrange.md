---
title: IncludesLastFolderInRange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IncludesLastFolderInRange
api_type:
- schema
ms.assetid: 95837904-17be-49b7-831c-de4fb20fccfb
description: El elemento IncludesLastFolderInRange indica si el último elemento para sincronizar se ha incluido en la respuesta.
ms.openlocfilehash: 6c4af5b394ee2fab6bc98f7bb6afa9ee80551869
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835908"
---
# <a name="includeslastfolderinrange"></a>IncludesLastFolderInRange

El elemento **IncludesLastFolderInRange** indica si el último elemento para sincronizar se ha incluido en la respuesta. 
  
[SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)
  
[IncludesLastFolderInRange](includeslastfolderinrange.md)
  
```xml
<IncludesLastFolderInRange/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de SyncFolderHierarchy.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto que representa un valor de tipo Boolean.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación SyncFolderHierarchy](syncfolderhierarchy-operation.md)


[Referencia EWS para Exchange](ews-reference-for-exchange.md)
  
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

