---
title: SentCcMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SentCcMe
api_type:
- schema
ms.assetid: bf5044e4-cbdf-4e24-a16f-b6454a51fcd5
description: El elemento SentCcMe indica si el propietario del buzón tiene que estar en la propiedad CcRecipients de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar.
ms.openlocfilehash: 634a83d477efbe8683255c4fab71e3f7f1ab2191
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837354"
---
# <a name="sentccme"></a>SentCcMe

El elemento **SentCcMe** indica si el propietario del buzón tiene que estar en la propiedad **CcRecipients** de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar. 
  
```XML
<SentCcMe>true | false</SentCcMe>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Condiciones](conditions.md) <br/> |Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.  <br/> |
|[Excepciones](exceptions.md) <br/> |Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** indica que debe ser el propietario del buzón en la propiedad **CcRecipients** de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar. Un valor de **false** indica que no debe ser el propietario del buzón en la propiedad **CcRecipients** de los mensajes entrantes en orden para la condición o la excepción que se debe aplicar. 
  
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

