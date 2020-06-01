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
description: El elemento de dominio contiene un dominio federado en una respuesta de GetFederationInformation o contiene un dominio con los valores de configuración que se solicitan en una solicitud de GetDomainSettings.
ms.openlocfilehash: f90c608ee1fc3356a227bca6411eaeff0c1e8b22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456986"
---
# <a name="domain-soap"></a>Dominio (SOAP)

El elemento de **dominio** contiene un dominio federado en una respuesta de **GetFederationInformation** o contiene un dominio con los valores de configuración que se solicitan en una solicitud de **GetDomainSettings** . 
  
```XML
<Domain/> 
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Dominios (SOAP)](domains-soap.md) <br/> |Representa los dominios a los que se devuelven las opciones de configuración en una operación **GetDomainSettings** o los dominios que la organización ha federado en una operación **GetFederationInformation** .  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **Domain** representa un nombre de dominio. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   

