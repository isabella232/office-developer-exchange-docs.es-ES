---
title: SendPrompt
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22cb5a30-75d9-49a8-9d98-255f2e8a722d
description: El elemento SendPrompt especifica el tipo de acción permitida para una opción de voto.
ms.openlocfilehash: f3220d957482ea04c46b014cdf1c67025d5ec21a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837346"
---
# <a name="sendprompt"></a><span data-ttu-id="fe14c-103">SendPrompt</span><span class="sxs-lookup"><span data-stu-id="fe14c-103">SendPrompt</span></span>

<span data-ttu-id="fe14c-104">El elemento **SendPrompt** especifica el tipo de acción permitida para una opción de voto.</span><span class="sxs-lookup"><span data-stu-id="fe14c-104">The **SendPrompt** element specifies the type of action allowed for a voting option.</span></span> 
  
```XML
<SendPrompt> None | Send | VotingOption </SendPrompt>
```

 <span data-ttu-id="fe14c-105">**SendPromptType**</span><span class="sxs-lookup"><span data-stu-id="fe14c-105">**SendPromptType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fe14c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fe14c-106">Attributes and elements</span></span>

<span data-ttu-id="fe14c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fe14c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fe14c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fe14c-108">Attributes</span></span>

<span data-ttu-id="fe14c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fe14c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fe14c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fe14c-110">Child elements</span></span>

<span data-ttu-id="fe14c-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fe14c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fe14c-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fe14c-112">Parent elements</span></span>

[<span data-ttu-id="fe14c-113">VotingOptionData</span><span class="sxs-lookup"><span data-stu-id="fe14c-113">VotingOptionData</span></span>](votingoptiondata.md)
  
## <a name="text-value"></a><span data-ttu-id="fe14c-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fe14c-114">Text value</span></span>

<span data-ttu-id="fe14c-115">El valor de texto del elemento **SendPrompt** es una acción de opción votación.</span><span class="sxs-lookup"><span data-stu-id="fe14c-115">The text value of the **SendPrompt** element is a voting option action.</span></span> <span data-ttu-id="fe14c-116">En la siguiente tabla se enumera los valores posibles para este elemento.</span><span class="sxs-lookup"><span data-stu-id="fe14c-116">The following table lists the possible values for this element.</span></span> 
  
****

|<span data-ttu-id="fe14c-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fe14c-117">**Value**</span></span>|<span data-ttu-id="fe14c-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fe14c-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe14c-119">None</span><span class="sxs-lookup"><span data-stu-id="fe14c-119">None</span></span>  <br/> |<span data-ttu-id="fe14c-120">Ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="fe14c-120">No action.</span></span>  <br/> |
|<span data-ttu-id="fe14c-121">Envío</span><span class="sxs-lookup"><span data-stu-id="fe14c-121">Send</span></span>  <br/> |<span data-ttu-id="fe14c-122">La respuesta se envía inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="fe14c-122">The response is sent immediately.</span></span>  <br/> |
|<span data-ttu-id="fe14c-123">VotingOption</span><span class="sxs-lookup"><span data-stu-id="fe14c-123">VotingOption</span></span>  <br/> |<span data-ttu-id="fe14c-124">El aprobador puede escribir comentarios durante la aprobación o rechazo.</span><span class="sxs-lookup"><span data-stu-id="fe14c-124">The approver can enter comments while approving or rejecting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe14c-125">Notas</span><span class="sxs-lookup"><span data-stu-id="fe14c-125">Remarks</span></span>

<span data-ttu-id="fe14c-126">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="fe14c-126">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="fe14c-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fe14c-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fe14c-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fe14c-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe14c-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fe14c-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fe14c-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fe14c-130">Schema Name</span></span>  <br/> |<span data-ttu-id="fe14c-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fe14c-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="fe14c-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fe14c-132">Validation File</span></span>  <br/> |<span data-ttu-id="fe14c-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fe14c-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fe14c-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fe14c-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="fe14c-135">Verdadero</span><span class="sxs-lookup"><span data-stu-id="fe14c-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fe14c-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="fe14c-136">See also</span></span>



[<span data-ttu-id="fe14c-137">VotingOptionData</span><span class="sxs-lookup"><span data-stu-id="fe14c-137">VotingOptionData</span></span>](votingoptiondata.md)


- [<span data-ttu-id="fe14c-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="fe14c-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

