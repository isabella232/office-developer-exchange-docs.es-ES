---
title: AutodiscoverResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 203a5ac3-ebd0-4514-acbe-bc1c74638127
description: El elemento AutodiscoverResponse (SOAP) representa el elemento base de todas las respuestas que devuelve el servicio de detección automática.
ms.openlocfilehash: 71bbb0f1aa6602a260c163ccfdfd3c3d38442e31
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514875"
---
# <a name="autodiscoverresponse-soap"></a>AutodiscoverResponse (SOAP)

El **elemento AutodiscoverResponse (SOAP)** representa el elemento base de todas las respuestas que devuelve el servicio de detección automática. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[UserResponses (SOAP)](userresponses-soap.md) <br/> |Representa una colección de [elementos UserResponse (SOAP).](userresponse-soap.md)  <br/> |
|[UserSettingErrors (SOAP)](usersettingerrors-soap.md) <br/> |Representa una colección [de elementos UserSettingError (SOAP).](usersettingerror-soap.md)  <br/> |
|[UserSettings (SOAP)](usersettings-soap.md) <br/> |Representa una colección de [elementos UserSetting (SOAP).](usersetting-soap.md)  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
- [Operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)
- [Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)

