---
title: ImItemList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 556457d5-a730-4131-853f-1198c27c5942
description: El elemento ImItemList contiene una lista de contactos de mensajería instantánea y de grupos de mensajería instantáneos.
ms.openlocfilehash: 490ac57da0c7ae7bedc75e94b7e21dc30c9da23f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835896"
---
# <a name="imitemlist"></a>ImItemList

El elemento **ImItemList** contiene una lista de contactos de mensajería instantánea y de grupos de mensajería instantáneos. 
  
```XML
<ImItemList>
   <Groups/>
   <Personas/>
</ImItemList>
```

 **ImItemListType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[Grupos (ArrayOfImGroupType)](groups-arrayofimgrouptype.md) | [roles](personas-ex15websvcsotherref.md)
  
### <a name="parent-elements"></a>Elementos principales

[GetImItemsResponse](getimitemsresponse.md) | [GetImItemListResponse](getimitemlistresponse.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

