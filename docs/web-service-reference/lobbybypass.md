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
# <a name="lobbybypass"></a><span data-ttu-id="83846-103">LobbyBypass</span><span class="sxs-lookup"><span data-stu-id="83846-103">LobbyBypass</span></span>

<span data-ttu-id="83846-104">El elemento **LobbyBypass** especifica la reunión en línea para omitir la sala de espera virtual.</span><span class="sxs-lookup"><span data-stu-id="83846-104">The **LobbyBypass** element specifies the online meeting setting to bypass the virtual lobby.</span></span> 
  
```XML
<LobbyBypass> Disabled | EnabledForGatewayParticipants </LobbyBypass>
```

 <span data-ttu-id="83846-105">**LobbyBypassType**</span><span class="sxs-lookup"><span data-stu-id="83846-105">**LobbyBypassType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83846-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="83846-106">Attributes and elements</span></span>

<span data-ttu-id="83846-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="83846-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83846-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="83846-108">Attributes</span></span>

<span data-ttu-id="83846-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="83846-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83846-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="83846-110">Child elements</span></span>

<span data-ttu-id="83846-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="83846-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="83846-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="83846-112">Parent elements</span></span>

[<span data-ttu-id="83846-113">OnlineMeetingSettings</span><span class="sxs-lookup"><span data-stu-id="83846-113">OnlineMeetingSettings</span></span>](onlinemeetingsettings.md)
  
## <a name="text-value"></a><span data-ttu-id="83846-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="83846-114">Text value</span></span>

<span data-ttu-id="83846-115">El valor de texto del elemento **LobbyBypass** puede ser **deshabilitado** o **EnabledForGatewayParticipants**.</span><span class="sxs-lookup"><span data-stu-id="83846-115">The text value of the **LobbyBypass** element can be either **Disabled** or **EnabledForGatewayParticipants**.</span></span> <span data-ttu-id="83846-116">El valor **deshabilitado** indica que el desvío de la sala de espera está deshabilitado por lo que deben tener acceso todos los asistentes a la reunión a través de la sala de espera virtual.</span><span class="sxs-lookup"><span data-stu-id="83846-116">The **Disabled** value indicates that the lobby bypass is disabled so all meeting attendees must access through the virtual lobby.</span></span> <span data-ttu-id="83846-117">El valor de **EnabledForGatewayParticipants** indica que el desvío de la sala de espera está habilitado para los participantes de teléfono.</span><span class="sxs-lookup"><span data-stu-id="83846-117">The **EnabledForGatewayParticipants** value indicates that the lobby bypass is enabled for telephone participants.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="83846-118">Notas</span><span class="sxs-lookup"><span data-stu-id="83846-118">Remarks</span></span>

<span data-ttu-id="83846-119">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="83846-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="83846-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="83846-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  

