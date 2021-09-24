---
title: UserRoles
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: be003e12-3496-468d-a61c-48af0b819654
description: El elemento UserRoles especifica los roles de usuario que el usuario que realiza la llamada o el usuario en el que actúa la aplicación de socio de llamada quiere aplicar a la llamada actual.
ms.openlocfilehash: c861cda9a010e909c9ecc5303ddc637a14bcb824
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514980"
---
# <a name="userroles"></a>UserRoles

El **elemento UserRoles** especifica los roles de usuario que el usuario que realiza la llamada o el usuario en el que actúa la aplicación de socio de llamada quiere aplicar a la llamada actual. 
  
```XML
<UserRoles>
   <Role/>
</UserRoles>
```

 **NonEmptyArrayOfRoleType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[Rol](role.md)
  
### <a name="parent-elements"></a>Elementos principales

[ManagementRole](managementrole.md)
  
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
   

