---
title: PolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa4b1447-dc7b-47ad-a677-78fcee443dc6
description: El elemento PolicyTag especifica el identificador de retención en una carpeta o elemento.
ms.openlocfilehash: d6cd5aab1145f6006912541c8f8c1d0a91d1e17e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836835"
---
# <a name="policytag"></a>PolicyTag

El elemento **PolicyTag** especifica el identificador de retención en una carpeta o elemento. 
  
```xml
<PolicyTag IsExplicit="true | false"></PolicyTag>
```

 **RetentionTagType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|IsExplicit  <br/> |Indica si una etiqueta de directiva se estableció explícitamente en un elemento o carpeta.  <br/> Un valor de texto de **true** para el atributo **IsExplicit** indica que la etiqueta de directiva se establezca explícitamente en el elemento o la carpeta. Un valor de texto de **false** indica que la etiqueta de directiva implícitamente se estableció en el elemento o la carpeta en función de la etiqueta de directiva de carpeta primaria.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[SearchPreviewItem](searchpreviewitem.md) | [elemento](item.md) | [contacto](contact.md) | [mensaje](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [tarea](task.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **PolicyTag** es el identificador de etiqueta de directiva. El identificador de etiqueta de directiva es un GUID. 
  
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

