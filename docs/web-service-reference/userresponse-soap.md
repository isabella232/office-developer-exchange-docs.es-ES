---
title: UserResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5007b1ba-bfcc-40d7-b1cb-e32fbaf54ffd
description: El elemento UserResponse representa una respuesta a una solicitud de GetUserSettings para un usuario individual.
ms.openlocfilehash: 6fcd82e06916df5acdd317cb44161c1b69e58574
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19840924"
---
# <a name="userresponse-soap"></a>UserResponse (SOAP)

El elemento **UserResponse** representa una respuesta a una solicitud de GetUserSettings para un usuario individual. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Representa un código de error devuelto por el servicio Detección automática.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Representa un mensaje en el que está asociado con un código de error devuelto por el servicio Detección automática.  <br/> |
|[RedirectTarget (SOAP)](redirecttarget-soap.md) <br/> |Contiene el destino de la dirección de correo electrónico o dirección URL de redirección.  <br/> |
|[UserSettingErrors (SOAP)](usersettingerrors-soap.md) <br/> |Representa una colección de información sobre la configuración que no se pudo devolver.  <br/> |
|[UserSettings (SOAP)](usersettings-soap.md) <br/> |La configuración solicitada para el usuario.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ArrayOfUserResponse (SOAP)](arrayofuserresponse-soap.md) <br/> |Contiene una matriz de las respuestas del usuario.  <br/> |
|[UserResponses (SOAP)](userresponses-soap.md) <br/> |Contiene las opciones de configuración para cada usuario solicitado.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[Elementos de Autodiscover XML SOAP para Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

