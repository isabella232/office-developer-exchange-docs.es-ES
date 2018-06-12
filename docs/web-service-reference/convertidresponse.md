---
title: ConvertIdResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertIdResponse
api_type:
- schema
ms.assetid: ac1f044f-04a4-42ef-b762-cac5cd37894d
description: El elemento ConvertIdResponse contiene una respuesta a una solicitud de ConvertId. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 80299afebcebf15546b0fdbe14f0b08960527a47
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763886"
---
# <a name="convertidresponse"></a><span data-ttu-id="dc625-104">ConvertIdResponse</span><span class="sxs-lookup"><span data-stu-id="dc625-104">ConvertIdResponse</span></span>

<span data-ttu-id="dc625-105">El elemento **ConvertIdResponse** contiene una respuesta a una solicitud de ConvertId.</span><span class="sxs-lookup"><span data-stu-id="dc625-105">The **ConvertIdResponse** element contains a response to a ConvertId request.</span></span> <span data-ttu-id="dc625-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="dc625-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ConvertIdResponse>
   <ResponseMessages/>
</ConvertIdResponse>
```

 <span data-ttu-id="dc625-107">**ConvertIdResponseType**</span><span class="sxs-lookup"><span data-stu-id="dc625-107">**ConvertIdResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc625-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dc625-108">Attributes and elements</span></span>

<span data-ttu-id="dc625-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dc625-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc625-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="dc625-110">Attributes</span></span>

<span data-ttu-id="dc625-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dc625-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc625-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dc625-112">Child elements</span></span>

|<span data-ttu-id="dc625-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="dc625-113">**Element**</span></span>|<span data-ttu-id="dc625-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dc625-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc625-115">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="dc625-115">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="dc625-116">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="dc625-116">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dc625-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dc625-117">Parent elements</span></span>

<span data-ttu-id="dc625-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dc625-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc625-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc625-119">Remarks</span></span>

<span data-ttu-id="dc625-120">Los mensajes de respuesta que están contenidos en el elemento [ResponseMessages](responsemessages.md) serán instancias de ConvertIdResponseMessageType.</span><span class="sxs-lookup"><span data-stu-id="dc625-120">The response messages that are contained within the [ResponseMessages](responsemessages.md) element will be instances of ConvertIdResponseMessageType.</span></span> 
  
<span data-ttu-id="dc625-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="dc625-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc625-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dc625-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc625-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dc625-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dc625-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dc625-124">Schema Name</span></span>  <br/> |<span data-ttu-id="dc625-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="dc625-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dc625-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dc625-126">Validation File</span></span>  <br/> |<span data-ttu-id="dc625-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dc625-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dc625-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dc625-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="dc625-129">False</span><span class="sxs-lookup"><span data-stu-id="dc625-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc625-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="dc625-130">See also</span></span>



[<span data-ttu-id="dc625-131">Operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="dc625-131">ConvertId operation</span></span>](convertid-operation.md)


- [<span data-ttu-id="dc625-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="dc625-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="dc625-133">Convertir identificadores</span><span class="sxs-lookup"><span data-stu-id="dc625-133">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

