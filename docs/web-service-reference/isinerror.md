---
title: IsInError
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsInError
api_type:
- schema
ms.assetid: f56e6c31-a566-4761-8755-d90ffe6fe790
description: El elemento IsInError indica si la regla está en una condición de error.
ms.openlocfilehash: 9f77bbe11106174d0e82c5257e08c3728d67c60c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836033"
---
# <a name="isinerror"></a>IsInError

El elemento **IsInError** indica si la regla está en una condición de error. 
  
```XML
<IsInError/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Regla (RuleType)](rule-ruletype.md) <br/> |Representa una regla en el buzón del usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** indica que la regla está en una condición de error. Un valor de **false** indica que la regla no está en una condición de error. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

