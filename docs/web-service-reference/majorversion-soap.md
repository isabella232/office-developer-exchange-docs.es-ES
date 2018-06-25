---
title: MajorVersion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 0b2a83cf-e173-4073-9603-b2ea3b36ec1a
description: El elemento MajorVersion representa el número de versión principal para el servidor.
ms.openlocfilehash: ca619d4c36e17ca9a811019f0a13b45353cab1e2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836333"
---
# <a name="majorversion-soap"></a>MajorVersion (SOAP)

El elemento **MajorVersion** representa el número de versión principal para el servidor. 
  
```XML
<MajorVersion/>
```

 **int**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ServerVersionInfo (SOAP)](serverversioninfo-soap.md) <br/> |Contiene la versión del servidor que procesa la solicitud.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto para el elemento **MajorVersion** es un entero que representa el número de versión principal del servidor que procesa la solicitud. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
  
[Operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)

