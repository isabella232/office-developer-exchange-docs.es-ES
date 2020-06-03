---
title: Estado (HoldStatusType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fee3f1f9-e868-49fa-a554-7ff096964718
description: El elemento status especifica el estado de retención de un buzón.
ms.openlocfilehash: cecfdfaf67b00b6f8cf02188e7a4df7062a732e4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459990"
---
# <a name="status-holdstatustype"></a><span data-ttu-id="5286c-103">Estado (HoldStatusType)</span><span class="sxs-lookup"><span data-stu-id="5286c-103">Status (HoldStatusType)</span></span>

<span data-ttu-id="5286c-104">El elemento **status** especifica el estado de retención de un buzón.</span><span class="sxs-lookup"><span data-stu-id="5286c-104">The **Status** element specifies the hold status for a mailbox.</span></span> 
  
```XML
<Status> NotOnHold | Pending | OnHold | PartialHold | Failed </Status>
```

 <span data-ttu-id="5286c-105">**HoldStatusType**</span><span class="sxs-lookup"><span data-stu-id="5286c-105">**HoldStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5286c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5286c-106">Attributes and elements</span></span>

<span data-ttu-id="5286c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5286c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5286c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5286c-108">Attributes</span></span>

<span data-ttu-id="5286c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5286c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5286c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5286c-110">Child elements</span></span>

<span data-ttu-id="5286c-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5286c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5286c-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5286c-112">Parent elements</span></span>

[<span data-ttu-id="5286c-113">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="5286c-113">MailboxHoldStatus</span></span>](mailboxholdstatus.md)
  
## <a name="text-value"></a><span data-ttu-id="5286c-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5286c-114">Text value</span></span>

<span data-ttu-id="5286c-115">El valor de texto del elemento de **Estado** es el estado de conservación de un buzón.</span><span class="sxs-lookup"><span data-stu-id="5286c-115">The text value of the **Status** element is the hold status of a mailbox.</span></span> <span data-ttu-id="5286c-116">El elemento **status** puede tener los valores de la siguiente lista.</span><span class="sxs-lookup"><span data-stu-id="5286c-116">The **Status** element can have the values in the following list.</span></span> 
  
> <span data-ttu-id="5286c-117">NotOnHold: el buzón de correo no está en suspensión.</span><span class="sxs-lookup"><span data-stu-id="5286c-117">NotOnHold - The mailbox is not on hold.</span></span>
    
> <span data-ttu-id="5286c-118">Pending: el buzón de correo está pendiente de ser colocado o lanzado en espera.</span><span class="sxs-lookup"><span data-stu-id="5286c-118">Pending - The mailbox is pending either being placed or released on hold.</span></span> 
    
> <span data-ttu-id="5286c-119">Cohold: la suspensión se aplicó correctamente al buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="5286c-119">OnHold - The hold was successfully applied to the mailbox.</span></span> 
    
> <span data-ttu-id="5286c-120">PartialHold: la retención se aplicó correctamente a algunos buzones, pero no a todos los buzones.</span><span class="sxs-lookup"><span data-stu-id="5286c-120">PartialHold - The hold was successfully applied to some mailboxes but not to all mailboxes.</span></span>
    
> <span data-ttu-id="5286c-121">Failed: no se pudo aplicar la retención al buzón.</span><span class="sxs-lookup"><span data-stu-id="5286c-121">Failed - The hold failed to apply to the mailbox.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5286c-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5286c-122">Remarks</span></span>

<span data-ttu-id="5286c-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5286c-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5286c-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5286c-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5286c-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5286c-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5286c-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="5286c-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5286c-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5286c-127">Schema name</span></span>  <br/> |<span data-ttu-id="5286c-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5286c-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="5286c-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5286c-129">Validation file</span></span>  <br/> |<span data-ttu-id="5286c-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5286c-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5286c-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5286c-131">Can be empty</span></span>  <br/> ||
   

