---
title: TokenRequests
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: fbab89e9-b41a-44c4-8ad3-d46aa8e56652
description: El elemento TokenRequests contiene una matriz de solicitudes de token.
ms.openlocfilehash: 262f34bdf0c5c1eaf946d1de7ba656470be99e50
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527247"
---
# <a name="tokenrequests"></a>TokenRequests

El **elemento TokenRequests** contiene una matriz de solicitudes de token. 
  
```XML
<TokenRequests>
   <TokenRequest/>
</TokenRequests>
```

 **NonEmptyArrayOfClientAccessTokenRequestsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
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
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

