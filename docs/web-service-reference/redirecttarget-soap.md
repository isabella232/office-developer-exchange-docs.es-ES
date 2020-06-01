---
title: RedirectTarget (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f8162724-cf9a-4543-a1ad-5846c8b10bfa
description: El elemento RedirectTarget (SOAP) contiene el destino de la dirección URL de redirección o de correo electrónico.
ms.openlocfilehash: 092d575560379d43b12dd98a3efa155b59c31450
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462202"
---
# <a name="redirecttarget-soap"></a>RedirectTarget (SOAP)

El elemento [RedirectTarget (SOAP)](redirecttarget-soap.md) contiene el destino de la dirección URL de redirección o de correo electrónico. 
  
```XML
<RedirectTarget/>
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
|[UserResponse (SOAP)](userresponse-soap.md) <br/> |Representa una respuesta a una solicitud de GetUserSettings para un usuario individual.  <br/> |
|[DomainResponse (SOAP)](domainresponse-soap.md) <br/> |Contiene la configuración solicitada para el dominio especificado.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto contiene el destino de la dirección URL de redirección o de correo electrónico que se debe usar para una solicitud GetUserSettings o GetDomainSettings subsiguiente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   

