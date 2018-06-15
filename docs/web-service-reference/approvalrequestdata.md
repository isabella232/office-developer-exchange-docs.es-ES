---
title: ApprovalRequestData
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6c971cf7-5c3a-4e5e-9a7d-048f4ac0aadb
description: El elemento ApprovalRequestData especifica el estado de aprobación de un mensaje de solicitud de aprobación.
ms.openlocfilehash: ed1c1e3db4edd2cf4de032dc61abd73e863d4f1d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763541"
---
# <a name="approvalrequestdata"></a><span data-ttu-id="917f3-103">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="917f3-103">ApprovalRequestData</span></span>

<span data-ttu-id="917f3-104">El elemento **ApprovalRequestData** especifica el estado de aprobación de un mensaje de solicitud de aprobación.</span><span class="sxs-lookup"><span data-stu-id="917f3-104">The **ApprovalRequestData** element specifies the approval state of an approval request message.</span></span> 
  
```xml
<ApprovalRequestData>
   <IsUndecidedApprovalRequest/>
   <ApprovalDecision/>
   <ApprovalDecisionMaker/>
   <ApprovalDecisionTime/>
</ApprovalRequestData>
```

 <span data-ttu-id="917f3-105">**ApprovalRequestDataType**</span><span class="sxs-lookup"><span data-stu-id="917f3-105">**ApprovalRequestDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="917f3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="917f3-106">Attributes and elements</span></span>

<span data-ttu-id="917f3-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="917f3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="917f3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="917f3-108">Attributes</span></span>

<span data-ttu-id="917f3-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="917f3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="917f3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="917f3-110">Child elements</span></span>

<span data-ttu-id="917f3-111">[IsUndecidedApprovalRequest](isundecidedapprovalrequest.md) | [ApprovalDecision](approvaldecision.md) | [ApprovalDecisionMaker](approvaldecisionmaker.md) | [ApprovalDecisionTime](approvaldecisiontime.md)</span><span class="sxs-lookup"><span data-stu-id="917f3-111">[IsUndecidedApprovalRequest](isundecidedapprovalrequest.md) | [ApprovalDecision](approvaldecision.md) | [ApprovalDecisionMaker](approvaldecisionmaker.md) | [ApprovalDecisionTime](approvaldecisiontime.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="917f3-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="917f3-112">Parent elements</span></span>

[<span data-ttu-id="917f3-113">Message</span><span class="sxs-lookup"><span data-stu-id="917f3-113">Message</span></span>](message-ex15websvcsotherref.md)
  
## <a name="remarks"></a><span data-ttu-id="917f3-114">Notas</span><span class="sxs-lookup"><span data-stu-id="917f3-114">Remarks</span></span>

<span data-ttu-id="917f3-115">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="917f3-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="917f3-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="917f3-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="917f3-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="917f3-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="917f3-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="917f3-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="917f3-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="917f3-119">Schema Name</span></span>  <br/> |<span data-ttu-id="917f3-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="917f3-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="917f3-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="917f3-121">Validation File</span></span>  <br/> |<span data-ttu-id="917f3-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="917f3-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="917f3-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="917f3-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="917f3-124">Verdadero</span><span class="sxs-lookup"><span data-stu-id="917f3-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="917f3-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="917f3-125">See also</span></span>

- [<span data-ttu-id="917f3-126">Message</span><span class="sxs-lookup"><span data-stu-id="917f3-126">Message</span></span>](message-ex15websvcsotherref.md)
- [<span data-ttu-id="917f3-127">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="917f3-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
