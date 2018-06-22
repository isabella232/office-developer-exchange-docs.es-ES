---
title: ActionType (HoldActionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f50449b9-e73b-43c5-af96-6433bf434dce
description: El elemento ActionType indica el tipo de acción para la suspensión.
ms.openlocfilehash: cb1cfa8a1306c4a6cacf5c82824d19cab57e7941
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763384"
---
# <a name="actiontype-holdactiontype"></a><span data-ttu-id="d1841-103">ActionType (HoldActionType)</span><span class="sxs-lookup"><span data-stu-id="d1841-103">ActionType (HoldActionType)</span></span>

<span data-ttu-id="d1841-104">El elemento **ActionType** indica el tipo de acción para la suspensión.</span><span class="sxs-lookup"><span data-stu-id="d1841-104">The **ActionType** element indicates the type of action for the hold.</span></span> 
  
```XML
<ActionType> Create | Update | Remove </ActionType>
```

 <span data-ttu-id="d1841-105">**HoldActionType**</span><span class="sxs-lookup"><span data-stu-id="d1841-105">**HoldActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d1841-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d1841-106">Attributes and elements</span></span>

<span data-ttu-id="d1841-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d1841-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d1841-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d1841-108">Attributes</span></span>

<span data-ttu-id="d1841-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d1841-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d1841-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d1841-110">Child elements</span></span>

<span data-ttu-id="d1841-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d1841-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d1841-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d1841-112">Parent elements</span></span>

[<span data-ttu-id="d1841-113">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="d1841-113">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="d1841-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d1841-114">Text value</span></span>

<span data-ttu-id="d1841-115">El valor de texto del elemento **ActionType** es el tipo de espera que se establece en un buzón.</span><span class="sxs-lookup"><span data-stu-id="d1841-115">The text value of the **ActionType** element is the type of hold set on a mailbox.</span></span> <span data-ttu-id="d1841-116">Un valor de texto de **creación** indica que se creará una suspensión de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d1841-116">A text value of **Create** indicates that a mailbox hold will be created.</span></span> <span data-ttu-id="d1841-117">Un valor de texto de **actualización** indica que se actualizará una suspensión de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d1841-117">A text value of **Update** indicates that a mailbox hold will be updated.</span></span> <span data-ttu-id="d1841-118">Un valor de texto de **Quitar** indica que se eliminará una suspensión de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d1841-118">A text value of **Remove** indicates that a mailbox hold will be removed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d1841-119">Notas</span><span class="sxs-lookup"><span data-stu-id="d1841-119">Remarks</span></span>

<span data-ttu-id="d1841-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d1841-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d1841-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d1841-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d1841-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d1841-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1841-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d1841-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d1841-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d1841-124">Schema name</span></span>  <br/> |<span data-ttu-id="d1841-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d1841-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="d1841-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d1841-126">Validation file</span></span>  <br/> |<span data-ttu-id="d1841-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d1841-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d1841-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d1841-128">Can be empty</span></span>  <br/> |<span data-ttu-id="d1841-129">falso</span><span class="sxs-lookup"><span data-stu-id="d1841-129">false</span></span>  <br/> |
   

