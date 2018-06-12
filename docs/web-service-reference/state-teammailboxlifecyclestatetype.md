---
title: Estado (TeamMailboxLifecycleStateType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b1bc531-6988-41c3-9aad-3f5ad5b732a9
description: El elemento de estado contiene el estado del ciclo de vida que se haya establecido en un buzón del sitio.
ms.openlocfilehash: accd70d36cc34e7364387b98a2e94c56b91f012f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837571"
---
# <a name="state-teammailboxlifecyclestatetype"></a>Estado (TeamMailboxLifecycleStateType)

El elemento de **estado** contiene el estado del ciclo de vida que se haya establecido en un buzón del sitio. 
  
```XML
<State> Active | Closed | Unlinked | PendingDelete </State>
```

**TeamMailboxLifecycleStateType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[SetTeamMailbox](setteammailbox.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento de **estado** es el estado de ciclo de vida que se haya establecido en un buzón del sitio. Un valor de texto de **activo** indica que un buzón del sitio está en uso. Un valor de texto de **cerrada** indica que un buzón del sitio se ha cerrado y no está en uso. Un valor de texto de **no vinculados** indica que un buzón del sitio no está vinculado a un entorno de colaboración basado en web. Los valores **activo**, **cerrado**y **PendingDelete** son mutuamente excluyentes, pero el valor **no vinculados** no es mutuamente exclusivos de los demás valores de la implementación. Un valor de texto de **PendingDelete** indica que un buzón del sitio está pendiente de eliminación. Tiene un buzón del sitio que se cierre antes de que se puede establecer como **PendingDelete**.
  
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

