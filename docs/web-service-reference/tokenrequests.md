---
title: TokenRequests
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fbab89e9-b41a-44c4-8ad3-d46aa8e56652
description: El elemento TokenRequests contiene una matriz de las solicitudes de símbolo (token).
ms.openlocfilehash: 01d847d7d496a5bd1d5621a3787d0e3cc6ddd7ff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840724"
---
# <a name="tokenrequests"></a>TokenRequests

El elemento **TokenRequests** contiene una matriz de las solicitudes de símbolo (token). 
  
```XML
<TokenRequests>
   <TokenRequest/>
</TokenRequests>
```

 **NonEmptyArrayOfClientAccessTokenRequestsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[TokenRequest](tokenrequest.md)
  
### <a name="parent-elements"></a>Elementos principales

[GetClientAccessToken](getclientaccesstoken.md)
  
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
   

