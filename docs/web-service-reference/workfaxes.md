---
title: WorkFaxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 95d115a1-2743-4416-af6f-1ef1be8c4e93
description: El elemento WorkFaxes especifica una matriz de números de fax de trabajo y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: 5186f6d389732e78bd06d21f13e8cefabf57c921
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19841006"
---
# <a name="workfaxes"></a>WorkFaxes

El elemento **WorkFaxes** especifica una matriz de números de fax de trabajo y los identificadores de sus atribuciones de origen para el rol asociado. 
  
```XML
<WorkFaxes>
   <PhoneNumberAttributedValue/>
</WorkFaxes>
```

 **ArrayOfPhoneNumberAttributedValuesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[PhoneNumberAttributedValue](phonenumberattributedvalue.md)
  
### <a name="parent-elements"></a>Elementos principales

[Rol](persona.md)
  
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

