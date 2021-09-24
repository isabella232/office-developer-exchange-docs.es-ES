---
title: HasStartTimeChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 04a6968d-7fb5-47ee-b66e-dc99c35dbb63
description: El elemento HasStartTimeChanged especifica si la hora de inicio de una reunión ha cambiado.
ms.openlocfilehash: 7f04c4d34a081b91adbb0796019e93bc50bfb8ab
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539650"
---
# <a name="hasstarttimechanged"></a>HasStartTimeChanged

El **elemento HasStartTimeChanged** especifica si la hora de inicio de una reunión ha cambiado. 
  
```XML
<HasStartTimeChanged> true | false </HasStartTimeChanged>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ChangeHighlights](changehighlights.md) <br/> |Especifica lo que ha cambiado entre dos versiones de un mensaje de solicitud de reunión.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el **elemento HasStartTimeChanged** indica que la hora de inicio de una reunión ha cambiado. Un valor de **false** indica que la hora de inicio no ha cambiado. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

