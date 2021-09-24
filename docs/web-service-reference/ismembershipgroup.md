---
title: IsMembershipGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0dc3e285-8f49-48ad-b844-37041c0d782b
description: El elemento IsMembershipGroup especifica un valor booleano que indica si la entidad es un grupo de distribución o un buzón.
ms.openlocfilehash: 111a517a5258a48aada1c7768c908d62f3a47b9e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540982"
---
# <a name="ismembershipgroup"></a>IsMembershipGroup

El **elemento IsMembershipGroup** especifica un valor booleano que indica si la entidad es un grupo de distribución o un buzón. 
  
```XML
<IsMembershipGroup>true | false</IsMembershipGroup>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SearchableMailbox](searchablemailbox.md) <br/> |Especifica un buzón devuelto desde una **solicitud GetSearchableMailboxes.**  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el **elemento IsMembershipGroup** indica que la entidad es un grupo de distribución o un buzón. Un valor de false indica que la entidad no es un grupo de distribución o un buzón. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

