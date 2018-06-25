---
title: IncludePersonalArchive
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b373bb1a-6b1d-4959-98a1-4c4ea62973bc
description: El elemento IncludePersonalArchive especifica si se debe incluir el archivo personal en la búsqueda.
ms.openlocfilehash: ba2dcaae3befd3595815c7281858e4fa8a738e0a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835905"
---
# <a name="includepersonalarchive"></a>IncludePersonalArchive

El elemento **IncludePersonalArchive** especifica si se debe incluir el archivo personal en la búsqueda. 
  
```XML
<IncludePersonalArchive>true | false</IncludePersonalArchive>
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
|[FindMailboxStatisticsByKeywords](findmailboxstatisticsbykeywords.md) <br/> |Especifica una solicitud para buscar las estadísticas de buzón de correo por palabra clave.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** para el elemento **IncludePersonalArchive** indica que el archivo personal está incluido en la búsqueda. Un valor de **false** indica que el archivo personal no se incluye en la búsqueda. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

