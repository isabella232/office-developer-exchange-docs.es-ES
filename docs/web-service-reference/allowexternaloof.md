---
title: AllowExternalOof
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AllowExternalOof
api_type:
- schema
ms.assetid: e5387172-5b92-4bb1-8394-180e9c7ff771
description: El elemento AllowExternalOof contiene un valor que identifica a la que se envían los mensajes externos de fuera de oficina (OOF).
ms.openlocfilehash: 1c87a51676bf6e44b2e650a4e973d0ab89a52e31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763432"
---
# <a name="allowexternaloof"></a>AllowExternalOof

El elemento **AllowExternalOof** contiene un valor que identifica a la que se envían los mensajes externos de fuera de oficina (OOF). 
  
- [GetUserOofSettingsResponse](getuseroofsettingsresponse.md)
  
- [AllowExternalOof](allowexternaloof.md)
  
```xml
<AllowExternalOof>None or Known or All</AllowExternalOof>
```

 **ExternalAudience**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |Contiene los resultados de la respuesta y la configuración de fuera de la oficina de un usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto es necesario para este elemento. En la siguiente tabla se enumera los valores posibles para este elemento.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|**None** <br/> |Los remitentes de correo electrónico fuera de la organización del usuario de buzón de correo que envían mensajes al usuario no recibirá una respuesta de mensaje de fuera de la oficina externa.  <br/> |
|**Conocidos** <br/> |Los remitentes de correo electrónico fuera de la organización del usuario de buzón de correo que envían mensajes al usuario sólo recibirá una respuesta de mensaje de fuera de la oficina externa si el remitente está en Exchange del usuario almacenan la lista de contactos.  <br/> |
|**All** <br/> |Los remitentes de correo electrónico fuera de la organización del usuario de buzón de correo que envían mensajes al usuario recibirá una respuesta de mensaje de fuera de la oficina externa.  <br/> |
   
## <a name="remarks"></a>Notas

Este elemento comparte el mismo tipo que el elemento [ExternalAudience](externalaudience.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserOofSettings](getuseroofsettings-operation.md) 
- [Operación SetUserOofSettings](setuseroofsettings-operation.md)

