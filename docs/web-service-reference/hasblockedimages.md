---
title: HasBlockedImages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ddeb11db-797d-4939-91d5-3e44be5f0778
description: El elemento HasBlockedImages especifica un valor booleano que indica si el elemento ha bloqueado imágenes.
ms.openlocfilehash: 1f4031f95ce5040eabf6993320a184afaf469bd1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59537837"
---
# <a name="hasblockedimages"></a>HasBlockedImages

El **elemento HasBlockedImages** especifica un valor booleano que indica si el elemento ha bloqueado imágenes. 
  
```XML
<HasBlockedImages> true | false </HasBlockedImages>
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
|[Item](item.md) <br/> |Representa un elemento genérico en el Exchange almacén.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el **elemento HasBlockedImages** indica que el elemento ha bloqueado imágenes. Un valor de **false** indica que el elemento no tiene ninguna imagen bloqueada. 
  
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

