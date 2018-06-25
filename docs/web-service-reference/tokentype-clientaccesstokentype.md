---
title: TokenType en (ClientAccessTokenType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96103f15-a3e0-497c-af21-90adbf9a4b14
description: El elemento TokenType en identifica el tipo de token de acceso de cliente que se devuelve en la respuesta de GetClientAccessToken.
ms.openlocfilehash: c9adb60acf76fefebd58e2fd3bc899332a63dbee
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840701"
---
# <a name="tokentype-clientaccesstokentype"></a>TokenType en (ClientAccessTokenType)

El elemento **TokenType en** identifica el tipo de token de acceso de cliente que se devuelve en la respuesta de **GetClientAccessToken** . 
  
```XML
<TokenType>CallerIdentity | ExtensionCallback | ScopedToken</TokenType>
```

 **ClientAccessTokenTypeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[TokenRequest](tokenrequest.md) | [(ClientAccessTokenType) de Token](token-clientaccesstokentype.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto de **CallerIdentity** significa que se devuelve un token de acceso de cliente de identidad de autor de la llamada. Un valor de texto de **ExtensionCallback** indica que se devuelve un token de acceso de cliente de devolución de llamada de extensión. Un valor de texto de **ScopedToken** indica que el token de acceso de cliente es un token de ámbito. 
  
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
   

