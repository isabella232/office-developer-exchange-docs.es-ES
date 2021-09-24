---
title: IsExternalMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5cc83174-e684-42c8-b72a-f82d3de3bb2f
description: El elemento IsExternalMailbox indica si el buzón es externo a la organización.
ms.openlocfilehash: f2435356a7315c51f3d99aeedf0ae2b21500981c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524234"
---
# <a name="isexternalmailbox"></a>IsExternalMailbox

El **elemento IsExternalMailbox** indica si el buzón es externo a la organización. 
  
```XML
<IsExternalMailbox>true | false</IsExternalMailbox>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[SearchableMailbox](searchablemailbox.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el **elemento IsExternalMailbox** indica que el buzón está en una organización externa. Un valor de **false** indica que el buzón está en la organización. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

