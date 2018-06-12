---
title: Dominio (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 849629a0-0467-422f-88f6-3b8a95c17bba
description: El elemento de dominio contiene un dominio federado en una respuesta de GetFederationInformation o un dominio de las opciones de configuración para la que se solicitan en una solicitud de GetDomainSettings.
ms.openlocfilehash: 411ca866800322ef06eeecc2ab92adc6f711917c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764261"
---
# <a name="domain-soap"></a>Dominio (SOAP)

El elemento de **dominio** contiene un dominio federado en una respuesta de **GetFederationInformation** o un dominio de las opciones de configuración para la que se solicitan en una solicitud de **GetDomainSettings** . 
  
```XML
<Domain/> 
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Dominios (SOAP)](domains-soap.md) <br/> |Representa los dominios de las opciones de configuración para la que se devuelven en una operación **GetDomainSettings** o los dominios que la organización ha federados en una operación de **GetFederationInformation** .  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento de **dominio** representa un nombre de dominio. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |True  <br/> |
   

