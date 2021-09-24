---
title: Endpoint (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 630cdbb5-d1c7-422c-924a-abf5738e9e5e
description: El elemento Endpoint especifica el extremo de servicio de token de seguridad.
ms.openlocfilehash: 49a85dc80a92828262ab75652299d4a0c4d75de8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530976"
---
# <a name="endpoint-soap"></a>Endpoint (SOAP)

El **elemento Endpoint** especifica el extremo de servicio de token de seguridad. 
  
```XML
<Endpoint/>
```

 **xs:anyURI**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[TokenIssuer (SOAP)](tokenissuer-soap.md) <br/> |Especifica el URI y el punto de conexión para el servicio de token de seguridad.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el punto de conexión del servicio web de token de seguridad.
  
## <a name="remarks"></a>Comentarios

El extremo se usa para comunicarse con el servicio web de token de seguridad.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   

