---
title: Extremo (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 630cdbb5-d1c7-422c-924a-abf5738e9e5e
description: El elemento de extremo especifica el extremo de servicio de token de seguridad.
ms.openlocfilehash: 85e1ad785b35649238ac3944f51472addf617c20
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764411"
---
# <a name="endpoint-soap"></a>Extremo (SOAP)

El elemento de **extremo** especifica el extremo de servicio de token de seguridad. 
  
```XML
<Endpoint/>
```

 **xs: anyURI**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[TokenIssuer (SOAP)](tokenissuer-soap.md) <br/> |Especifica el URI y el extremo para el servicio de token de seguridad.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el extremo para el servicio web del token de seguridad.
  
## <a name="remarks"></a>Comentarios

El extremo se usa para comunicarse con el servicio web de token de seguridad.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |True  <br/> |
   

