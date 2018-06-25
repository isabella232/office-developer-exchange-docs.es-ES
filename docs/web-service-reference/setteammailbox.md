---
title: SetTeamMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d6ee7cc-8f88-4de2-ae5c-cabf2f2193d0
description: El elemento SetTeamMailbox contiene una solicitud para establecer un buzón del sitio.
ms.openlocfilehash: 708863168f4e89775deee8c5d66427df41515089
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837455"
---
# <a name="setteammailbox"></a><span data-ttu-id="ed9d0-103">SetTeamMailbox</span><span class="sxs-lookup"><span data-stu-id="ed9d0-103">SetTeamMailbox</span></span>

<span data-ttu-id="ed9d0-104">El elemento **SetTeamMailbox** contiene una solicitud para establecer un buzón del sitio.</span><span class="sxs-lookup"><span data-stu-id="ed9d0-104">The **SetTeamMailbox** element contains a request to set a site mailbox.</span></span> 
  
```XML
<SetTeamMailbox>
   <EmailAddress/>
   <SharePointSiteUrl/>
   <State/>
</SetTeamMailbox>
```

 <span data-ttu-id="ed9d0-105">**SetTeamMailboxRequestType**</span><span class="sxs-lookup"><span data-stu-id="ed9d0-105">**SetTeamMailboxRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ed9d0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ed9d0-106">Attributes and elements</span></span>

<span data-ttu-id="ed9d0-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ed9d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ed9d0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ed9d0-108">Attributes</span></span>

<span data-ttu-id="ed9d0-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ed9d0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ed9d0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ed9d0-110">Child elements</span></span>

<span data-ttu-id="ed9d0-111">[EmailAddress (EmailAddressType)](emailaddress-emailaddresstype.md) | [SharePointSiteUrl](sharepointsiteurl.md) | [estado (TeamMailboxLifecycleStateType)](state-teammailboxlifecyclestatetype.md)</span><span class="sxs-lookup"><span data-stu-id="ed9d0-111">[EmailAddress (EmailAddressType)](emailaddress-emailaddresstype.md) | [SharePointSiteUrl](sharepointsiteurl.md) | [State (TeamMailboxLifecycleStateType)](state-teammailboxlifecyclestatetype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ed9d0-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ed9d0-112">Parent elements</span></span>

<span data-ttu-id="ed9d0-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ed9d0-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ed9d0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ed9d0-114">Remarks</span></span>

<span data-ttu-id="ed9d0-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ed9d0-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ed9d0-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ed9d0-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ed9d0-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ed9d0-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed9d0-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ed9d0-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ed9d0-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ed9d0-119">Schema name</span></span>  <br/> |<span data-ttu-id="ed9d0-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ed9d0-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ed9d0-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ed9d0-121">Validation file</span></span>  <br/> |<span data-ttu-id="ed9d0-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ed9d0-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ed9d0-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ed9d0-123">Can be empty</span></span>  <br/> ||
   

