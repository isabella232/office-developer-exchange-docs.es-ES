---
title: Valor (ProtectionRuleValueType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Value
api_type:
- schema
ms.assetid: b039bd6e-2198-47cf-9c78-a5e8b9d51c98
description: El elemento Value identifica un único destinatario o departamento de remitentes.
ms.openlocfilehash: 908ea451800abc343fb6e4d4a4ed98d57223bd23
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465243"
---
# <a name="value-protectionrulevaluetype"></a>Valor (ProtectionRuleValueType)

El elemento **Value** identifica un único destinatario o departamento de remitentes. 
  
```XML
<Value/>
```

**ProtectionRuleValueType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Destinatarioes](recipientis.md) <br/> |Especifica que cualquier destinatario del mensaje de correo electrónico coincide con cualquiera de los destinatarios especificados en los elementos secundarios de **valor** .  <br/> |
|[SenderDepartments](senderdepartments.md) <br/> |Especifica que el Departamento del remitente coincide con cualquiera de los departamentos especificados en los elementos secundarios de **valor** .  <br/> |
   
## <a name="text-value"></a>Valor de texto

Este elemento debe contener un valor de cadena no vacío.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

