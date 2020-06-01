---
title: Solicitud (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: da54eb32-7ce5-4384-9893-255a2243a959
description: El elemento request contiene la solicitud al servicio Detección automática.
ms.openlocfilehash: bc215d614441ed8f12c0f1490f4abdbb7b574ad0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459549"
---
# <a name="request-pox"></a>Solicitud (POX)

El elemento **request** contiene la solicitud al servicio Detección automática. 
  
- [Detección automática (POX)](autodiscover-pox.md) 
- [Solicitud (POX)](request-pox.md)
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AcceptableResponseSchema (POX)](acceptableresponseschema-pox.md) <br/> |Identifica el esquema para una respuesta de detección automática.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Identifica la dirección de correo electrónico del usuario.  <br/> |
|[LegacyDN (POX)](legacydn-pox.md) <br/> |Identifica el buzón de un usuario mediante el nombre distintivo heredado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Detección automática (POX)](autodiscover-pox.md) <br/> |El elemento raíz en una solicitud de detección automática.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

