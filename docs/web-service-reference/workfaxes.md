---
title: WorkFaxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 95d115a1-2743-4416-af6f-1ef1be8c4e93
description: El elemento WorkFaxes especifica una matriz de números de fax de trabajo y los identificadores de sus atribuciones de origen para la persona asociada.
ms.openlocfilehash: a3ba76f322d653a8244cdeebd8c2a9ada9504859
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525508"
---
# <a name="workfaxes"></a>WorkFaxes

El **elemento WorkFaxes** especifica una matriz de números de fax de trabajo y los identificadores de sus atribuciones de origen para la persona asociada. 
  
```XML
<WorkFaxes>
   <PhoneNumberAttributedValue/>
</WorkFaxes>
```

 **ArrayOfPhoneNumberAttributedValuesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[PhoneNumberAttributedValue](phonenumberattributedvalue.md)
  
### <a name="parent-elements"></a>Elementos principales

[Rol](persona.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

