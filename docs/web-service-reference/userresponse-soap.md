---
title: UserResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd
description: El elemento UserResponse representa una respuesta a una solicitud GetUserSettings para un usuario individual.
ms.openlocfilehash: 8def0183a5c2e212e80699a3c2f58c64f67ce690
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538544"
---
# <a name="userresponse-soap"></a>UserResponse (SOAP)

El **elemento UserResponse** representa una respuesta a una solicitud GetUserSettings para un usuario individual. 
  
```XML
<UserResponse>
   <ErrorCode/>
   <ErrorMessage/>
   <RedirectTarget/>
   <UserSettingErrors/>
   <UserSettings/>
</UserResponse>
```

 **UserResponse**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Representa un código de error devuelto por el servicio de detección automática.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Representa un mensaje asociado a un código de error devuelto por el servicio de detección automática.  <br/> |
|[RedirectTarget (SOAP)](redirecttarget-soap.md) <br/> |Contiene el destino de la dirección URL de redirección o de correo electrónico.  <br/> |
|[UserSettingErrors (SOAP)](usersettingerrors-soap.md) <br/> |Representa una colección de información sobre la configuración que no se pudo devolver.  <br/> |
|[UserSettings (SOAP)](usersettings-soap.md) <br/> |La configuración solicitada para el usuario.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ArrayOfUserResponse (SOAP)](arrayofuserresponse-soap.md) <br/> |Contiene una matriz de respuestas de usuario.  <br/> |
|[UserResponses (SOAP)](userresponses-soap.md) <br/> |Contiene las opciones de configuración de cada usuario solicitado.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[Elementos XML de detección automática soap para Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

