---
title: OofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OofSettings
api_type:
- schema
ms.assetid: 8f37d174-db11-427c-bbed-fdde754a60c7
description: El elemento OofSettings contiene la configuración de fuera de la oficina (OOF).
ms.openlocfilehash: c1b214fd8bfab5b7a82d41a5187cf6e0fc4ba79c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467196"
---
# <a name="oofsettings"></a>OofSettings

El elemento **OofSettings** contiene la configuración de fuera de la oficina (OOF). 
  
[GetUserOofSettingsResponse](getuseroofsettingsresponse.md)
  
[OofSettings](oofsettings.md)
  
```xml
<OofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</OofSettings>
```

 **UserOofSettings**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[OofState](oofstate.md) <br/> |Contiene el estado de OOF del usuario.  <br/> |
|[ExternalAudience](externalaudience.md) <br/> |Contiene un valor que determina a quién se envían los mensajes de OOF externos.  <br/> |
|[Duración (UserOofSettings)](duration-useroofsettings.md) <br/> |Contiene la duración para la que está habilitado el estado OOF si el elemento [OofState](oofstate.md) está establecido en **programado**. Si el elemento [OofState](oofstate.md) está establecido en **habilitado** o **deshabilitado**, se omite el valor de este elemento.  <br/> |
|[InternalReply](internalreply.md) <br/> |Contiene la respuesta OOF enviada a otros usuarios en el dominio del usuario o en un dominio de confianza.  <br/> |
|[ExternalReply](externalreply.md) <br/> |Contiene la respuesta OOF enviada a direcciones fuera del dominio del destinatario o de dominios de confianza.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |Contiene los resultados de la respuesta y la configuración de OOF para un usuario.  <br/> La siguiente es la expresión XPath a este elemento:  <br/>  `/GetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserOofSettings](getuseroofsettings-operation.md)
  
[Operación SetUserOofSettings](setuseroofsettings-operation.md)

