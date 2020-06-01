---
title: State (TeamMailboxLifecycleStateType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b1bc531-6988-41c3-9aad-3f5ad5b732a9
description: El elemento State contiene el estado del ciclo de vida que se establece en un buzón del sitio.
ms.openlocfilehash: 597946b48649d997f8dd57823b4e0fcc091a6f84
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465166"
---
# <a name="state-teammailboxlifecyclestatetype"></a>State (TeamMailboxLifecycleStateType)

El elemento **State** contiene el estado del ciclo de vida que se establece en un buzón del sitio. 
  
```XML
<State> Active | Closed | Unlinked | PendingDelete </State>
```

**TeamMailboxLifecycleStateType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[SetTeamMailbox](setteammailbox.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento de **Estado** es el estado de ciclo de vida que se establece en un buzón de sitio. Un valor de texto **activo** indica que un buzón de sitio está en uso. Un valor de texto de **Closed** indica que se ha cerrado un buzón de sitio y no está en uso activo. Un valor de texto de **unlinkd** indica que un buzón de sitio no está vinculado a un entorno de colaboración basado en Web. Los valores **Active**, **Closed**y **PendingDelete** se excluyen mutuamente, pero el valor **desvinculado** no se excluye mutuamente de los demás valores. Un valor de texto de **PendingDelete** indica que hay un buzón de sitio pendiente de eliminación. Un buzón de sitio tiene que cerrarse antes de que se pueda establecer como **PendingDelete**.
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> ||
   

