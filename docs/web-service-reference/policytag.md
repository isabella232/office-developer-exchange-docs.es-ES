---
title: PolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa4b1447-dc7b-47ad-a677-78fcee443dc6
description: El elemento PolicyTag especifica el identificador de retención de un elemento o una carpeta.
ms.openlocfilehash: ddc4d890d1e514586ba5ea7f6a8b541b2e4786c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460900"
---
# <a name="policytag"></a>PolicyTag

El elemento **PolicyTag** especifica el identificador de retención de un elemento o una carpeta. 
  
```xml
<PolicyTag IsExplicit="true | false"></PolicyTag>
```

 **RetentionTagType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|IsExplicit  <br/> |Indica si una etiqueta de Directiva se estableció explícitamente en un elemento o una carpeta.  <br/> Un valor de texto de **true** para el atributo **IsExplicit** indica que la etiqueta de Directiva se estableció explícitamente en el elemento o carpeta. Un valor de texto **falso** indica que la etiqueta de Directiva se ha configurado implícitamente en el elemento o la carpeta basándose en la etiqueta de directiva de carpeta principal.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[SearchPreviewItem](searchpreviewitem.md)  |  [Elemento](item.md)  |  [Contacto](contact.md)  |  [Mensaje de error](message-ex15websvcsotherref.md)  |  [DistributionList](distributionlist.md)  |  [CalendarItem](calendaritem.md)  |  [PostItem](postitem.md)  |  [Tarea](task.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **PolicyTag** es el identificador de la etiqueta de directiva. El identificador de etiqueta de directiva es un GUID. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   

