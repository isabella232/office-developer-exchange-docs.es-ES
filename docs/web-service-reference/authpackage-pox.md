---
title: AuthPackage (POX)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 709dbe53-6141-41f8-a2b9-a399bae47991
description: El elemento AuthPackage especifica el esquema de autenticación que se usa al autenticarse en el servidor exchange que tiene instalado el rol de servidor Buzón de correo.
ms.openlocfilehash: aff4e84cd44d76c2c5a913b6627e1b0c87bab4dc
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513027"
---
# <a name="authpackage-pox"></a>AuthPackage (POX)

El **elemento AuthPackage** especifica el esquema de autenticación que se usa al autenticarse en el servidor exchange que tiene instalado el rol de servidor Buzón de correo. 
  
- [AutoDiscover (POX)](autodiscover-pox.md)
  
- [Response (POX)](response-pox.md)
  
- [Account (POX)](account-pox.md)
  
- [Protocol (POX)](protocol-pox.md)
  
- [AuthPackage (POX)](authpackage-pox.md)
  
```xml
<AuthPackage>basic or kerb or kerbntlm or ntlm or certificate or negotiate or nego2</AuthPackage>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Protocol (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al servidor de acceso de cliente.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto especifica el esquema de autenticación que se usa al autenticar en el servidor de buzones de correo. Los valores posibles son los siguientes:
  
- basic
- kerb
- kerbntlm
- ntlm
- certificado
- negociar
- nego2
    
## <a name="remarks"></a>Comentarios

El **elemento AuthPackage** solo se usa cuando el elemento [Type (POX)](type-pox.md) tiene un valor de texto de EXCH o EXPR. 
  
### <a name="version-differences"></a>Diferencias de versión

Office 365, Exchange Online y las versiones locales de Exchange a partir de la compilación 15.00.0995.014 devuelven un valor de "negociar" solo si el servidor está configurado para usar la autenticación Negotiate y el cliente incluye un encabezado [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) que contiene "Negotiate". 
  
## <a name="see-also"></a>Ver también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

