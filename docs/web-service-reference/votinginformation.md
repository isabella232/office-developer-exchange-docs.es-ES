---
title: VotingInformation
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 351c8dfe-cf8c-45ba-a07d-d764f8189773
description: El elemento VotingInformation especifica información votación en un mensaje de votación y whereApproveandRejectare de mensaje de solicitud de aprobación de las opciones de voto.
ms.openlocfilehash: f11c25bb1f3a3c4781cfa6c51e11ff87af40c7f0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840966"
---
# <a name="votinginformation"></a><span data-ttu-id="acfac-103">VotingInformation</span><span class="sxs-lookup"><span data-stu-id="acfac-103">VotingInformation</span></span>

<span data-ttu-id="acfac-104">El elemento **VotingInformation** especifica información votación en un mensaje votación y el mensaje de solicitud de aprobación donde "Aprobar" y "Rechazar" es las opciones de voto.</span><span class="sxs-lookup"><span data-stu-id="acfac-104">The **VotingInformation** element specifies voting information on a voting message and approval request message where "Approve" and "Reject" are the voting options.</span></span> 
  
```XML
<VotingInformation
   <UserOptions/>
   <VotingResponse/>
</VotingInformation>
```

 <span data-ttu-id="acfac-105">**VotingInformationType**</span><span class="sxs-lookup"><span data-stu-id="acfac-105">**VotingInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="acfac-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="acfac-106">Attributes and elements</span></span>

<span data-ttu-id="acfac-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="acfac-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="acfac-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="acfac-108">Attributes</span></span>

<span data-ttu-id="acfac-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="acfac-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="acfac-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="acfac-110">Child elements</span></span>

<span data-ttu-id="acfac-111">[UserOptions](useroptions.md) | [VotingResponse](votingresponse.md)</span><span class="sxs-lookup"><span data-stu-id="acfac-111">[UserOptions](useroptions.md) | [VotingResponse](votingresponse.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="acfac-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="acfac-112">Parent elements</span></span>

[<span data-ttu-id="acfac-113">Message</span><span class="sxs-lookup"><span data-stu-id="acfac-113">Message</span></span>](message-ex15websvcsotherref.md)
  
## <a name="remarks"></a><span data-ttu-id="acfac-114">Notas</span><span class="sxs-lookup"><span data-stu-id="acfac-114">Remarks</span></span>

<span data-ttu-id="acfac-115">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="acfac-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="acfac-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="acfac-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="acfac-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="acfac-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="acfac-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="acfac-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="acfac-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="acfac-119">Schema Name</span></span>  <br/> |<span data-ttu-id="acfac-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="acfac-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="acfac-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="acfac-121">Validation File</span></span>  <br/> |<span data-ttu-id="acfac-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="acfac-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="acfac-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="acfac-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="acfac-124">Verdadero</span><span class="sxs-lookup"><span data-stu-id="acfac-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="acfac-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="acfac-125">See also</span></span>



[<span data-ttu-id="acfac-126">Message</span><span class="sxs-lookup"><span data-stu-id="acfac-126">Message</span></span>](message-ex15websvcsotherref.md)


- [<span data-ttu-id="acfac-127">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="acfac-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

