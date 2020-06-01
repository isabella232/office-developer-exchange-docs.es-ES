---
title: IsUndecidedApprovalRequest
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 90841617-3b83-4124-8125-0293c9470f4a
description: El elemento IsUndecidedApprovalRequest especifica si se ha actuado en un mensaje de solicitud de aprobación.
ms.openlocfilehash: 0949cf64b8583c4b3fa5a1700475f01cc480f69f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458176"
---
# <a name="isundecidedapprovalrequest"></a><span data-ttu-id="c7fde-103">IsUndecidedApprovalRequest</span><span class="sxs-lookup"><span data-stu-id="c7fde-103">IsUndecidedApprovalRequest</span></span>

<span data-ttu-id="c7fde-104">El elemento **IsUndecidedApprovalRequest** especifica si se ha actuado en un mensaje de solicitud de aprobación.</span><span class="sxs-lookup"><span data-stu-id="c7fde-104">The **IsUndecidedApprovalRequest** element specifies whether an approval request message has been acted on.</span></span> 
  
```XML
<IsUndecidedApprovalRequest> true | false </IsUndecidedApprovalRequest>
```

 <span data-ttu-id="c7fde-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c7fde-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c7fde-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c7fde-106">Attributes and elements</span></span>

<span data-ttu-id="c7fde-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c7fde-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7fde-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c7fde-108">Attributes</span></span>

<span data-ttu-id="c7fde-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c7fde-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c7fde-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c7fde-110">Child elements</span></span>

<span data-ttu-id="c7fde-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c7fde-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c7fde-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c7fde-112">Parent elements</span></span>

[<span data-ttu-id="c7fde-113">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="c7fde-113">ApprovalRequestData</span></span>](approvalrequestdata.md)
  
## <a name="text-value"></a><span data-ttu-id="c7fde-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c7fde-114">Text value</span></span>

<span data-ttu-id="c7fde-115">El valor de texto del elemento **IsUndecidedApprovalRequest** es **true** si no se ha actuado en un mensaje de solicitud de aprobación.</span><span class="sxs-lookup"><span data-stu-id="c7fde-115">The text value of the **IsUndecidedApprovalRequest** element is **true** if an approval request message has not been acted on.</span></span> <span data-ttu-id="c7fde-116">Un valor de **false** indica que se ha decidido la solicitud de aprobación.</span><span class="sxs-lookup"><span data-stu-id="c7fde-116">A value of **false** indicates that the approval request has been decided.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c7fde-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c7fde-117">Remarks</span></span>

<span data-ttu-id="c7fde-118">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c7fde-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="c7fde-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c7fde-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c7fde-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c7fde-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7fde-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="c7fde-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c7fde-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c7fde-122">Schema Name</span></span>  <br/> |<span data-ttu-id="c7fde-123">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c7fde-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="c7fde-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c7fde-124">Validation File</span></span>  <br/> |<span data-ttu-id="c7fde-125">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c7fde-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c7fde-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c7fde-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="c7fde-127">Verdadero</span><span class="sxs-lookup"><span data-stu-id="c7fde-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7fde-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7fde-128">See also</span></span>



[<span data-ttu-id="c7fde-129">ApprovalRequestData</span><span class="sxs-lookup"><span data-stu-id="c7fde-129">ApprovalRequestData</span></span>](approvalrequestdata.md)


- [<span data-ttu-id="c7fde-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c7fde-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

