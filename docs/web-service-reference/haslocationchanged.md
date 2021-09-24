---
title: HasLocationChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5fd465b4-6070-4cd0-9ac3-ed9d2bfd5951
description: El elemento HasLocationChanged especifica si la propiedad location de una reunión ha cambiado.
ms.openlocfilehash: f59bca138d0baee87afd12470d9c50704edc75bd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519551"
---
# <a name="haslocationchanged"></a>HasLocationChanged

El **elemento HasLocationChanged** especifica si la propiedad location de una reunión ha cambiado. 
  
```XML
<HasLocationChanged> true | false </HasLocationChanged>
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

Un valor de texto **de true** para el **elemento HasLocationChanged** indica que la propiedad location de una reunión ha cambiado. Un valor **false** indica que la propiedad location de una reunión no ha cambiado. 
  
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

