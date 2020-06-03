---
title: UserRoles
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: be003e12-3496-468d-a61c-48af0b819654
description: El elemento UserRoles especifica las funciones de usuario que el usuario que realiza la llamada o el usuario en el que actúa la aplicación de socio de llamada desea aplicar a la llamada actual.
ms.openlocfilehash: 5155b82781321b16d1b58fdcaffe7b8cf2372717
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467133"
---
# <a name="userroles"></a>UserRoles

El elemento **UserRoles** especifica las funciones de usuario que el usuario que realiza la llamada o el usuario en el que actúa la aplicación de socio de llamada desea aplicar a la llamada actual. 
  
```XML
<UserRoles>
   <Role/>
</UserRoles>
```

 **NonEmptyArrayOfRoleType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
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
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   

