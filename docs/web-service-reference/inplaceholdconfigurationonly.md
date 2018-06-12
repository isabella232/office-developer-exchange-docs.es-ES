---
title: InPlaceHoldConfigurationOnly
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 921ecc73-b7e2-40a7-8458-68f18dd5a13b
description: El elemento InPlaceHoldConfigurationOnly especifica si para incluir la conservación local configuración.
ms.openlocfilehash: 3ad020a10e43d8f54e3d603906c856e01b1956eb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835934"
---
# <a name="inplaceholdconfigurationonly"></a>InPlaceHoldConfigurationOnly

El elemento **InPlaceHoldConfigurationOnly** especifica si para incluir la conservación local configuración. 
  
```XML
<InPlaceHoldConfigurationOnly>true | false</InPlaceHoldConfigurationOnly>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[GetDiscoverySearchConfiguration](getdiscoverysearchconfiguration.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** para el elemento **InPlaceHoldConfigurationOnly** indica que se incluye la configuración de suspensión en contexto. Un valor de **false** indica que no se incluye la configuración de suspensión en contexto. 
  
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

