---
title: LobbyBypass
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e05ed6eb-00ae-49c8-8341-43f6e0d728ff
description: El elemento LobbyBypass especifica la reunión en línea para omitir la sala de espera virtual.
ms.openlocfilehash: 9ecc920acd9e1aea3476ad1194d6c7d0529b21c7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836246"
---
# <a name="lobbybypass"></a>LobbyBypass

El elemento **LobbyBypass** especifica la reunión en línea para omitir la sala de espera virtual. 
  
```XML
<LobbyBypass> Disabled | EnabledForGatewayParticipants </LobbyBypass>
```

 **LobbyBypassType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[OnlineMeetingSettings](onlinemeetingsettings.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **LobbyBypass** puede ser **deshabilitado** o **EnabledForGatewayParticipants**. El valor **deshabilitado** indica que el desvío de la sala de espera está deshabilitado por lo que deben tener acceso todos los asistentes a la reunión a través de la sala de espera virtual. El valor de **EnabledForGatewayParticipants** indica que el desvío de la sala de espera está habilitado para los participantes de teléfono. 
  
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  

