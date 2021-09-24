---
title: SentOnlyToMe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SentOnlyToMe
api_type:
- schema
ms.assetid: b6d4dea5-812d-4b29-917d-071ebd7ddd92
description: El elemento SentOnlyToMe indica si el propietario del buzón debe ser el único de la propiedad ToRecipients de los mensajes entrantes para que se aplique la condición o excepción.
ms.openlocfilehash: c82989cbfc3725b1c8a4fea560d9f8ce30956ea5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59534310"
---
# <a name="sentonlytome"></a>SentOnlyToMe

El **elemento SentOnlyToMe** indica si el propietario del buzón debe ser el único de la propiedad **ToRecipients** de los mensajes entrantes para que se aplique la condición o excepción. 
  
```XML
<SentOnlyToMe/>true | false</SentOnlyToMe>
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
|[Condiciones](conditions.md) <br/> |Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.  <br/> |
|[Excepciones](exceptions.md) <br/> |Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** indica que el propietario del buzón debe ser el único de la propiedad **ToRecipients** de los mensajes entrantes para que se aplique la condición o excepción. Un valor **de false** indica que el propietario del buzón no debe ser el único de la propiedad **ToRecipients** de los mensajes entrantes para que se aplique la condición o excepción. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

