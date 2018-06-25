---
title: Usuario (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: c6bc0031-bc1d-41bd-84e4-9074a5b77012
description: El elemento de usuario representa la identidad de un único usuario.
ms.openlocfilehash: a8dcb22f5c74a9622f978f34e48146115351fe82
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840899"
---
# <a name="user-soap"></a>Usuario (SOAP)

El elemento de **usuario** representa la identidad de un único usuario. 
  
```XML
<User>
    <LegacyDN/>
    <Mailbox/>
    <RequestedSettings/>
</User>
```

 **User**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[LegacyDN (SOAP)](legacydn-soap.md) <br/> |Representa el nombre distintivo heredado de buzón de correo alternativas.  <br/> |
|[Buzón de correo (SOAP)](mailbox-soap.md) <br/> |Contiene la dirección de correo electrónico del usuario para ser detectado.  <br/> |
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |Contiene los nombres de las opciones de configuración solicitado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Usuarios (SOAP)](users-soap.md) <br/> |Representa una colección de elementos de **usuario** .  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
  
[Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)
  
[Operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)

