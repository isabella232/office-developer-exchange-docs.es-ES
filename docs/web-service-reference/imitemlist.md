---
title: ImItemList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 556457d5-a730-4131-853f-1198c27c5942
description: El elemento ImItemList contiene una lista de grupos de mensajería instantánea y contactos de mensajería instantánea.
ms.openlocfilehash: fdd2865ceb1553a7f75d7059b08ea96ce89aa096
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59547249"
---
# <a name="imitemlist"></a>ImItemList

El **elemento ImItemList** contiene una lista de grupos de mensajería instantánea y contactos de mensajería instantánea. 
  
```XML
<ImItemList>
   <Groups/>
   <Personas/>
</ImItemList>
```

 **ImItemListType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

[Grupos (ArrayOfImGroupType)](groups-arrayofimgrouptype.md)  |  [Personas](personas-ex15websvcsotherref.md)
  
### <a name="parent-elements"></a>Elementos principales

[GetImItemsResponse](getimitemsresponse.md)  |  [GetImItemListResponse](getimitemlistresponse.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

