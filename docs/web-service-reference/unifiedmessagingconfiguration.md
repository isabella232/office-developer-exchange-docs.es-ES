---
title: UnifiedMessagingConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnifiedMessagingConfiguration
api_type:
- schema
ms.assetid: cbdb4268-077e-44ed-8ec2-9d759c84cc6d
description: El elemento UnifiedMessagingConfiguration contiene información de configuración del servicio para el servicio de mensajería unificada.
ms.openlocfilehash: 3f9f4ed65721929c552615c07e2239f48ef837f3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528695"
---
# <a name="unifiedmessagingconfiguration"></a>UnifiedMessagingConfiguration

El elemento **UnifiedMessagingConfiguration** contiene información de configuración del servicio para el servicio de mensajería unificada. 
  
```XML
<UnifiedMessagingConfiguration>
   <UmEnabled/>
   <PlayOnPhoneDialString/>
   <PlayOnPhoneEnabled/>
</UnifiedMessagingConfiguration>
```

 **UnifiedMessageServiceConfiguration**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[UmEnabled](umenabled.md) <br/> |Indica si la mensajería unificada está habilitada para una cuenta. Se requiere este elemento.  <br/> |
|[PlayOnPhoneDialString (servicios web Exchange)](playonphonedialstring-exchange-web-services.md) <br/> |Identifica la cadena de marcado de reproducción en teléfono. Se requiere este elemento.  <br/> |
|[PlayOnPhoneEnabled](playonphoneenabled.md) <br/> |Indica si está habilitada la característica de reproducción en teléfono. Se requiere este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ServiceConfigurationResponseMessageType](serviceconfigurationresponsemessagetype.md) <br/> |Contiene las opciones de configuración del servicio.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

