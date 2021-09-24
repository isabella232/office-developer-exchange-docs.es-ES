---
title: IsUMEnabled (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- IsUMEnabled
api_type:
- schema
ms.assetid: 33810bbd-837f-4a71-9ed9-cb4b8c52186d
description: El elemento IsUMEnabled indica si un buzón está habilitado para la mensajería unificada.
ms.openlocfilehash: 43632c28c5fb0c526dcf2ad936784953b00cc14a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524122"
---
# <a name="isumenabled-um-web-service"></a>IsUMEnabled (servicio web de mensajería unificada)

El **elemento IsUMEnabled** indica si un buzón está habilitado para la mensajería unificada. 
  
```xml
<IsUMEnabled/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

Si se incluye este elemento, se requiere un valor de texto que represente un valor booleano. Un valor **true** indica que el buzón está habilitado para la mensajería unificada. Un valor de **false** significa que el buzón no está habilitado para la mensajería unificada. 
  
## <a name="remarks"></a>Comentarios

Para determinar si un buzón está habilitado para la mensajería unificada, use la operación [IsUMEnabled (servicio web de](isumenabled-operation-um-web-service.md)mensajería unificada).
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación IsUMEnabled (servicio web de mensajería unificada)](isumenabled-operation-um-web-service.md)


[Elementos XML del servicio web de mensajería unificada para Exchange](unified-messaging-web-service-xml-elements-for-exchange.md)

