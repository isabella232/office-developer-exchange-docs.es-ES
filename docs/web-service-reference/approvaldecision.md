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
ms.openlocfilehash: 4ca73813440200e5d2fb9f920d81459d8cd5e4ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763537"
---
# <a name="approvaldecision"></a><span data-ttu-id="b5500-103">ApprovalDecision</span><span class="sxs-lookup"><span data-stu-id="b5500-103">ApprovalDecision</span></span>

<span data-ttu-id="b5500-104">El elemento **ApprovalDecision** especifica la decisión tomada en un mensaje de solicitud de aprobación.</span><span class="sxs-lookup"><span data-stu-id="b5500-104">The **ApprovalDecision** element specifies the decision made on an approval request message.</span></span> 
  
```XML
<ApprovalDecision> 1 | 2 </ApprovalDecision>
```

 <span data-ttu-id="b5500-105">**int**</span><span class="sxs-lookup"><span data-stu-id="b5500-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b5500-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b5500-106">Attributes and elements</span></span>

<span data-ttu-id="b5500-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b5500-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5500-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b5500-108">Attributes</span></span>

<span data-ttu-id="b5500-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b5500-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b5500-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b5500-110">Child elements</span></span>

<span data-ttu-id="b5500-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b5500-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b5500-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b5500-112">Parent elements</span></span>

[<span data-ttu-id="b5500-113">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="b5500-113">ApprovalRequestData</span></span>](approvalrequestdata.md)
  
## <a name="text-value"></a><span data-ttu-id="b5500-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b5500-114">Text value</span></span>

<span data-ttu-id="b5500-115">El valor de texto del elemento **ApprovalDecision** es 1 si aprueba y 2 si se rechaza.</span><span class="sxs-lookup"><span data-stu-id="b5500-115">The text value of the **ApprovalDecision** element is 1 if approved and 2 if rejected.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b5500-116">Notas</span><span class="sxs-lookup"><span data-stu-id="b5500-116">Remarks</span></span>

<span data-ttu-id="b5500-117">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="b5500-117">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="b5500-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b5500-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5500-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b5500-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5500-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b5500-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b5500-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b5500-121">Schema Name</span></span>  <br/> |<span data-ttu-id="b5500-122">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b5500-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="b5500-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b5500-123">Validation File</span></span>  <br/> |<span data-ttu-id="b5500-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b5500-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b5500-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b5500-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="b5500-126">Verdadero</span><span class="sxs-lookup"><span data-stu-id="b5500-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b5500-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="b5500-127">See also</span></span>

- [<span data-ttu-id="b5500-128">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="b5500-128">ApprovalRequestData</span></span>](approvalrequestdata.md)
- [<span data-ttu-id="b5500-129">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b5500-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

