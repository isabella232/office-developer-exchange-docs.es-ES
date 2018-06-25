---
title: SendPrompt
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22cb5a30-75d9-49a8-9d98-255f2e8a722d
description: El elemento SendPrompt especifica el tipo de acción permitida para una opción de voto.
ms.openlocfilehash: f3220d957482ea04c46b014cdf1c67025d5ec21a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837346"
---
# <a name="sendprompt"></a>SendPrompt

El elemento **SendPrompt** especifica el tipo de acción permitida para una opción de voto. 
  
```XML
<SendPrompt> None | Send | VotingOption </SendPrompt>
```

 **SendPromptType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[VotingOptionData](votingoptiondata.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **SendPrompt** es una acción de opción votación. En la siguiente tabla se enumera los valores posibles para este elemento. 
  
****

|**Valor**|**Descripción**|
|:-----|:-----|
|None  <br/> |Ninguna acción.  <br/> |
|Envío  <br/> |La respuesta se envía inmediatamente.  <br/> |
|VotingOption  <br/> |El aprobador puede escribir comentarios durante la aprobación o rechazo.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[VotingOptionData](votingoptiondata.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

