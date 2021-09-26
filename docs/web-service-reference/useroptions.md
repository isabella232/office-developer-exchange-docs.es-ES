---
title: UserOptions
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1acbb8a3-9110-4427-a06c-7e6e627e969f
description: El elemento UserOptions especifica la lista de opciones de votación de un mensaje.
ms.openlocfilehash: 3f4a30cf66700210dc0a6bcce4d5d4521a288a7c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541696"
---
# <a name="useroptions"></a>UserOptions

El **elemento UserOptions** especifica la lista de opciones de votación de un mensaje. 
  
```XML
<UserOptions>
   <VotingOptionData>
</UserOptions>
```

 **ArrayOfVotingOptionDataType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

[VotingOptionData](votingoptiondata.md)
  
### <a name="parent-elements"></a>Elementos principales

[VotingInformation](votinginformation.md)
  
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
   
## <a name="see-also"></a>Consulte también



[VotingInformation](votinginformation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

