---
title: DraftItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c228f7e7-6dc8-476d-9b8c-99cd5b6f9f0c
description: El elemento DraftItemIds contiene una matriz de identificadores de elemento a los elementos de borrador de una conversación.
ms.openlocfilehash: 5e635e354c9d2d768bab5efaafafde272fe568d3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463576"
---
# <a name="draftitemids"></a>DraftItemIds

El elemento **DraftItemIds** contiene una matriz de identificadores de elemento a los elementos de borrador de una conversación. 
  
```XML
<DraftItemIds>
   <ItemId/>
   <OccirrenceItemId/>
   <RecurringMasterItemId/>
   <RecurringMasterItemIdRanges/>
</DraftItemIds>
```

 **NonEmptyArrayOfBaseItemIdsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

[Itemid](itemid.md)  |  [OccurrenceItemId](occurrenceitemid.md)  |  [RecurringMasterItemId](recurringmasteritemid.md)  |  [RecurringMasterItemIdRanges](recurringmasteritemidranges.md)
  
### <a name="parent-elements"></a>Elementos principales

[Conversación (ConversationType)](conversation-conversationtype.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   

