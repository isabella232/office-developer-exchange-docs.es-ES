---
title: IsWritable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d4af8eee-7001-4a8e-b9bd-d14882f2406b
description: El elemento IsWritable especifica si se puede escribir el contacto subyacente o el destinatario de Active Directory.
ms.openlocfilehash: 2663e18f2589516f304930b86a717455b6ab77c3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516716"
---
# <a name="iswritable"></a>IsWritable

El **elemento IsWritable** especifica si se puede escribir el contacto subyacente o el destinatario de Active Directory. 
  
```XML
<IsWritable> true | false </IsWritable>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[Attribution (PersonaAttributionType)](attribution-personaattributiontype.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el **elemento IsWritable** indica que el contacto u objeto de Active Directory está disponible para el acceso de escritura. Un valor de **false** indica que el contacto u objeto de Active Directory no está disponible para el acceso de escritura. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  

