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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458099"
---
# <a name="lobbybypass"></a><span data-ttu-id="c1a49-103">LobbyBypass</span><span class="sxs-lookup"><span data-stu-id="c1a49-103">LobbyBypass</span></span>

<span data-ttu-id="c1a49-104">El elemento **LobbyBypass** especifica la configuración de reunión en línea para omitir la sala de espera virtual.</span><span class="sxs-lookup"><span data-stu-id="c1a49-104">The **LobbyBypass** element specifies the online meeting setting to bypass the virtual lobby.</span></span> 
  
```XML
<LobbyBypass> Disabled | EnabledForGatewayParticipants </LobbyBypass>
```

 <span data-ttu-id="c1a49-105">**LobbyBypassType**</span><span class="sxs-lookup"><span data-stu-id="c1a49-105">**LobbyBypassType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1a49-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c1a49-106">Attributes and elements</span></span>

<span data-ttu-id="c1a49-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c1a49-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1a49-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c1a49-108">Attributes</span></span>

<span data-ttu-id="c1a49-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c1a49-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1a49-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c1a49-110">Child elements</span></span>

<span data-ttu-id="c1a49-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c1a49-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c1a49-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c1a49-112">Parent elements</span></span>

[<span data-ttu-id="c1a49-113">OnlineMeetingSettings</span><span class="sxs-lookup"><span data-stu-id="c1a49-113">OnlineMeetingSettings</span></span>](onlinemeetingsettings.md)
  
## <a name="text-value"></a><span data-ttu-id="c1a49-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c1a49-114">Text value</span></span>

<span data-ttu-id="c1a49-115">El valor de texto del elemento **LobbyBypass** puede estar **deshabilitado** o en **EnabledForGatewayParticipants**.</span><span class="sxs-lookup"><span data-stu-id="c1a49-115">The text value of the **LobbyBypass** element can be either **Disabled** or **EnabledForGatewayParticipants**.</span></span> <span data-ttu-id="c1a49-116">El valor **Disabled** indica que la omisión de la sala de espera está deshabilitada para que todos los asistentes a la reunión deban tener acceso a través de la sala virtual.</span><span class="sxs-lookup"><span data-stu-id="c1a49-116">The **Disabled** value indicates that the lobby bypass is disabled so all meeting attendees must access through the virtual lobby.</span></span> <span data-ttu-id="c1a49-117">El valor **EnabledForGatewayParticipants** indica que la omisión de la sala de espera está habilitada para los participantes telefónicos.</span><span class="sxs-lookup"><span data-stu-id="c1a49-117">The **EnabledForGatewayParticipants** value indicates that the lobby bypass is enabled for telephone participants.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c1a49-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c1a49-118">Remarks</span></span>

<span data-ttu-id="c1a49-119">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c1a49-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c1a49-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1a49-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  

