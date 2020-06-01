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
description: El elemento FreeBusyResponseArray contiene la información de disponibilidad de los usuarios solicitados y el estado de respuesta.
ms.openlocfilehash: b45938c19b76a377fca125fb6a19f9d712718db6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457812"
---
# <a name="freebusyresponsearray"></a><span data-ttu-id="1a5e1-103">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="1a5e1-103">FreeBusyResponseArray</span></span>

<span data-ttu-id="1a5e1-104">El elemento **FreeBusyResponseArray** contiene la información de disponibilidad de los usuarios solicitados y el estado de respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a5e1-104">The **FreeBusyResponseArray** element contains the requested users' availability information and the response status.</span></span> 
  
[<span data-ttu-id="1a5e1-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1a5e1-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="1a5e1-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="1a5e1-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
```xml
<FreeBusyResponseArray>
   <FreeBusyResponse>...</FreeBusyResponse>
</FreeBusyResponseArray>
```

 <span data-ttu-id="1a5e1-107">**ArrayOfFreeBusyResponse**</span><span class="sxs-lookup"><span data-stu-id="1a5e1-107">**ArrayOfFreeBusyResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1a5e1-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1a5e1-108">Attributes and elements</span></span>

<span data-ttu-id="1a5e1-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1a5e1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1a5e1-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="1a5e1-110">Attributes</span></span>

<span data-ttu-id="1a5e1-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1a5e1-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1a5e1-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1a5e1-112">Child elements</span></span>

|<span data-ttu-id="1a5e1-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1a5e1-113">**Element**</span></span>|<span data-ttu-id="1a5e1-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1a5e1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1a5e1-115">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="1a5e1-115">FreeBusyResponse</span></span>](freebusyresponse.md) <br/> |<span data-ttu-id="1a5e1-116">Contiene la información de disponibilidad de un usuario de buzón de correo único y el estado de respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a5e1-116">Contains the free/busy information for a single mailbox user and the response status.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1a5e1-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1a5e1-117">Parent elements</span></span>

|<span data-ttu-id="1a5e1-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1a5e1-118">**Element**</span></span>|<span data-ttu-id="1a5e1-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1a5e1-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1a5e1-120">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1a5e1-120">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md) <br/> |<span data-ttu-id="1a5e1-121">Contiene las propiedades que definen la información de disponibilidad de usuario o la información de hora de reunión sugerida.</span><span class="sxs-lookup"><span data-stu-id="1a5e1-121">Contains the properties that define user availability information or suggested meeting time information.</span></span>  <br/> <span data-ttu-id="1a5e1-122">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="1a5e1-122">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a5e1-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1a5e1-123">Remarks</span></span>

<span data-ttu-id="1a5e1-124">Este elemento no se incluye en una respuesta GetUserAvailability si no se solicita información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="1a5e1-124">This element is not included in a GetUserAvailability response if free/busy information is not requested.</span></span>
  
<span data-ttu-id="1a5e1-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="1a5e1-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1a5e1-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1a5e1-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a5e1-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="1a5e1-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1a5e1-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1a5e1-128">Schema Name</span></span>  <br/> |<span data-ttu-id="1a5e1-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1a5e1-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1a5e1-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1a5e1-130">Validation File</span></span>  <br/> |<span data-ttu-id="1a5e1-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="1a5e1-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1a5e1-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1a5e1-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="1a5e1-133">Falso</span><span class="sxs-lookup"><span data-stu-id="1a5e1-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1a5e1-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a5e1-134">See also</span></span>



[<span data-ttu-id="1a5e1-135">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="1a5e1-135">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="1a5e1-136">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1a5e1-136">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="1a5e1-137">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="1a5e1-137">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

