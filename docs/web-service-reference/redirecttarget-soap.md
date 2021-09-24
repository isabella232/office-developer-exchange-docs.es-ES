---
title: RedirectTarget (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: f8162724-cf9a-4543-a1ad-5846c8b10bfa
description: El elemento RedirectTarget (SOAP) contiene el destino de la dirección URL de redirección o dirección de correo electrónico.
ms.openlocfilehash: 0e09529f62dfde66f1ef05875bb0b0a0886db452
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513545"
---
# <a name="redirecttarget-soap"></a>RedirectTarget (SOAP)

El [elemento RedirectTarget (SOAP)](redirecttarget-soap.md) contiene el destino de la dirección URL de redirección o dirección de correo electrónico. 
  
```XML
<RedirectTarget/>
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
|[UserResponse (SOAP)](userresponse-soap.md) <br/> |Representa una respuesta a una solicitud GetUserSettings para un usuario individual.  <br/> |
|[DomainResponse (SOAP)](domainresponse-soap.md) <br/> |Contiene la configuración solicitada para el dominio especificado.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto contiene el destino de la dirección URL de redirección o dirección de correo electrónico que se debe usar para una solicitud GetUserSettings o GetDomainSettings posterior.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   

