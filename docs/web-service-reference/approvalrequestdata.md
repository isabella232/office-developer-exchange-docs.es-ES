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
ms.openlocfilehash: decbd4d646a56b9810387adcdb6a9049da89bc38
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462307"
---
# <a name="approvalrequestdata"></a><span data-ttu-id="ef2a9-103">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="ef2a9-103">ApprovalRequestData</span></span>

<span data-ttu-id="ef2a9-104">El elemento **ApprovalRequestData** especifica el estado de aprobación de un mensaje de solicitud de aprobación.</span><span class="sxs-lookup"><span data-stu-id="ef2a9-104">The **ApprovalRequestData** element specifies the approval state of an approval request message.</span></span> 
  
```xml
<ApprovalRequestData>
   <IsUndecidedApprovalRequest/>
   <ApprovalDecision/>
   <ApprovalDecisionMaker/>
   <ApprovalDecisionTime/>
</ApprovalRequestData>
```

 <span data-ttu-id="ef2a9-105">**ApprovalRequestDataType**</span><span class="sxs-lookup"><span data-stu-id="ef2a9-105">**ApprovalRequestDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef2a9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ef2a9-106">Attributes and elements</span></span>

<span data-ttu-id="ef2a9-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ef2a9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef2a9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ef2a9-108">Attributes</span></span>

<span data-ttu-id="ef2a9-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ef2a9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef2a9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ef2a9-110">Child elements</span></span>

<span data-ttu-id="ef2a9-111">[IsUndecidedApprovalRequest](isundecidedapprovalrequest.md)  |  [ApprovalDecision](approvaldecision.md)  |  [ApprovalDecisionMaker](approvaldecisionmaker.md)  |  [ApprovalDecisionTime](approvaldecisiontime.md)</span><span class="sxs-lookup"><span data-stu-id="ef2a9-111">[IsUndecidedApprovalRequest](isundecidedapprovalrequest.md) | [ApprovalDecision](approvaldecision.md) | [ApprovalDecisionMaker](approvaldecisionmaker.md) | [ApprovalDecisionTime](approvaldecisiontime.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ef2a9-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ef2a9-112">Parent elements</span></span>

[<span data-ttu-id="ef2a9-113">Message</span><span class="sxs-lookup"><span data-stu-id="ef2a9-113">Message</span></span>](message-ex15websvcsotherref.md)
  
## <a name="remarks"></a><span data-ttu-id="ef2a9-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ef2a9-114">Remarks</span></span>

<span data-ttu-id="ef2a9-115">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ef2a9-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="ef2a9-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ef2a9-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef2a9-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ef2a9-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef2a9-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef2a9-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ef2a9-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ef2a9-119">Schema Name</span></span>  <br/> |<span data-ttu-id="ef2a9-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ef2a9-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="ef2a9-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ef2a9-121">Validation File</span></span>  <br/> |<span data-ttu-id="ef2a9-122">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ef2a9-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ef2a9-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ef2a9-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="ef2a9-124">Verdadero</span><span class="sxs-lookup"><span data-stu-id="ef2a9-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef2a9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef2a9-125">See also</span></span>

- [<span data-ttu-id="ef2a9-126">Message</span><span class="sxs-lookup"><span data-stu-id="ef2a9-126">Message</span></span>](message-ex15websvcsotherref.md)
- [<span data-ttu-id="ef2a9-127">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ef2a9-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

