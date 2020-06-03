---
title: ApprovalDecision
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5e7c5687-cb9e-4f0b-ac8f-b82591914a39
description: El elemento ApprovalDecision especifica la decisión tomada en un mensaje de solicitud de aprobación.
ms.openlocfilehash: a8dc168edec882ba97cdea764f8d20c71ed85f8a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463450"
---
# <a name="approvaldecision"></a><span data-ttu-id="a635e-103">ApprovalDecision</span><span class="sxs-lookup"><span data-stu-id="a635e-103">ApprovalDecision</span></span>

<span data-ttu-id="a635e-104">El elemento **ApprovalDecision** especifica la decisión tomada en un mensaje de solicitud de aprobación.</span><span class="sxs-lookup"><span data-stu-id="a635e-104">The **ApprovalDecision** element specifies the decision made on an approval request message.</span></span> 
  
```XML
<ApprovalDecision> 1 | 2 </ApprovalDecision>
```

 <span data-ttu-id="a635e-105">**int**</span><span class="sxs-lookup"><span data-stu-id="a635e-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a635e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a635e-106">Attributes and elements</span></span>

<span data-ttu-id="a635e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a635e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a635e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a635e-108">Attributes</span></span>

<span data-ttu-id="a635e-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a635e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a635e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a635e-110">Child elements</span></span>

<span data-ttu-id="a635e-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a635e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a635e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a635e-112">Parent elements</span></span>

[<span data-ttu-id="a635e-113">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="a635e-113">ApprovalRequestData</span></span>](approvalrequestdata.md)
  
## <a name="text-value"></a><span data-ttu-id="a635e-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a635e-114">Text value</span></span>

<span data-ttu-id="a635e-115">El valor de texto del elemento **ApprovalDecision** es 1 si se aprueba y 2 si se rechaza.</span><span class="sxs-lookup"><span data-stu-id="a635e-115">The text value of the **ApprovalDecision** element is 1 if approved and 2 if rejected.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a635e-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a635e-116">Remarks</span></span>

<span data-ttu-id="a635e-117">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a635e-117">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="a635e-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a635e-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a635e-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a635e-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a635e-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="a635e-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a635e-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a635e-121">Schema Name</span></span>  <br/> |<span data-ttu-id="a635e-122">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a635e-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="a635e-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a635e-123">Validation File</span></span>  <br/> |<span data-ttu-id="a635e-124">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a635e-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a635e-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a635e-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="a635e-126">Verdadero</span><span class="sxs-lookup"><span data-stu-id="a635e-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a635e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a635e-127">See also</span></span>

- [<span data-ttu-id="a635e-128">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="a635e-128">ApprovalRequestData</span></span>](approvalrequestdata.md)
- [<span data-ttu-id="a635e-129">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a635e-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

