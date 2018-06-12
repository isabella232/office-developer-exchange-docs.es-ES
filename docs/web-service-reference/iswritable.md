---
title: IsWritable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d4af8eee-7001-4a8e-b9bd-d14882f2406b
description: El elemento IsWritable especifica si se puede escribir en el contacto subyacente o el destinatario de Active Directory.
ms.openlocfilehash: 03f258d01ecfc12dfa4e09ac88f4a75340d2acf3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836158"
---
# <a name="iswritable"></a>IsWritable

El elemento **IsWritable** especifica si se puede escribir en el contacto subyacente o el destinatario de Active Directory. 
  
```XML
<IsWritable> true | false </IsWritable>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[Atribución (PersonaAttributionType)](attribution-personaattributiontype.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** para el elemento **IsWritable** indica que el contacto o el objeto de Active Directory está disponible para el acceso de escritura. Un valor de **false** indica que el contacto o el objeto de Active Directory no está disponible para el acceso de escritura. 
  
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  

