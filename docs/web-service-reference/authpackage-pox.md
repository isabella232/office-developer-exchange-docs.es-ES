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
description: El elemento AuthPackage especifica el esquema de autenticación que se usa cuando se realiza en el servidor de Exchange que tenga instalado el rol de servidor de buzón de correo.
ms.openlocfilehash: 120ec00ac82166ae2002a8fbac0edf9a1e23afc7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763584"
---
# <a name="authpackage-pox"></a>AuthPackage (POX)

El elemento **AuthPackage** especifica el esquema de autenticación que se usa cuando se realiza en el servidor de Exchange que tenga instalado el rol de servidor de buzón de correo. 
  
- [Detección automática (POX)](autodiscover-pox.md)
  
- [Respuesta (POX)](response-pox.md)
  
- [Cuenta (POX)](account-pox.md)
  
- [Protocolo (POX)](protocol-pox.md)
  
- [AuthPackage (POX)](authpackage-pox.md)
  
```xml
<AuthPackage>basic or kerb or kerbntlm or ntlm or certificate or negotiate or nego2</AuthPackage>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar a un cliente con el servidor de acceso de cliente.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto especifica el esquema de autenticación que se usa cuando se realiza en el servidor de buzón de correo. Los valores posibles son:
  
- básica
- Kerbtray
- kerbntlm
- NTLM
- certificado
- negociar
- nego2
    
## <a name="remarks"></a>Notas

El elemento **AuthPackage** solo se usa cuando el elemento de [Tipo (POX)](type-pox.md) tiene un valor de texto de EXCH o EXPR. 
  
### <a name="version-differences"></a>Diferencias de versión

Office 365, Exchange Online y versiones locales de inicio de Exchange con creación 15.00.0995.014 devuelto un valor de "negociar" sólo si el servidor está configurado para usar la autenticación Negotiate y el cliente incluye un encabezado [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) que contiene "Negotiate". 
  
## <a name="see-also"></a>Ver también

- [Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

