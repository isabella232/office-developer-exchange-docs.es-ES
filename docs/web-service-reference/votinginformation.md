---
title: VotingInformation
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 351c8dfe-cf8c-45ba-a07d-d764f8189773
description: El elemento VotingInformation especifica la información de voto en un mensaje de voto y un mensaje de solicitud de aprobación whereApproveandRejectare las opciones de votación.
ms.openlocfilehash: d946ba8c71d19c8cbb1befbe8c4e43e93590ccae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467749"
---
# <a name="votinginformation"></a><span data-ttu-id="cebda-103">VotingInformation</span><span class="sxs-lookup"><span data-stu-id="cebda-103">VotingInformation</span></span>

<span data-ttu-id="cebda-104">El elemento **VotingInformation** especifica la información de votación en un mensaje de votación y un mensaje de solicitud de aprobación donde "aprobar" y "rechazar" son las opciones de votación.</span><span class="sxs-lookup"><span data-stu-id="cebda-104">The **VotingInformation** element specifies voting information on a voting message and approval request message where "Approve" and "Reject" are the voting options.</span></span> 
  
```XML
<VotingInformation
   <UserOptions/>
   <VotingResponse/>
</VotingInformation>
```

 <span data-ttu-id="cebda-105">**VotingInformationType**</span><span class="sxs-lookup"><span data-stu-id="cebda-105">**VotingInformationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cebda-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cebda-106">Attributes and elements</span></span>

<span data-ttu-id="cebda-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cebda-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cebda-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cebda-108">Attributes</span></span>

<span data-ttu-id="cebda-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cebda-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cebda-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cebda-110">Child elements</span></span>

<span data-ttu-id="cebda-111">[UserOptions](useroptions.md)  |  [VotingResponse](votingresponse.md)</span><span class="sxs-lookup"><span data-stu-id="cebda-111">[UserOptions](useroptions.md) | [VotingResponse](votingresponse.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cebda-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cebda-112">Parent elements</span></span>

[<span data-ttu-id="cebda-113">Message</span><span class="sxs-lookup"><span data-stu-id="cebda-113">Message</span></span>](message-ex15websvcsotherref.md)
  
## <a name="remarks"></a><span data-ttu-id="cebda-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cebda-114">Remarks</span></span>

<span data-ttu-id="cebda-115">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="cebda-115">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="cebda-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="cebda-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cebda-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cebda-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cebda-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="cebda-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cebda-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cebda-119">Schema Name</span></span>  <br/> |<span data-ttu-id="cebda-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="cebda-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="cebda-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cebda-121">Validation File</span></span>  <br/> |<span data-ttu-id="cebda-122">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="cebda-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cebda-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cebda-123">Can be Empty</span></span>  <br/> |<span data-ttu-id="cebda-124">Verdadero</span><span class="sxs-lookup"><span data-stu-id="cebda-124">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cebda-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="cebda-125">See also</span></span>



[<span data-ttu-id="cebda-126">Message</span><span class="sxs-lookup"><span data-stu-id="cebda-126">Message</span></span>](message-ex15websvcsotherref.md)


- [<span data-ttu-id="cebda-127">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cebda-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

