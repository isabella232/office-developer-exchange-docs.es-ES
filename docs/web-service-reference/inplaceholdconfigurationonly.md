---
title: InPlaceHoldConfigurationOnly
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 921ecc73-b7e2-40a7-8458-68f18dd5a13b
description: El elemento InPlaceHoldConfigurationOnly especifica si se debe incluir la configuración de la conservación local.
ms.openlocfilehash: ca364ee7d8a9e2e4a608f8f6c4ca5851fa7d4b64
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466104"
---
# <a name="inplaceholdconfigurationonly"></a>InPlaceHoldConfigurationOnly

El elemento **InPlaceHoldConfigurationOnly** especifica si se debe incluir la configuración de la conservación local. 
  
```XML
<InPlaceHoldConfigurationOnly>true | false</InPlaceHoldConfigurationOnly>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** para el elemento **InPlaceHoldConfigurationOnly** indica que se incluye la configuración de conservación local. Un valor de **false** indica que no se incluye la configuración de la retención local. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> ||
   

