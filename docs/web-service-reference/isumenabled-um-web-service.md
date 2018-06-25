---
title: IsUMEnabled (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- IsUMEnabled
api_type:
- schema
ms.assetid: 33810bbd-837f-4a71-9ed9-cb4b8c52186d
description: El elemento IsUMEnabled indica si un buzón de correo está habilitado para mensajería unificada.
ms.openlocfilehash: 5f4d59c5497158e5afbc8bb5db4900bd129df50b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836113"
---
# <a name="isumenabled-um-web-service"></a>IsUMEnabled (servicio web de mensajería unificada)

El elemento **IsUMEnabled** indica si un buzón de correo está habilitado para mensajería unificada. 
  
```xml
<IsUMEnabled/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

Si este elemento se incluye, se requiere un valor de texto que representa un valor de tipo Boolean. Un valor de **true** indica que el buzón está habilitado para mensajería unificada. Un valor de **false** significa que el buzón de correo no está habilitado para mensajería unificada. 
  
## <a name="remarks"></a>Comentarios

Para determinar si un buzón de correo está habilitado para mensajería unificada, use la [operación de IsUMEnabled (servicio web de mensajería unificada)](isumenabled-operation-um-web-service.md).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación IsUMEnabled (servicio web de mensajería unificada)](isumenabled-operation-um-web-service.md)


[Elementos XML de servicio de web de Unified Messaging para Exchange](unified-messaging-web-service-xml-elements-for-exchange.md)

