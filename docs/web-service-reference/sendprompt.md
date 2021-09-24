---
title: SendPrompt
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 22cb5a30-75d9-49a8-9d98-255f2e8a722d
description: El elemento SendPrompt especifica el tipo de acción permitido para una opción de votación.
ms.openlocfilehash: 32537210aadce91911d1fb5002fbafcaa70aa9ab
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59532135"
---
# <a name="sendprompt"></a>SendPrompt

El **elemento SendPrompt** especifica el tipo de acción permitido para una opción de votación. 
  
```XML
<SendPrompt> None | Send | VotingOption </SendPrompt>
```

 **SendPromptType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[VotingOptionData](votingoptiondata.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento SendPrompt** es una acción de opción de voto. En la tabla siguiente se enumeran los valores posibles para este elemento. 
  
****

|**Valor**|**Descripción**|
|:-----|:-----|
|Ninguno  <br/> |Sin acción.  <br/> |
|Enviar  <br/> |La respuesta se envía inmediatamente.  <br/> |
|VotingOption  <br/> |El aprobador puede escribir comentarios al aprobar o rechazar.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[VotingOptionData](votingoptiondata.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

