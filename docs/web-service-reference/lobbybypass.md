---
title: LobbyBypass
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e05ed6eb-00ae-49c8-8341-43f6e0d728ff
description: El elemento LobbyBypass especifica la configuración de la reunión en línea para omitir la sala de espera virtual.
ms.openlocfilehash: 41ab9c3f846112d2b679bbb477a0de355a477ffa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540786"
---
# <a name="lobbybypass"></a>LobbyBypass

El **elemento LobbyBypass** especifica la configuración de la reunión en línea para omitir la sala de espera virtual. 
  
```XML
<LobbyBypass> Disabled | EnabledForGatewayParticipants </LobbyBypass>
```

 **LobbyBypassType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[OnlineMeetingSettings](onlinemeetingsettings.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento LobbyBypass** puede ser **Disabled** o **EnabledForGatewayParticipants**. El **valor Disabled** indica que la omisión de la sala de espera está deshabilitada, por lo que todos los asistentes a la reunión deben tener acceso a través de la sala de espera virtual. El **valor EnabledForGatewayParticipants** indica que la omisión de la sala de espera está habilitada para los participantes telefónicos. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  

