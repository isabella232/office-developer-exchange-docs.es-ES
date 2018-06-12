---
title: Estado (HoldStatusType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fee3f1f9-e868-49fa-a554-7ff096964718
description: El elemento Status especifica el estado de suspensión para un buzón de correo.
ms.openlocfilehash: c40dc865d2b305ac86fa40d536e2d516a14260ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837579"
---
# <a name="status-holdstatustype"></a><span data-ttu-id="1f93a-103">Estado (HoldStatusType)</span><span class="sxs-lookup"><span data-stu-id="1f93a-103">Status (HoldStatusType)</span></span>

<span data-ttu-id="1f93a-104">El elemento **Status** especifica el estado de suspensión para un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="1f93a-104">The **Status** element specifies the hold status for a mailbox.</span></span> 
  
```XML
<Status> NotOnHold | Pending | OnHold | PartialHold | Failed </Status>
```

 <span data-ttu-id="1f93a-105">**HoldStatusType**</span><span class="sxs-lookup"><span data-stu-id="1f93a-105">**HoldStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1f93a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1f93a-106">Attributes and elements</span></span>

<span data-ttu-id="1f93a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1f93a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f93a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1f93a-108">Attributes</span></span>

<span data-ttu-id="1f93a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1f93a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1f93a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1f93a-110">Child elements</span></span>

<span data-ttu-id="1f93a-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1f93a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1f93a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1f93a-112">Parent elements</span></span>

[<span data-ttu-id="1f93a-113">MailboxHoldStatus</span><span class="sxs-lookup"><span data-stu-id="1f93a-113">MailboxHoldStatus</span></span>](mailboxholdstatus.md)
  
## <a name="text-value"></a><span data-ttu-id="1f93a-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1f93a-114">Text value</span></span>

<span data-ttu-id="1f93a-115">El valor de texto del elemento de **estado** es el estado de espera de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="1f93a-115">The text value of the **Status** element is the hold status of a mailbox.</span></span> <span data-ttu-id="1f93a-116">El elemento de **estado** puede tener los valores de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="1f93a-116">The **Status** element can have the values in the following list.</span></span> 
  
> <span data-ttu-id="1f93a-117">NotOnHold - el buzón no está en espera.</span><span class="sxs-lookup"><span data-stu-id="1f93a-117">NotOnHold - The mailbox is not on hold.</span></span>
    
> <span data-ttu-id="1f93a-118">Pendiente: el buzón de correo está pendiente se colocan o publicado en espera.</span><span class="sxs-lookup"><span data-stu-id="1f93a-118">Pending - The mailbox is pending either being placed or released on hold.</span></span> 
    
> <span data-ttu-id="1f93a-119">OnHold - la suspensión se ha aplicado correctamente al buzón.</span><span class="sxs-lookup"><span data-stu-id="1f93a-119">OnHold - The hold was successfully applied to the mailbox.</span></span> 
    
> <span data-ttu-id="1f93a-120">PartialHold - la suspensión se ha aplicado correctamente para algunos buzones de correo, pero no para todos los buzones.</span><span class="sxs-lookup"><span data-stu-id="1f93a-120">PartialHold - The hold was successfully applied to some mailboxes but not to all mailboxes.</span></span>
    
> <span data-ttu-id="1f93a-121">No se pudo - la suspensión no se pudieron aplicar al buzón.</span><span class="sxs-lookup"><span data-stu-id="1f93a-121">Failed - The hold failed to apply to the mailbox.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1f93a-122">Notas</span><span class="sxs-lookup"><span data-stu-id="1f93a-122">Remarks</span></span>

<span data-ttu-id="1f93a-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="1f93a-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1f93a-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1f93a-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1f93a-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1f93a-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f93a-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1f93a-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1f93a-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1f93a-127">Schema name</span></span>  <br/> |<span data-ttu-id="1f93a-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1f93a-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="1f93a-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1f93a-129">Validation file</span></span>  <br/> |<span data-ttu-id="1f93a-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1f93a-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1f93a-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1f93a-131">Can be empty</span></span>  <br/> ||
   

