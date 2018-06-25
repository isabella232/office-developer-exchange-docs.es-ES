---
title: GetUserOofSettingsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserOofSettingsResponse
api_type:
- schema
ms.assetid: 011cb38b-da3c-4b1b-8836-a6b212b511f6
description: El elemento GetUserOofSettingsResponse contiene el mensaje de respuesta y la configuración de fuera de oficina (OOF) para un usuario.
ms.openlocfilehash: dc63b6d54471973ce5961a5a5ad6a23f6521fc0e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835693"
---
# <a name="getuseroofsettingsresponse"></a>GetUserOofSettingsResponse

El elemento **GetUserOofSettingsResponse** contiene el mensaje de respuesta y la configuración de fuera de oficina (OOF) para un usuario. 
  
```xml
<GetUserOofSettingsResponse>
   <ResponseMessage>...</ResponseMessage>
   <OofSettings>...</OofSettings>
   <AllowExternalOof>...</AllowExternalOof>
</GetUserOofSettingsResponse>
```

 **GetUserOofSettingsResponse**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ResponseMessage](responsemessage.md) <br/> |Proporciona información descriptiva sobre el estado de respuesta.  <br/> |
|[OofSettings](oofsettings.md) <br/> |Contiene la configuración de fuera de la oficina.  <br/> |
|[AllowExternalOof](allowexternaloof.md) <br/> |Contiene un valor que identifica a la que se envían los mensajes externos de fuera de la oficina.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
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

