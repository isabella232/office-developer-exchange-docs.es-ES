---
title: OofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- OofSettings
api_type:
- schema
ms.assetid: 8f37d174-db11-427c-bbed-fdde754a60c7
description: El elemento OofSettings contiene la configuración fuera de Office (OOF).
ms.openlocfilehash: 0a612cacb69464dfda3c1f235c32f569d3e45775
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543173"
---
# <a name="oofsettings"></a>OofSettings

El **elemento OofSettings** contiene la configuración fuera de Office (OOF). 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[OofState](oofstate.md) <br/> |Contiene el estado OOF del usuario.  <br/> |
|[ExternalAudience](externalaudience.md) <br/> |Contiene un valor que determina a quién se envían los mensajes OOF externos.  <br/> |
|[Duration (UserOofSettings)](duration-useroofsettings.md) <br/> |Contiene la duración durante la cual el estado de OOF está habilitado si el elemento [OofState](oofstate.md) está establecido en **Scheduled**. Si el [elemento OofState](oofstate.md) está establecido en **Enabled** o **Disabled**, se omite el valor de este elemento.  <br/> |
|[InternalReply](internalreply.md) <br/> |Contiene la respuesta de OOF enviada a otros usuarios en el dominio o dominio de confianza del usuario.  <br/> |
|[ExternalReply](externalreply.md) <br/> |Contiene la respuesta OOF enviada a direcciones fuera del dominio del destinatario o dominios de confianza.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |Contiene los resultados de la respuesta y la configuración de OOF de un usuario.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/GetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



[Operación GetUserOofSettings](getuseroofsettings-operation.md)
  
[Operación SetUserOofSettings](setuseroofsettings-operation.md)

