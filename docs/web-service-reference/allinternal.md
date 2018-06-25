---
title: AllInternal
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AllInternal
api_type:
- schema
ms.assetid: b7e5072f-5d9f-4ee0-b58b-4d75d878ea1c
description: El elemento AllInternal se evalúa como true si todos los destinatarios de un mensaje de correo electrónico son internos a la organización del remitente.
ms.openlocfilehash: 0ffd4178e711e3117497eed682e3fd3e0594989b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763426"
---
# <a name="allinternal"></a>AllInternal

El elemento **AllInternal** se evalúa como **true** si todos los destinatarios de un mensaje de correo electrónico son internos a la organización del remitente. 
  
```xml
<AllInternal/>
```

 **ProtectionRuleAllInternalType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Condición](condition.md) <br/> |Identifica la condición que debe cumplirse para el elemento de acción de la regla que se va a ejecutar.  <br/> |
|[Y (ProtectionRuleAndType)](and-protectionruleandtype.md) <br/> |Especifica que deben coincidir con todos los elementos secundarios para evaluar en **true**.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El elemento **AllInternal** debe estar vacío. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

