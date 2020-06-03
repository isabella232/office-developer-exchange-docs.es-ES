---
title: ConfigurationName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConfigurationName
api_type:
- schema
ms.assetid: 3b524a2f-9c6b-4550-9f3d-f78d176b0f7b
description: El elemento ConfigurationName especifica las configuraciones de servicio solicitadas por nombre.
ms.openlocfilehash: 5e1216253a633af643dbd276827842dbe2db5d5f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463926"
---
# <a name="configurationname"></a>ConfigurationName

El elemento **ConfigurationName** especifica las configuraciones de servicio solicitadas por nombre. 
  
```xml
<ConfigurationName>MailTips or UnifiedMessagingConfiguration or ProtectionRules</ConfigurationName>
```

 **ServiceConfigurationType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[RequestedConfiguration](requestedconfiguration.md) <br/> |Contiene las configuraciones de servicio solicitadas.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumeran los valores posibles para el elemento **ConfigurationName** . 
  
**Valores del elemento ConfigurationName**

|**Valor**|**Descripción**|
|:-----|:-----|
|MailTips  <br/> |Identifica la configuración del servicio de sugerencias de correo.  <br/> |
|UnifiedMessagingConfiguration  <br/> |Identifica la configuración del servicio de mensajería unificada.  <br/> |
|ProtectionRules  <br/> |Identifica la configuración del servicio de reglas de protección.  <br/> |
   
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

