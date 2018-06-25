---
title: GroupId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 656d9b9a-8a65-4a75-8466-5b0d96512dab
description: El elemento GroupId identifica de forma única un grupo.
ms.openlocfilehash: eaba176321c0dd872b71ef50cbaa298d1277bb79
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835750"
---
# <a name="groupid"></a>GroupId

El elemento **GroupId** identifica de forma única un grupo. 
  
```XML
<GroupId Id="" ChangeKey=""/>
```

 **ItemIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|Id  <br/> |El valor de texto del atributo **Id** es el identificador del grupo.  <br/> |
|ChangeKey  <br/> |El valor de texto del atributo **ChangeKey** es la clave de cambio del grupo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[AddNewImContactToGroup](addnewimcontacttogroup.md) | [AddNewTelUriContactToGroup](addnewteluricontacttogroup.md) | [AddImContactToGroup](addimcontacttogroup.md) | [RemoveContactFromImList](removecontactfromimlist.md) | [RemoveImContactFromGroup](removeimcontactfromgroup.md) | [RemoveImGroup](removeimgroup.md)  |  [RemoveDistributionGroupFromImList](removedistributiongroupfromimlist.md) | [SetImGroup](setimgroup.md)
  
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
   

