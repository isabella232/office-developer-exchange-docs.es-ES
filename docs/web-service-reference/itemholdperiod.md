---
title: ItemHoldPeriod
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 30369db5-4d45-40e8-bc83-3236667fc404
description: El elemento ItemHoldPeriod especifica la cantidad de tiempo para contener contenido que coincide con la consulta de buzón.
ms.openlocfilehash: de56c410c876917bbe8d545c9ef4f38ee6948b21
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522855"
---
# <a name="itemholdperiod"></a>ItemHoldPeriod

El **elemento ItemHoldPeriod** especifica la cantidad de tiempo para contener contenido que coincide con la consulta de buzón. 
  
```XML
<ItemHoldPeriod/>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[SetHoldOnMailboxes](setholdonmailboxes.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto puede ser "Unlimited" o el valor de cadena de cualquier [valor de Timespan.](https://msdn.microsoft.com/library/1ecy8h51%28v=vs.110%29.aspx) 
  
## <a name="remarks"></a>Comentarios

Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[SetHoldOnMailboxes](setholdonmailboxes.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

