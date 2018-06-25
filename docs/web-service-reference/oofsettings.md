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
description: El elemento OofSettings contiene la configuración de fuera de oficina (OOF).
ms.openlocfilehash: d71f068ff24af22da98b6b4de090ab26d3f74f26
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836649"
---
# <a name="oofsettings"></a>OofSettings

El elemento **OofSettings** contiene la configuración de fuera de oficina (OOF). 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[OofState](oofstate.md) <br/> |Contiene el estado de fuera de la oficina del usuario.  <br/> |
|[ExternalAudience](externalaudience.md) <br/> |Contiene un valor que determina a quienes se envían los mensajes externos de fuera de la oficina.  <br/> |
|[Duración (UserOofSettings)](duration-useroofsettings.md) <br/> |Contiene la duración para la que está habilitado el estado de fuera de la oficina si el elemento [OofState](oofstate.md) está establecido en **programado**. Si el elemento de [OofState](oofstate.md) se establece en **habilitada** o **deshabilitada**, se ignora el valor de este elemento.  <br/> |
|[InternalReply](internalreply.md) <br/> |Contiene la respuesta OOF enviada a otros usuarios de dominio o los dominios de confianza del usuario.  <br/> |
|[ExternalReply](externalreply.md) <br/> |Contiene la respuesta OOF enviada a direcciones fuera del destinatario dominio o dominios de confianza.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |Contiene los resultados de la respuesta y la configuración de fuera de la oficina de un usuario.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/GetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserOofSettings](getuseroofsettings-operation.md)
  
[Operación SetUserOofSettings](setuseroofsettings-operation.md)

