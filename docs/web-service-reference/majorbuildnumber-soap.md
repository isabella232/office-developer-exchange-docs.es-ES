---
title: MajorBuildNumber (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 7335b1c1-0b47-4452-a8cb-d19cddcfc281
description: El elemento MajorBuildNumber representa el número de compilación principal del servidor.
ms.openlocfilehash: da6431a1e97ab7d57e398eeffaa683e3cbb877d5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511106"
---
# <a name="majorbuildnumber-soap"></a>MajorBuildNumber (SOAP)

El **elemento MajorBuildNumber** representa el número de compilación principal del servidor. 
  
```XML
<MajorBuildNumber/>
```

 **xs:int**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ServerVersionInfo (SOAP)](serverversioninfo-soap.md) <br/> |Contiene la versión del servidor que procesó la solicitud.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento MajorBuildNumber es un entero que representa el número de compilación principal del servidor que procesó la solicitud.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
  
[Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)
  
[Operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)

