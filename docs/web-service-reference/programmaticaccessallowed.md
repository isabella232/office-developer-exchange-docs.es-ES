---
title: ProgrammaticAccessAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a1fc7dff-a303-4809-b7f4-9672f86c183c
description: El elemento ProgrammaticAccessAllowed especifica si el acceso mediante programación está habilitado para los datos administrados con derechos.
ms.openlocfilehash: 3e7f16a148fe1d81bbf942c098591f108529d456
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523849"
---
# <a name="programmaticaccessallowed"></a>ProgrammaticAccessAllowed

El **elemento ProgrammaticAccessAllowed** especifica si el acceso mediante programación está habilitado para los datos administrados con derechos. 
  
```XML
<ProgrammaticAccessAllowed> true | false </ProgrammaticAccessAllowed>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[RightsManagementLicenseData](rightsmanagementlicensedata.md)
  
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** para el **elemento ProgrammaticAccessAllowed** indica que los datos son accesibles mediante programación. Un valor de **false** indica que los datos no son accesibles mediante programación. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

