---
title: SendPrompt
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22cb5a30-75d9-49a8-9d98-255f2e8a722d
description: El elemento SendPrompt especifica el tipo de acción permitida para una opción de votación.
ms.openlocfilehash: 98ffc69cdc94c3f7b9c325bee0c1ebaeb407ee96
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462104"
---
# <a name="sendprompt"></a>SendPrompt

El elemento **SendPrompt** especifica el tipo de acción permitida para una opción de votación. 
  
```XML
<SendPrompt> None | Send | VotingOption </SendPrompt>
```

 **SendPromptType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[VotingOptionData](votingoptiondata.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **SendPrompt** es una acción de la opción de voto. En la siguiente tabla se enumeran los valores posibles para este elemento. 
  
****

|**Valor**|**Descripción**|
|:-----|:-----|
|Ninguno  <br/> |Ninguna acción.  <br/> |
|Enviar  <br/> |La respuesta se envía inmediatamente.  <br/> |
|VotingOption  <br/> |El aprobador puede escribir comentarios al aprobarlos o rechazarlos.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[VotingOptionData](votingoptiondata.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

