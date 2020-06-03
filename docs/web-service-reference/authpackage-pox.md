---
title: AuthPackage (POX)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 709dbe53-6141-41f8-a2b9-a399bae47991
description: El elemento AuthPackage especifica el esquema de autenticación que se usa al autenticar en el servidor de Exchange que tiene instalado el rol de servidor buzón de correo.
ms.openlocfilehash: 5317cf49d354a558417829e1d1b5b67cd6874309
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459107"
---
# <a name="authpackage-pox"></a>AuthPackage (POX)

El elemento **AuthPackage** especifica el esquema de autenticación que se usa al autenticar en el servidor de Exchange que tiene instalado el rol de servidor buzón de correo. 
  
- [Detección automática (POX)](autodiscover-pox.md)
  
- [Respuesta (POX)](response-pox.md)
  
- [Cuenta (POX)](account-pox.md)
  
- [Protocolo (POX)](protocol-pox.md)
  
- [AuthPackage (POX)](authpackage-pox.md)
  
```xml
<AuthPackage>basic or kerb or kerbntlm or ntlm or certificate or negotiate or nego2</AuthPackage>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al servidor de acceso de cliente.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto especifica el esquema de autenticación que se usa al autenticar en el servidor de buzones de correo. Los valores posibles son los siguientes:
  
- elementos
- kerbtray
- kerbntlm
- NTLM
- certificado
- negociar
- nego2
    
## <a name="remarks"></a>Comentarios

El elemento **AuthPackage** solo se usa cuando el elemento [Type (POX)](type-pox.md) tiene un valor de texto de EXCH o expr. 
  
### <a name="version-differences"></a>Diferencias de versión

Office 365, Exchange Online y versiones locales de Exchange que comienzan con la compilación 15.00.0995.014 devuelven un valor de "Negotiate" solo si el servidor está configurado para usar la autenticación Negotiate y el cliente incluye un encabezado [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) que contiene "Negotiate". 
  
## <a name="see-also"></a>Vea también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

