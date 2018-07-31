---
title: Request (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: da54eb32-7ce5-4384-9893-255a2243a959
description: El elemento de solicitud contiene la solicitud para el servicio Detección automática.
ms.openlocfilehash: 3f5d5258a92840fe79c4936370323b78aa4715b3
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354431"
---
# <a name="request-pox"></a>Request (POX)

El elemento de **solicitud** contiene la solicitud para el servicio Detección automática. 
  
- [AutoDiscover (POX)](autodiscover-pox.md) 
- [Request (POX)](request-pox.md)
  
```xml
<Request>
   <AcceptableResponseSchema/>
   <EMailAddress/>
</Request>
```

```xml
<Request>
   <AcceptableResponseSchema/> 
   <LegacyDN/>
</Request>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[AcceptableResponseSchema (POX)](acceptableresponseschema-pox.md) <br/> |Identifica el esquema de una respuesta de detección automática.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Identifica la dirección de correo electrónico del usuario.  <br/> |
|[LegacyDN (POX)](legacydn-pox.md) <br/> |Identifica el buzón de un usuario por su nombre distintivo (DN) heredado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[AutoDiscover (POX)](autodiscover-pox.md) <br/> |El elemento raíz en una solicitud de detección automática.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

