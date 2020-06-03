---
title: GroupId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 656d9b9a-8a65-4a75-8466-5b0d96512dab
description: El elemento GroupId identifica de forma exclusiva a un grupo.
ms.openlocfilehash: 3b8de4d0fef95e2caff4db0d90bb303830022d36
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530095"
---
# <a name="groupid"></a>GroupId

El elemento **GROUPID** identifica de forma exclusiva a un grupo. 
  
```XML
<GroupId Id="" ChangeKey=""/>
```

 **ItemIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|Id  <br/> |El valor de texto del atributo **ID** es el identificador del grupo.  <br/> |
|ChangeKey  <br/> |El valor de texto del atributo **changekey** es la clave de cambio del grupo.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[AddNewImContactToGroup](addnewimcontacttogroup.md)  |  [AddNewTelUriContactToGroup](addnewteluricontacttogroup.md)  |  [AddImContactToGroup](addimcontacttogroup.md)  |  [RemoveContactFromImList](removecontactfromimlist.md)  |  [RemoveImContactFromGroup](removeimcontactfromgroup.md)  |  [RemoveImGroup](removeimgroup.md)  |  [RemoveDistributionGroupFromImList](removedistributiongroupfromimlist.md)  |  [SetImGroup](setimgroup.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |messages. xsd  <br/> |
|Puede estar vacío  <br/> ||
   

