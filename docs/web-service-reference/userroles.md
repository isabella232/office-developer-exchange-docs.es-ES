---
title: UserRoles
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: be003e12-3496-468d-a61c-48af0b819654
description: El elemento UserRoles especifica las funciones de usuario que el usuario realiza la llamada, o el usuario que la aplicación de socio llamada actúa como, desea aplicar a la llamada actual.
ms.openlocfilehash: 19dc1a7e00decb9141326b53b650d72101013c11
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840926"
---
# <a name="userroles"></a>UserRoles

El elemento **UserRoles** especifica las funciones de usuario que el usuario realiza la llamada, o el usuario que la aplicación de socio llamada actúa como, desea aplicar a la llamada actual. 
  
```XML
<UserRoles>
   <Role/>
</UserRoles>
```

 **NonEmptyArrayOfRoleType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[Role](role.md)
  
### <a name="parent-elements"></a>Elementos principales

[ManagementRole](managementrole.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

