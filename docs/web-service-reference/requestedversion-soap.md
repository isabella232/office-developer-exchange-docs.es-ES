---
title: RequestedVersion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 962036c9-9b13-4669-bed2-2502c0f5aabe
description: El elemento RequestedVersion especifica la versión de servicio mínimo que el cliente desea recibir la solicitud que va a procesar en.
ms.openlocfilehash: 0d8682c33790d2d26001512ad9e2191ae52074d0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837134"
---
# <a name="requestedversion-soap"></a>RequestedVersion (SOAP)

El elemento **RequestedVersion** especifica la versión de servicio mínimo que el cliente desea recibir la solicitud que va a procesar en. 
  
```XML
<RequestedVersion/>
```

 **ExchangeVersion**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Solicitud (SOAP)](request-soap.md) <br/> |Contiene las opciones de configuración solicitado y los usuarios de destino.  <br/> |
|[Solicitud (SOAP) (GetDomainSettings)](request-getdomainsettingssoap.md) <br/> |Representa una solicitud para obtener la configuración de dominio.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto para el elemento **RequestedVersion** puede ser Exchange2010, Exchange2010_SP1, Exchange2010_SP2 o Exchange2013.
  
## <a name="remarks"></a>Comentarios

Si este elemento no está presente, se utiliza la versión más reciente del servicio.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
  
[Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)

