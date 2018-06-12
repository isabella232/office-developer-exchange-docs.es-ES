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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836127"
---
# <a name="isundecidedapprovalrequest"></a><span data-ttu-id="9dca0-103">IsUndecidedApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="9dca0-103">IsUndecidedApprovalRequest</span></span>

<span data-ttu-id="9dca0-104">El elemento **IsUndecidedApprovalRequest** especifica si un mensaje de solicitud de aprobación ha sido actúa en.</span><span class="sxs-lookup"><span data-stu-id="9dca0-104">The **IsUndecidedApprovalRequest** element specifies whether an approval request message has been acted on.</span></span> 
  
```XML
<IsUndecidedApprovalRequest> true | false </IsUndecidedApprovalRequest>
```

 <span data-ttu-id="9dca0-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9dca0-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9dca0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9dca0-106">Attributes and elements</span></span>

<span data-ttu-id="9dca0-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9dca0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9dca0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9dca0-108">Attributes</span></span>

<span data-ttu-id="9dca0-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9dca0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9dca0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9dca0-110">Child elements</span></span>

<span data-ttu-id="9dca0-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9dca0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9dca0-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9dca0-112">Parent elements</span></span>

[<span data-ttu-id="9dca0-113">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="9dca0-113">ApprovalRequestData</span></span>](approvalrequestdata.md)
  
## <a name="text-value"></a><span data-ttu-id="9dca0-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9dca0-114">Text value</span></span>

<span data-ttu-id="9dca0-115">El valor de texto del elemento **IsUndecidedApprovalRequest** es **true** si un mensaje de solicitud de aprobación no ha sido actúa en.</span><span class="sxs-lookup"><span data-stu-id="9dca0-115">The text value of the **IsUndecidedApprovalRequest** element is **true** if an approval request message has not been acted on.</span></span> <span data-ttu-id="9dca0-116">Un valor de **false** indica que se haya decidido la solicitud de aprobación.</span><span class="sxs-lookup"><span data-stu-id="9dca0-116">A value of **false** indicates that the approval request has been decided.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9dca0-117">Notas</span><span class="sxs-lookup"><span data-stu-id="9dca0-117">Remarks</span></span>

<span data-ttu-id="9dca0-118">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="9dca0-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="9dca0-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="9dca0-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9dca0-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9dca0-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9dca0-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9dca0-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9dca0-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9dca0-122">Schema Name</span></span>  <br/> |<span data-ttu-id="9dca0-123">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9dca0-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="9dca0-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9dca0-124">Validation File</span></span>  <br/> |<span data-ttu-id="9dca0-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9dca0-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9dca0-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9dca0-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="9dca0-127">Verdadero</span><span class="sxs-lookup"><span data-stu-id="9dca0-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9dca0-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="9dca0-128">See also</span></span>



[<span data-ttu-id="9dca0-129">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="9dca0-129">ApprovalRequestData</span></span>](approvalrequestdata.md)


- [<span data-ttu-id="9dca0-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="9dca0-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

