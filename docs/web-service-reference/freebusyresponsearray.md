---
title: FreeBusyResponseArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyResponseArray
api_type:
- schema
ms.assetid: 5592a37e-cf4b-4643-8a2a-fa58c40345b9
description: El elemento FreeBusyResponseArray contiene información sobre la disponibilidad de los usuarios solicitado y el estado de la respuesta.
ms.openlocfilehash: cc6022c28213667c40dc00b5627ed88c4f78e2f2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764716"
---
# <a name="freebusyresponsearray"></a><span data-ttu-id="c7516-103">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="c7516-103">FreeBusyResponseArray</span></span>

<span data-ttu-id="c7516-104">El elemento **FreeBusyResponseArray** contiene información sobre la disponibilidad de los usuarios solicitado y el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7516-104">The **FreeBusyResponseArray** element contains the requested users' availability information and the response status.</span></span> 
  
[<span data-ttu-id="c7516-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="c7516-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="c7516-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="c7516-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
```xml
<FreeBusyResponseArray>
   <FreeBusyResponse>...</FreeBusyResponse>
</FreeBusyResponseArray>
```

 <span data-ttu-id="c7516-107">**ArrayOfFreeBusyResponse**</span><span class="sxs-lookup"><span data-stu-id="c7516-107">**ArrayOfFreeBusyResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c7516-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c7516-108">Attributes and elements</span></span>

<span data-ttu-id="c7516-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c7516-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7516-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="c7516-110">Attributes</span></span>

<span data-ttu-id="c7516-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c7516-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c7516-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c7516-112">Child elements</span></span>

|<span data-ttu-id="c7516-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="c7516-113">**Element**</span></span>|<span data-ttu-id="c7516-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7516-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7516-115">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="c7516-115">FreeBusyResponse</span></span>](freebusyresponse.md) <br/> |<span data-ttu-id="c7516-116">Contiene la información de disponibilidad para un usuario de buzón único y el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7516-116">Contains the free/busy information for a single mailbox user and the response status.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c7516-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c7516-117">Parent elements</span></span>

|<span data-ttu-id="c7516-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="c7516-118">**Element**</span></span>|<span data-ttu-id="c7516-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c7516-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7516-120">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="c7516-120">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md) <br/> |<span data-ttu-id="c7516-121">Contiene las propiedades que definen la información de disponibilidad del usuario o sugeridas información de tiempo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="c7516-121">Contains the properties that define user availability information or suggested meeting time information.</span></span>  <br/> <span data-ttu-id="c7516-122">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="c7516-122">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7516-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c7516-123">Remarks</span></span>

<span data-ttu-id="c7516-124">Este elemento no está incluido en una respuesta de GetUserAvailability si no se solicita información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="c7516-124">This element is not included in a GetUserAvailability response if free/busy information is not requested.</span></span>
  
<span data-ttu-id="c7516-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="c7516-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c7516-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c7516-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7516-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c7516-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c7516-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c7516-128">Schema Name</span></span>  <br/> |<span data-ttu-id="c7516-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c7516-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c7516-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c7516-130">Validation File</span></span>  <br/> |<span data-ttu-id="c7516-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c7516-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c7516-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c7516-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="c7516-133">False</span><span class="sxs-lookup"><span data-stu-id="c7516-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7516-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7516-134">See also</span></span>



[<span data-ttu-id="c7516-135">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="c7516-135">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="c7516-136">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="c7516-136">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="c7516-137">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="c7516-137">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

