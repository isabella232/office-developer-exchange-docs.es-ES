---
title: Valor (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 24eaa473-0024-47e2-b7d2-051d5dd4f53c
description: El elemento Value especifica el valor de una EmailAddress asociada a una matriz de atribuciones.
ms.openlocfilehash: 45af2aaab7d2475ae46ae24ed13b1435f5b352c6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467602"
---
# <a name="value-emailaddresstype"></a>Valor (EmailAddressType)

El elemento **Value** especifica el valor de una **EmailAddress** asociada a una matriz de atribuciones. 
  
```XML
<Value>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
   <OriginalDisplayName/>
</Value>
```

**EmailAddressType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

[Name (cadena)](name-string.md)  |  [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)  |  [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)  |  [MailboxType](mailboxtype.md)  |  [Itemid](itemid.md)  |  [OriginalDisplayName](originaldisplayname.md)
  
### <a name="parent-elements"></a>Elementos principales

[EmailAddressAttributedValue](emailaddressattributedvalue.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

