---
title: Tiempo de espera (duración)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bb15f9a7-8ea5-4765-9877-762c3f98bf50
description: El elemento timeout especifica el período de tiempo que debe transcurrir antes de que el servidor supere el tiempo de espera de una suscripción de extracción.
ms.openlocfilehash: b5b0e77d794080cd8e0da1e14acf4cb059b80b08
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460284"
---
# <a name="timeout-duration"></a>Tiempo de espera (duración)

El elemento **timeout** especifica el período de tiempo que debe transcurrir antes de que el servidor supere el tiempo de espera de una suscripción de extracción. 
  
```XML
<Timeout></Timeout>
```

 **SubscriptionTimeoutType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[PullSubscriptionRequest](pullsubscriptionrequest.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **timeout** es el período de tiempo, en minutos, antes de que el servidor agote el tiempo de espera de una suscripción de extracción. El valor mínimo es 1; el valor máximo es 1440. 
  
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
   

