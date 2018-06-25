---
title: TokenType en
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83c650eb-7ab8-480c-a7c9-df60072ee042
description: El elemento TokenType en especifica el tipo de símbolo (token).
ms.openlocfilehash: 5c8e880f035ed74776a7c77e4b4e60ca46d66d4e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840695"
---
# <a name="tokentype"></a>TokenType en

El elemento **TokenType en** especifica el tipo de símbolo (token). 
  
```XML
<TokenType> CallerIdentity | ExtensionCallback | ScopedToken </TokenType>
```

 **ClientAccessTokenTypeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[TokenRequest](tokenrequest.md) | [símbolo (token)](token.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **TokenType en** es el tipo de símbolo (token). El valor de texto de **CallerIdentity** indica que el token es un token de identidad del autor de la llamada. El valor de texto de **ExtensionCallback** indica que el token es para una devolución de llamada de extensión. El valor de texto de **ScopedToken** indica que el token de acceso de cliente es un token de ámbito. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |falso  <br/> |
   

