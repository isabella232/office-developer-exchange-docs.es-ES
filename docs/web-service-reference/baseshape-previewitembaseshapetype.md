---
title: BaseShape (PreviewItemBaseShapeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b9e2fdd-5678-4178-9297-7f12a3ca9d64
description: El elemento BaseShape especifica la vista previa predeterminada con todas las propiedades devueltas o una vista previa compacta con menos propiedades devueltas.
ms.openlocfilehash: 29f008840d649f97dfb299fee8e7bf5aaa573404
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527421"
---
# <a name="baseshape-previewitembaseshapetype"></a>BaseShape (PreviewItemBaseShapeType)

El elemento **BaseShape** especifica la vista previa predeterminada con todas las propiedades devueltas o una vista previa compacta con menos propiedades devueltas. 
  
```XML
<BaseShape> Default | Compact</BaseShape>
```

 **PreviewItemBaseShapeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PreviewItemResponseShape](previewitemresponseshape.md) <br/> |Contiene la forma de la respuesta.  <br/> |
   
## <a name="text-value"></a>Valor de texto

**Valores de texto del elemento BaseShape**

|**Valor**|**Descripción**|
|:-----|:-----|
|Predeterminado  <br/> |Indica que se muestran todas las propiedades.  <br/> |
|Compacto  <br/> |Indica que solo se muestran las propiedades seleccionadas.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

