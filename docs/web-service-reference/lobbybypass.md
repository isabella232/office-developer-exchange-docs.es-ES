---
title: LobbyBypass
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e05ed6eb-00ae-49c8-8341-43f6e0d728ff
description: El elemento LobbyBypass especifica la configuración de reunión en línea para omitir la sala de espera virtual.
ms.openlocfilehash: 6940428c944b9d4d64acc6dbbf3993576e1932eb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458099"
---
# <a name="lobbybypass"></a>LobbyBypass

El elemento **LobbyBypass** especifica la configuración de reunión en línea para omitir la sala de espera virtual. 
  
```XML
<LobbyBypass> Disabled | EnabledForGatewayParticipants </LobbyBypass>
```

 **LobbyBypassType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[OnlineMeetingSettings](onlinemeetingsettings.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **LobbyBypass** puede estar **deshabilitado** o en **EnabledForGatewayParticipants**. El valor **Disabled** indica que la omisión de la sala de espera está deshabilitada para que todos los asistentes a la reunión deban tener acceso a través de la sala virtual. El valor **EnabledForGatewayParticipants** indica que la omisión de la sala de espera está habilitada para los participantes telefónicos. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  

