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
description: El elemento AllowExternalOof contiene un valor que identifica a quién se envían los mensajes fuera de la oficina (OOF) externos.
ms.openlocfilehash: e4934bc4bc86e1f9f764279a13ecaeca073d9e5d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464815"
---
# <a name="allowexternaloof"></a>AllowExternalOof

El elemento **AllowExternalOof** contiene un valor que identifica a quién se envían los mensajes fuera de la oficina (OOF) externos. 
  
- [GetUserOofSettingsResponse](getuseroofsettingsresponse.md)
  
- [AllowExternalOof](allowexternaloof.md)
  
```xml
<AllowExternalOof>None or Known or All</AllowExternalOof>
```

 **ExternalAudience**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |Contiene los resultados de la respuesta y la configuración de OOF para un usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto para este elemento. En la siguiente tabla se enumeran los valores posibles para este elemento.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|**Ninguno** <br/> |Los remitentes de correo electrónico que se encuentran fuera de la organización del usuario del buzón que envían mensajes al usuario no recibirán una respuesta de mensaje OOF externa.  <br/> |
|**Válida** <br/> |Los remitentes de correo electrónico que se encuentran fuera de la organización del usuario del buzón de correo que envían mensajes al usuario solo recibirán una respuesta de mensaje de OOF externa si el remitente está en la lista de contactos del almacén de Exchange del usuario.  <br/> |
|**All** <br/> |Los remitentes de correo electrónico que se encuentran fuera de la organización del usuario del buzón de correo que envían mensajes al usuario recibirán una respuesta de mensaje OOF externa.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento comparte el mismo tipo que el elemento [ExternalAudience](externalaudience.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetUserOofSettings](getuseroofsettings-operation.md) 
- [Operación SetUserOofSettings](setuseroofsettings-operation.md)

