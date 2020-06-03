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
description: El elemento FreeBusyResponse contiene la información de disponibilidad de un único usuario de buzón de correo.
ms.openlocfilehash: 45a3e12756f3cbf29b76b442f7103abc5fb9a833
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461929"
---
# <a name="freebusyresponse"></a><span data-ttu-id="a5640-103">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="a5640-103">FreeBusyResponse</span></span>

<span data-ttu-id="a5640-104">El elemento **FreeBusyResponse** contiene la información de disponibilidad de un único usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a5640-104">The **FreeBusyResponse** element contains the free/busy information for a single mailbox user.</span></span> 
  
[<span data-ttu-id="a5640-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="a5640-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="a5640-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="a5640-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="a5640-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="a5640-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
```xml
<FreeBusyResponse>
   <ResponseMessage>...</ResponseMessage>
   <FreeBusyView>...</FreeBusyView>
</FreeBusyResponse>
```

 <span data-ttu-id="a5640-108">**FreeBusyResponseType**</span><span class="sxs-lookup"><span data-stu-id="a5640-108">**FreeBusyResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a5640-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a5640-109">Attributes and elements</span></span>

<span data-ttu-id="a5640-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a5640-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a5640-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="a5640-111">Attributes</span></span>

<span data-ttu-id="a5640-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a5640-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a5640-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a5640-113">Child elements</span></span>

|<span data-ttu-id="a5640-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a5640-114">**Element**</span></span>|<span data-ttu-id="a5640-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a5640-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a5640-116">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a5640-116">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="a5640-117">Proporciona información descriptiva sobre el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5640-117">Provides descriptive information about the response status.</span></span>  <br/> |
|[<span data-ttu-id="a5640-118">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="a5640-118">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="a5640-119">Contiene la información de disponibilidad de un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="a5640-119">Contains availability information for a specific user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a5640-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a5640-120">Parent elements</span></span>

|<span data-ttu-id="a5640-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a5640-121">**Element**</span></span>|<span data-ttu-id="a5640-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a5640-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a5640-123">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="a5640-123">FreeBusyResponseArray</span></span>](freebusyresponsearray.md) <br/> |<span data-ttu-id="a5640-124">Contiene la información de disponibilidad de los usuarios solicitados y el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5640-124">Contains the requested users' availability information and the response status.</span></span>  <br/> <span data-ttu-id="a5640-125">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="a5640-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5640-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5640-126">Remarks</span></span>

<span data-ttu-id="a5640-127">Este elemento no se incluye en una respuesta GetUserAvailability si no se solicita información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="a5640-127">This element is not included in a GetUserAvailability response if free/busy information is not requested.</span></span>
  
<span data-ttu-id="a5640-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="a5640-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a5640-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a5640-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a5640-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="a5640-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a5640-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a5640-131">Schema Name</span></span>  <br/> |<span data-ttu-id="a5640-132">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a5640-132">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a5640-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a5640-133">Validation File</span></span>  <br/> |<span data-ttu-id="a5640-134">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a5640-134">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a5640-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a5640-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="a5640-136">Falso</span><span class="sxs-lookup"><span data-stu-id="a5640-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a5640-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5640-137">See also</span></span>



[<span data-ttu-id="a5640-138">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="a5640-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="a5640-139">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="a5640-139">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="a5640-140">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="a5640-140">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

