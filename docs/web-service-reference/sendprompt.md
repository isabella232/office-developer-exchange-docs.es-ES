---
title: SendPrompt
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22cb5a30-75d9-49a8-9d98-255f2e8a722d
description: El elemento SendPrompt especifica el tipo de acción permitida para una opción de votación.
ms.openlocfilehash: 98ffc69cdc94c3f7b9c325bee0c1ebaeb407ee96
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462104"
---
# <a name="sendprompt"></a><span data-ttu-id="8ab70-103">SendPrompt</span><span class="sxs-lookup"><span data-stu-id="8ab70-103">SendPrompt</span></span>

<span data-ttu-id="8ab70-104">El elemento **SendPrompt** especifica el tipo de acción permitida para una opción de votación.</span><span class="sxs-lookup"><span data-stu-id="8ab70-104">The **SendPrompt** element specifies the type of action allowed for a voting option.</span></span> 
  
```XML
<SendPrompt> None | Send | VotingOption </SendPrompt>
```

 <span data-ttu-id="8ab70-105">**SendPromptType**</span><span class="sxs-lookup"><span data-stu-id="8ab70-105">**SendPromptType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8ab70-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8ab70-106">Attributes and elements</span></span>

<span data-ttu-id="8ab70-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8ab70-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8ab70-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8ab70-108">Attributes</span></span>

<span data-ttu-id="8ab70-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8ab70-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8ab70-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8ab70-110">Child elements</span></span>

<span data-ttu-id="8ab70-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8ab70-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8ab70-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8ab70-112">Parent elements</span></span>

[<span data-ttu-id="8ab70-113">VotingOptionData</span><span class="sxs-lookup"><span data-stu-id="8ab70-113">VotingOptionData</span></span>](votingoptiondata.md)
  
## <a name="text-value"></a><span data-ttu-id="8ab70-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8ab70-114">Text value</span></span>

<span data-ttu-id="8ab70-115">El valor de texto del elemento **SendPrompt** es una acción de la opción de voto.</span><span class="sxs-lookup"><span data-stu-id="8ab70-115">The text value of the **SendPrompt** element is a voting option action.</span></span> <span data-ttu-id="8ab70-116">En la siguiente tabla se enumeran los valores posibles para este elemento.</span><span class="sxs-lookup"><span data-stu-id="8ab70-116">The following table lists the possible values for this element.</span></span> 
  
****

|<span data-ttu-id="8ab70-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8ab70-117">**Value**</span></span>|<span data-ttu-id="8ab70-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8ab70-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8ab70-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8ab70-119">None</span></span>  <br/> |<span data-ttu-id="8ab70-120">Ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="8ab70-120">No action.</span></span>  <br/> |
|<span data-ttu-id="8ab70-121">Enviar</span><span class="sxs-lookup"><span data-stu-id="8ab70-121">Send</span></span>  <br/> |<span data-ttu-id="8ab70-122">La respuesta se envía inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8ab70-122">The response is sent immediately.</span></span>  <br/> |
|<span data-ttu-id="8ab70-123">VotingOption</span><span class="sxs-lookup"><span data-stu-id="8ab70-123">VotingOption</span></span>  <br/> |<span data-ttu-id="8ab70-124">El aprobador puede escribir comentarios al aprobarlos o rechazarlos.</span><span class="sxs-lookup"><span data-stu-id="8ab70-124">The approver can enter comments while approving or rejecting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ab70-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8ab70-125">Remarks</span></span>

<span data-ttu-id="8ab70-126">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="8ab70-126">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="8ab70-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="8ab70-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8ab70-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8ab70-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ab70-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="8ab70-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8ab70-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8ab70-130">Schema Name</span></span>  <br/> |<span data-ttu-id="8ab70-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8ab70-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="8ab70-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8ab70-132">Validation File</span></span>  <br/> |<span data-ttu-id="8ab70-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="8ab70-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8ab70-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8ab70-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="8ab70-135">Verdadero</span><span class="sxs-lookup"><span data-stu-id="8ab70-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8ab70-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ab70-136">See also</span></span>



[<span data-ttu-id="8ab70-137">VotingOptionData</span><span class="sxs-lookup"><span data-stu-id="8ab70-137">VotingOptionData</span></span>](votingoptiondata.md)


- [<span data-ttu-id="8ab70-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8ab70-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

