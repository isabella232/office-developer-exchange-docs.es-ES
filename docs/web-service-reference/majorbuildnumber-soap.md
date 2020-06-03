---
title: MajorBuildNumber (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 7335b1c1-0b47-4452-a8cb-d19cddcfc281
description: El elemento MajorBuildNumber representa el número de compilación principal del servidor.
ms.openlocfilehash: 60a8cbeb4b689da85bbb72c2d93759799b913f2f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465887"
---
# <a name="majorbuildnumber-soap"></a>MajorBuildNumber (SOAP)

El elemento **MajorBuildNumber** representa el número de compilación principal del servidor. 
  
```XML
<MajorBuildNumber/>
```

 **XS: int**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ServerVersionInfo (SOAP)](serverversioninfo-soap.md) <br/> |Contiene la versión del servidor que ha procesado la solicitud.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento MajorBuildNumber es un entero que representa el número de compilación principal del servidor que procesó la solicitud.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
  
[Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)
  
[Operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)

