---
title: ActionType (HoldActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f50449b9-e73b-43c5-af96-6433bf434dce
description: El elemento ActionType indica el tipo de acción para la retención.
ms.openlocfilehash: 8f2796df818dac2bd285b055aa44fbcecd0de5e6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457861"
---
# <a name="actiontype-holdactiontype"></a><span data-ttu-id="5321d-103">ActionType (HoldActionType)</span><span class="sxs-lookup"><span data-stu-id="5321d-103">ActionType (HoldActionType)</span></span>

<span data-ttu-id="5321d-104">El elemento **ActionType** indica el tipo de acción para la retención.</span><span class="sxs-lookup"><span data-stu-id="5321d-104">The **ActionType** element indicates the type of action for the hold.</span></span> 
  
```XML
<ActionType> Create | Update | Remove </ActionType>
```

 <span data-ttu-id="5321d-105">**HoldActionType**</span><span class="sxs-lookup"><span data-stu-id="5321d-105">**HoldActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5321d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5321d-106">Attributes and elements</span></span>

<span data-ttu-id="5321d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5321d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5321d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5321d-108">Attributes</span></span>

<span data-ttu-id="5321d-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5321d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5321d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5321d-110">Child elements</span></span>

<span data-ttu-id="5321d-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5321d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5321d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5321d-112">Parent elements</span></span>

[<span data-ttu-id="5321d-113">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="5321d-113">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="5321d-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5321d-114">Text value</span></span>

<span data-ttu-id="5321d-115">El valor de texto del elemento **ActionType** es el tipo de retención establecido en un buzón.</span><span class="sxs-lookup"><span data-stu-id="5321d-115">The text value of the **ActionType** element is the type of hold set on a mailbox.</span></span> <span data-ttu-id="5321d-116">Un valor de texto de **Create** indica que se creará una retención de buzón.</span><span class="sxs-lookup"><span data-stu-id="5321d-116">A text value of **Create** indicates that a mailbox hold will be created.</span></span> <span data-ttu-id="5321d-117">Un valor de texto de **Update** indica que se actualizará una retención de buzón.</span><span class="sxs-lookup"><span data-stu-id="5321d-117">A text value of **Update** indicates that a mailbox hold will be updated.</span></span> <span data-ttu-id="5321d-118">Un valor de texto **quitar** indica que se quitará una retención de buzón.</span><span class="sxs-lookup"><span data-stu-id="5321d-118">A text value of **Remove** indicates that a mailbox hold will be removed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5321d-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5321d-119">Remarks</span></span>

<span data-ttu-id="5321d-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="5321d-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5321d-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5321d-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5321d-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5321d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5321d-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="5321d-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5321d-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5321d-124">Schema name</span></span>  <br/> |<span data-ttu-id="5321d-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5321d-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="5321d-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5321d-126">Validation file</span></span>  <br/> |<span data-ttu-id="5321d-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5321d-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5321d-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5321d-128">Can be empty</span></span>  <br/> |<span data-ttu-id="5321d-129">false</span><span class="sxs-lookup"><span data-stu-id="5321d-129">false</span></span>  <br/> |
   

