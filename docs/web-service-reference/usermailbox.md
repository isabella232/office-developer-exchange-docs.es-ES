---
title: UserMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1d47141c-3c3f-45b8-90c5-33a44adb34b2
description: El elemento UserMailbox identifica un buzón de usuario.
ms.openlocfilehash: c2a66b23de5e4b312f60019f0b4ecfb4088b3da2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542620"
---
# <a name="usermailbox"></a>UserMailbox

El **elemento UserMailbox** identifica un buzón de usuario. 
  
```XML
<UserMailbox Id="" IsArchive=""/>
```

 **UserMailboxType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|Id  <br/> |El valor de texto del **atributo Id** es el identificador del buzón.  <br/> |
|IsArchive  <br/> |El valor de texto del **atributo IsArchive** indica si el buzón es un buzón de archivo. Un valor de texto **de true** para el **atributo IsArchive** indica que el buzón es un buzón de archivo. Un valor de **false** para el **atributo IsArchive** indica que el buzón es un buzón principal.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[Buzones (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md)  |  [MailboxStatisticsSearchResult](mailboxstatisticssearchresult.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |true  <br/> |
   

