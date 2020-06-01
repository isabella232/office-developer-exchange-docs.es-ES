---
title: IsUMEnabled (servicio Web de mensajería unificada)
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
description: El elemento IsUMEnabled indica si un buzón está habilitado para mensajería unificada.
ms.openlocfilehash: ea5bde677c62664acad8afd5c8142e96d82b7a74
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458232"
---
# <a name="isumenabled-um-web-service"></a>IsUMEnabled (servicio Web de mensajería unificada)

El elemento **IsUMEnabled** indica si un buzón está habilitado para mensajería unificada. 
  
```xml
<IsUMEnabled/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

Ninguna.
  
## <a name="text-value"></a>Valor de texto

Si se incluye este elemento, es necesario un valor de texto que represente un valor booleano. Un valor de **true** indica que el buzón de correo está habilitado para mensajería unificada. Un valor de **false** significa que el buzón de correo no está habilitado para mensajería unificada. 
  
## <a name="remarks"></a>Comentarios

Para determinar si un buzón está habilitado para mensajería unificada, use la [operación IsUMEnabled (servicio Web de mensajería unificada)](isumenabled-operation-um-web-service.md).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación IsUMEnabled (servicio Web de mensajería unificada)](isumenabled-operation-um-web-service.md)


[Elementos XML de servicio Web de mensajería unificada para Exchange](unified-messaging-web-service-xml-elements-for-exchange.md)

