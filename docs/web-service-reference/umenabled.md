---
title: UmEnabled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UmEnabled
api_type:
- schema
ms.assetid: 87382d9b-0c02-49ec-85dc-3f5918df3195
description: El elemento UmEnabled indica si la mensajería unificada está habilitada para una cuenta.
ms.openlocfilehash: 9ff6432324e3a15b9ae805a7d6d836c9c895059c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527156"
---
# <a name="umenabled"></a>UmEnabled

El **elemento UmEnabled** indica si la mensajería unificada está habilitada para una cuenta. 
  
```XML
<UmEnabled>true | false</UmEnabled>
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
|[UnifiedMessagingConfiguration](unifiedmessagingconfiguration.md) <br/> |Contiene información de configuración del servicio de mensajería unificada.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento UmEnabled** es **true** si la mensajería unificada está habilitada para la cuenta; de lo contrario, el valor es **false**.
  
## <a name="remarks"></a>Comentarios

Se requiere este elemento.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

