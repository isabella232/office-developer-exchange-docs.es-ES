---
title: SetTeamMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d6ee7cc-8f88-4de2-ae5c-cabf2f2193d0
description: El elemento SetTeamMailbox contiene una solicitud para establecer un buzón de sitio.
ms.openlocfilehash: e4b7ebd308f4b58b6b6491289f24b9176c5dcf15
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465264"
---
# <a name="setteammailbox"></a><span data-ttu-id="a589a-103">SetTeamMailbox</span><span class="sxs-lookup"><span data-stu-id="a589a-103">SetTeamMailbox</span></span>

<span data-ttu-id="a589a-104">El elemento **SetTeamMailbox** contiene una solicitud para establecer un buzón de sitio.</span><span class="sxs-lookup"><span data-stu-id="a589a-104">The **SetTeamMailbox** element contains a request to set a site mailbox.</span></span> 
  
```XML
<SetTeamMailbox>
   <EmailAddress/>
   <SharePointSiteUrl/>
   <State/>
</SetTeamMailbox>
```

 <span data-ttu-id="a589a-105">**SetTeamMailboxRequestType**</span><span class="sxs-lookup"><span data-stu-id="a589a-105">**SetTeamMailboxRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a589a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a589a-106">Attributes and elements</span></span>

<span data-ttu-id="a589a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a589a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a589a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a589a-108">Attributes</span></span>

<span data-ttu-id="a589a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a589a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a589a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a589a-110">Child elements</span></span>

<span data-ttu-id="a589a-111">[EmailAddress (EmailAddressType)](emailaddress-emailaddresstype.md)  |  [SharePointSiteUrl](sharepointsiteurl.md)  |  [State (TeamMailboxLifecycleStateType)](state-teammailboxlifecyclestatetype.md)</span><span class="sxs-lookup"><span data-stu-id="a589a-111">[EmailAddress (EmailAddressType)](emailaddress-emailaddresstype.md) | [SharePointSiteUrl](sharepointsiteurl.md) | [State (TeamMailboxLifecycleStateType)](state-teammailboxlifecyclestatetype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a589a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a589a-112">Parent elements</span></span>

<span data-ttu-id="a589a-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a589a-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a589a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a589a-114">Remarks</span></span>

<span data-ttu-id="a589a-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a589a-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a589a-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a589a-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a589a-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a589a-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a589a-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="a589a-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a589a-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a589a-119">Schema name</span></span>  <br/> |<span data-ttu-id="a589a-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a589a-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a589a-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a589a-121">Validation file</span></span>  <br/> |<span data-ttu-id="a589a-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a589a-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a589a-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a589a-123">Can be empty</span></span>  <br/> ||
   

