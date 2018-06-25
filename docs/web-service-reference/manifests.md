---
title: Manifiestos
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 650d9fc0-1504-4db4-95d6-d3ba86df66ca
description: El elemento de manifiestos contiene una colección de manifiestos de aplicaciones con codificación base64 que estén instalados para la cuenta de correo electrónico.
ms.openlocfilehash: 3877841c097e6b968d0af51ae5261e5b4336c7ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836362"
---
# <a name="manifests"></a>Manifiestos

El elemento **manifiestos** contiene una colección de manifiestos de aplicaciones con codificación base64 que estén instalados para la cuenta de correo electrónico. 
  
```XML
<Manifests>
   <Manifest/>
</Manifests>
```

 **ArrayOfAppManifestsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[Manifest](manifest.md)
  
### <a name="parent-elements"></a>Elementos principales

[GetAppManifestsResponse](getappmanifestsresponse.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

