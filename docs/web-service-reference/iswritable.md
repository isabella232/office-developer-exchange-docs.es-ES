---
title: IsWritable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d4af8eee-7001-4a8e-b9bd-d14882f2406b
description: El elemento IsWritable especifica si se puede escribir en el contacto subyacente o en el destinatario de Active Directory.
ms.openlocfilehash: 96075adc1772027456f8829eee43bdc734644c09
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467574"
---
# <a name="iswritable"></a>IsWritable

El elemento **IsWritable** especifica si se puede escribir en el contacto subyacente o en el destinatario de Active Directory. 
  
```XML
<IsWritable> true | false </IsWritable>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[Atribución (PersonaAttributionType)](attribution-personaattributiontype.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** para el elemento **IsWritable** indica que el objeto de contacto o de Active Directory está disponible para el acceso de escritura. Un valor de **false** indica que el contacto o el objeto de Active Directory no está disponible para el acceso de escritura. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  

