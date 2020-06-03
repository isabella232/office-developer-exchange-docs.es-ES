---
title: AutodiscoverResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 203a5ac3-ebd0-4514-acbe-bc1c74638127
description: El elemento AutodiscoverResponse (SOAP) representa el elemento base para todas las respuestas devueltas por el servicio Detección automática.
ms.openlocfilehash: 81fd557578bde9552d07e24386c93903e44a9afa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463968"
---
# <a name="autodiscoverresponse-soap"></a>AutodiscoverResponse (SOAP)

El elemento **AutodiscoverResponse (SOAP)** representa el elemento base para todas las respuestas devueltas por el servicio Detección automática. 
  
- [AutodiscoverResponse (SOAP)](autodiscoverresponse-soap.md)
  
```XML
<AutodiscoverResponse>
    <UserResponses/>
    <UserSettingErrors/>
    <UserSettings/>
</AutodiscoverResponse>

```

 **AutodiscoverResponse**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[UserResponses (SOAP)](userresponses-soap.md) <br/> |Representa una colección de elementos [UserResponse (SOAP)](userresponse-soap.md) .  <br/> |
|[UserSettingErrors (SOAP)](usersettingerrors-soap.md) <br/> |Representa una colección de elementos [UserSettingError (SOAP)](usersettingerror-soap.md) .  <br/> |
|[UserSettings (SOAP)](usersettings-soap.md) <br/> |Representa una colección de elementos [UserSetting (SOAP)](usersetting-soap.md) .  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguna.
  
## <a name="text-value"></a>Valor de texto

Ninguna.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
- [Operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)
- [Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)

