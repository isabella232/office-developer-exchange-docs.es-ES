---
title: UserOptions
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1acbb8a3-9110-4427-a06c-7e6e627e969f
description: El elemento UserOptions especifica la lista de opciones en un mensaje de votación.
ms.openlocfilehash: 8a5bdbc254e3c0bce8822633d2714bc928f15f13
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840917"
---
# <a name="useroptions"></a>UserOptions

El elemento **UserOptions** especifica la lista de opciones de votación de un mensaje. 
  
```XML
<UserOptions>
   <VotingOptionData>
</UserOptions>
```

 **ArrayOfVotingOptionDataType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[VotingOptionData](votingoptiondata.md)
  
### <a name="parent-elements"></a>Elementos principales

[VotingInformation](votinginformation.md)
  
## <a name="remarks"></a>Notas

Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[VotingInformation](votinginformation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

