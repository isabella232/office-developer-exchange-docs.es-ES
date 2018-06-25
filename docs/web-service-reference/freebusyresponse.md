---
title: FreeBusyResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyResponse
api_type:
- schema
ms.assetid: 3038d106-9ac9-4ac7-bb43-96c783edbef5
description: El elemento FreeBusyResponse contiene la información de disponibilidad para un usuario de buzón único.
ms.openlocfilehash: 73e3972bb53d6bf59e5156098bad06bcde5f0155
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764713"
---
# <a name="freebusyresponse"></a><span data-ttu-id="ba546-103">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="ba546-103">FreeBusyResponse</span></span>

<span data-ttu-id="ba546-104">El elemento **FreeBusyResponse** contiene la información de disponibilidad para un usuario de buzón único.</span><span class="sxs-lookup"><span data-stu-id="ba546-104">The **FreeBusyResponse** element contains the free/busy information for a single mailbox user.</span></span> 
  
[<span data-ttu-id="ba546-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ba546-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="ba546-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="ba546-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="ba546-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="ba546-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
```xml
<FreeBusyResponse>
   <ResponseMessage>...</ResponseMessage>
   <FreeBusyView>...</FreeBusyView>
</FreeBusyResponse>
```

 <span data-ttu-id="ba546-108">**FreeBusyResponseType**</span><span class="sxs-lookup"><span data-stu-id="ba546-108">**FreeBusyResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba546-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ba546-109">Attributes and elements</span></span>

<span data-ttu-id="ba546-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ba546-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba546-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="ba546-111">Attributes</span></span>

<span data-ttu-id="ba546-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ba546-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba546-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ba546-113">Child elements</span></span>

|<span data-ttu-id="ba546-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba546-114">**Element**</span></span>|<span data-ttu-id="ba546-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ba546-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba546-116">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ba546-116">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="ba546-117">Proporciona información descriptiva sobre el estado de respuesta.</span><span class="sxs-lookup"><span data-stu-id="ba546-117">Provides descriptive information about the response status.</span></span>  <br/> |
|[<span data-ttu-id="ba546-118">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="ba546-118">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="ba546-119">Contiene la información de disponibilidad para un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="ba546-119">Contains availability information for a specific user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ba546-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ba546-120">Parent elements</span></span>

|<span data-ttu-id="ba546-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba546-121">**Element**</span></span>|<span data-ttu-id="ba546-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ba546-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba546-123">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="ba546-123">FreeBusyResponseArray</span></span>](freebusyresponsearray.md) <br/> |<span data-ttu-id="ba546-124">Contiene información sobre la disponibilidad de los usuarios solicitado y el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ba546-124">Contains the requested users' availability information and the response status.</span></span>  <br/> <span data-ttu-id="ba546-125">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="ba546-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba546-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ba546-126">Remarks</span></span>

<span data-ttu-id="ba546-127">Este elemento no está incluido en una respuesta de GetUserAvailability si no se solicita información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="ba546-127">This element is not included in a GetUserAvailability response if free/busy information is not requested.</span></span>
  
<span data-ttu-id="ba546-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="ba546-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba546-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ba546-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba546-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ba546-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ba546-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ba546-131">Schema Name</span></span>  <br/> |<span data-ttu-id="ba546-132">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ba546-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ba546-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ba546-133">Validation File</span></span>  <br/> |<span data-ttu-id="ba546-134">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ba546-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ba546-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ba546-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="ba546-136">False</span><span class="sxs-lookup"><span data-stu-id="ba546-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba546-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba546-137">See also</span></span>



[<span data-ttu-id="ba546-138">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="ba546-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="ba546-139">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ba546-139">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="ba546-140">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="ba546-140">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

