---
title: TokenType (ClientAccessTokenType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 96103f15-a3e0-497c-af21-90adbf9a4b14
description: El elemento TokenType identifica el tipo de token de acceso de cliente que se devolverá en la respuesta GetClientAccessToken.
ms.openlocfilehash: 967d64796799147876ef6443b40b16154b55c01a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523359"
---
# <a name="tokentype-clientaccesstokentype"></a>TokenType (ClientAccessTokenType)

El **elemento TokenType** identifica el tipo de token de acceso de cliente que se devolverá en la **respuesta GetClientAccessToken.** 
  
```XML
<TokenType>CallerIdentity | ExtensionCallback | ScopedToken</TokenType>
```

 **ClientAccessTokenTypeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[TokenRequest](tokenrequest.md)  |  [Token (ClientAccessTokenType)](token-clientaccesstokentype.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto de **CallerIdentity** significa que se devuelve un token de acceso de cliente de identidad de autor de la llamada. Un valor de texto de **ExtensionCallback** indica que se devuelve un token de acceso de cliente de devolución de llamada de extensión. Un valor de texto **de ScopedToken** indica que el token de acceso de cliente es un token con ámbito. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

