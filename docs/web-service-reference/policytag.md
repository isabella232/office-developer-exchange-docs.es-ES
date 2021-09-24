---
title: PolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: fa4b1447-dc7b-47ad-a677-78fcee443dc6
description: El elemento PolicyTag especifica el identificador de retención en un elemento o carpeta.
ms.openlocfilehash: 16759748dded6978e68450a6b8d504dd378c04be
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519257"
---
# <a name="policytag"></a>PolicyTag

El **elemento PolicyTag** especifica el identificador de retención en un elemento o carpeta. 
  
```xml
<PolicyTag IsExplicit="true | false"></PolicyTag>
```

 **RetentionTagType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|IsExplicit  <br/> |Indica si una etiqueta de directiva se estableció explícitamente en un elemento o carpeta.  <br/> Un valor de texto **de true** para el atributo **IsExplicit** indica que la etiqueta de directiva se estableció explícitamente en el elemento o carpeta. Un valor de texto de **false** indica que la etiqueta de directiva se estableció implícitamente en el elemento o carpeta en función de la etiqueta de directiva de carpetas primarias.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[SearchPreviewItem](searchpreviewitem.md)  |  [Elemento](item.md)  |  [Contacto](contact.md)  |  [Mensaje](message-ex15websvcsotherref.md)  |  [DistributionList](distributionlist.md)  |  [CalendarItem](calendaritem.md)  |  [PostItem](postitem.md)  |  [Tarea](task.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento PolicyTag** es el identificador de etiqueta de directiva. El identificador de etiqueta de directiva es un GUID. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

