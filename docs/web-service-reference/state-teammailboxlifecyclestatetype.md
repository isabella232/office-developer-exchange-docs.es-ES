---
title: State (TeamMailboxLifecycleStateType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3b1bc531-6988-41c3-9aad-3f5ad5b732a9
description: El elemento State contiene el estado de ciclo de vida que se establece en un buzón de sitio.
ms.openlocfilehash: 5189ee8573fd33d2265fd60c47bb40d17b16b8fe
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538971"
---
# <a name="state-teammailboxlifecyclestatetype"></a>State (TeamMailboxLifecycleStateType)

El **elemento State** contiene el estado de ciclo de vida que se establece en un buzón de sitio. 
  
```XML
<State> Active | Closed | Unlinked | PendingDelete </State>
```

**TeamMailboxLifecycleStateType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[SetTeamMailbox](setteammailbox.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento State** es el estado de ciclo de vida que se establece en un buzón de sitio. Un valor de texto **de Active** indica que un buzón de sitio está en uso activo. Un valor de texto **de Closed** indica que un buzón de sitio se ha cerrado y no está en uso activo. Un valor de texto **de Unlinked** indica que un buzón de sitio no está vinculado a un entorno de colaboración basado en web. Los **valores Active**, **Closed** y **PendingDelete** son mutuamente excluyentes, pero el valor **Unlinked** no es mutuamente excluyente de los otros valores. Un valor de texto de **PendingDelete** indica que un buzón de sitio está pendiente de eliminación. Un buzón de sitio debe cerrarse para poder establecerse como **PendingDelete**.
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

