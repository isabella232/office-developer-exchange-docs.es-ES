---
title: Domain (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 849629a0-0467-422f-88f6-3b8a95c17bba
description: El elemento Domain contiene un dominio federado en una respuesta GetFederationInformation o contiene un dominio cuyas opciones de configuración se solicitan en una solicitud GetDomainSettings.
ms.openlocfilehash: a2e69dc845f9841931263fe90e39550bceb81ab8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520825"
---
# <a name="domain-soap"></a>Domain (SOAP)

El **elemento Domain** contiene un dominio federado en una respuesta **GetFederationInformation** o contiene un dominio cuyas opciones de configuración se solicitan en una solicitud **GetDomainSettings.** 
  
```XML
<Domain/> 
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Domains (SOAP)](domains-soap.md) <br/> |Representa los dominios cuyas opciones de configuración se devuelven en una operación **GetDomainSettings** o los dominios que la organización ha federado en una operación **GetFederationInformation.**  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento Domain** representa un nombre de dominio. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   

