---
title: IsUndecidedApprovalRequest
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 90841617-3b83-4124-8125-0293c9470f4a
description: El elemento IsUndecidedApprovalRequest especifica si un mensaje de solicitud de aprobación ha sido actúa en.
ms.openlocfilehash: 82b4624df5b2fe7ca212fdf76248e1ccfa3a081f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836127"
---
# <a name="isundecidedapprovalrequest"></a><span data-ttu-id="ffc29-103">IsUndecidedApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="ffc29-103">IsUndecidedApprovalRequest</span></span>

<span data-ttu-id="ffc29-104">El elemento **IsUndecidedApprovalRequest** especifica si un mensaje de solicitud de aprobación ha sido actúa en.</span><span class="sxs-lookup"><span data-stu-id="ffc29-104">The **IsUndecidedApprovalRequest** element specifies whether an approval request message has been acted on.</span></span> 
  
```XML
<IsUndecidedApprovalRequest> true | false </IsUndecidedApprovalRequest>
```

 <span data-ttu-id="ffc29-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ffc29-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ffc29-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ffc29-106">Attributes and elements</span></span>

<span data-ttu-id="ffc29-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ffc29-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ffc29-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ffc29-108">Attributes</span></span>

<span data-ttu-id="ffc29-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ffc29-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ffc29-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ffc29-110">Child elements</span></span>

<span data-ttu-id="ffc29-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ffc29-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ffc29-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ffc29-112">Parent elements</span></span>

[<span data-ttu-id="ffc29-113">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="ffc29-113">ApprovalRequestData</span></span>](approvalrequestdata.md)
  
## <a name="text-value"></a><span data-ttu-id="ffc29-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ffc29-114">Text value</span></span>

<span data-ttu-id="ffc29-115">El valor de texto del elemento **IsUndecidedApprovalRequest** es **true** si un mensaje de solicitud de aprobación no ha sido actúa en.</span><span class="sxs-lookup"><span data-stu-id="ffc29-115">The text value of the **IsUndecidedApprovalRequest** element is **true** if an approval request message has not been acted on.</span></span> <span data-ttu-id="ffc29-116">Un valor de **false** indica que se haya decidido la solicitud de aprobación.</span><span class="sxs-lookup"><span data-stu-id="ffc29-116">A value of **false** indicates that the approval request has been decided.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ffc29-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ffc29-117">Remarks</span></span>

<span data-ttu-id="ffc29-118">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ffc29-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="ffc29-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ffc29-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ffc29-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ffc29-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ffc29-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ffc29-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ffc29-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ffc29-122">Schema Name</span></span>  <br/> |<span data-ttu-id="ffc29-123">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ffc29-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="ffc29-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ffc29-124">Validation File</span></span>  <br/> |<span data-ttu-id="ffc29-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ffc29-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ffc29-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ffc29-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="ffc29-127">Verdadero</span><span class="sxs-lookup"><span data-stu-id="ffc29-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ffc29-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffc29-128">See also</span></span>



[<span data-ttu-id="ffc29-129">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="ffc29-129">ApprovalRequestData</span></span>](approvalrequestdata.md)


- [<span data-ttu-id="ffc29-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ffc29-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

