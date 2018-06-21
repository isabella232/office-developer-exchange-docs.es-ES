---
title: SendItemResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendItemResponse
api_type:
- schema
ms.assetid: 26ac41c7-57d9-473e-ab7a-bae93e1d2aba
description: El elemento SendItemResponse define una respuesta a una solicitud de SendItem.
ms.openlocfilehash: 41f450e1d4c95f7ba389adcaa2ed7e18ea74d61c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2018
ms.locfileid: "19837339"
---
# <a name="senditemresponse"></a><span data-ttu-id="3bcbd-103">SendItemResponse</span><span class="sxs-lookup"><span data-stu-id="3bcbd-103">SendItemResponse</span></span>

<span data-ttu-id="3bcbd-104">El elemento **SendItemResponse** define una respuesta a una solicitud de SendItem.</span><span class="sxs-lookup"><span data-stu-id="3bcbd-104">The **SendItemResponse** element defines a response to a SendItem request.</span></span> 
  
```xml
<SendItemResponse>
   <ResponseMessages/>
</SendItemResponse>
```

 <span data-ttu-id="3bcbd-105">**SendItemResponseType**</span><span class="sxs-lookup"><span data-stu-id="3bcbd-105">**SendItemResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3bcbd-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3bcbd-106">Attributes and elements</span></span>

<span data-ttu-id="3bcbd-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3bcbd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3bcbd-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3bcbd-108">Attributes</span></span>

<span data-ttu-id="3bcbd-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3bcbd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3bcbd-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3bcbd-110">Child elements</span></span>

|<span data-ttu-id="3bcbd-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3bcbd-111">**Element**</span></span>|<span data-ttu-id="3bcbd-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3bcbd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3bcbd-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3bcbd-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="3bcbd-114">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3bcbd-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3bcbd-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3bcbd-115">Parent elements</span></span>

<span data-ttu-id="3bcbd-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3bcbd-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3bcbd-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3bcbd-117">Remarks</span></span>

<span data-ttu-id="3bcbd-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3bcbd-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3bcbd-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3bcbd-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3bcbd-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3bcbd-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3bcbd-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3bcbd-121">Schema name</span></span>  <br/> |<span data-ttu-id="3bcbd-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3bcbd-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3bcbd-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3bcbd-123">Validation file</span></span>  <br/> |<span data-ttu-id="3bcbd-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3bcbd-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3bcbd-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3bcbd-125">Can be empty</span></span>  <br/> |<span data-ttu-id="3bcbd-126">False</span><span class="sxs-lookup"><span data-stu-id="3bcbd-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3bcbd-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3bcbd-127">See also</span></span>



[<span data-ttu-id="3bcbd-128">Operación SendItem</span><span class="sxs-lookup"><span data-stu-id="3bcbd-128">SendItem operation</span></span>](senditem-operation.md)
  
[<span data-ttu-id="3bcbd-129">SendItem</span><span class="sxs-lookup"><span data-stu-id="3bcbd-129">SendItem</span></span>](senditem.md)


- [<span data-ttu-id="3bcbd-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3bcbd-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

