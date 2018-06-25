---
title: GetDelegateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetDelegateResponse
api_type:
- schema
ms.assetid: 71a418a5-5652-40e1-8f84-fe4f7c9f86af
description: El elemento GetDelegateResponse contiene el estado y el resultado de una solicitud de operación GetDelegate.
ms.openlocfilehash: 52731ea66420c21cf3fb8d19082aef65551c2af2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764802"
---
# <a name="getdelegateresponse"></a><span data-ttu-id="4cad5-103">GetDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="4cad5-103">GetDelegateResponse</span></span>

<span data-ttu-id="4cad5-104">El elemento **GetDelegateResponse** contiene el estado y el resultado de una solicitud de [operación GetDelegate](getdelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="4cad5-104">The **GetDelegateResponse** element contains the status and result of a [GetDelegate operation](getdelegate-operation.md) request.</span></span> 
  
```xml
<GetDelegateResponse>
   <DeliverMeetingRequests/>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</GetDelegateResponse>
```

 <span data-ttu-id="4cad5-105">**GetDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="4cad5-105">**GetDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4cad5-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4cad5-106">Attributes and elements</span></span>

<span data-ttu-id="4cad5-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4cad5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4cad5-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4cad5-108">Attributes</span></span>

<span data-ttu-id="4cad5-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4cad5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4cad5-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4cad5-110">Child elements</span></span>

|<span data-ttu-id="4cad5-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4cad5-111">**Element**</span></span>|<span data-ttu-id="4cad5-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4cad5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4cad5-113">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="4cad5-113">DeliverMeetingRequests</span></span>](delivermeetingrequests.md) <br/> |<span data-ttu-id="4cad5-114">Define cómo se controlan las convocatorias de reunión entre el delegado y la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="4cad5-114">Defines how meeting requests are handled between the delegate and the principal.</span></span>  <br/> |
|[<span data-ttu-id="4cad5-115">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="4cad5-115">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="4cad5-116">Contiene los mensajes de respuesta para una solicitud de administración de servicios Web de Exchange delegado.</span><span class="sxs-lookup"><span data-stu-id="4cad5-116">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="4cad5-117">MessageText</span><span class="sxs-lookup"><span data-stu-id="4cad5-117">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="4cad5-118">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4cad5-118">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="4cad5-119">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4cad5-119">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="4cad5-120">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4cad5-120">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="4cad5-121">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="4cad5-121">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="4cad5-122">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="4cad5-122">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="4cad5-123">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="4cad5-123">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="4cad5-124">MessageXml</span><span class="sxs-lookup"><span data-stu-id="4cad5-124">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="4cad5-125">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="4cad5-125">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4cad5-126">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4cad5-126">Parent elements</span></span>

<span data-ttu-id="4cad5-127">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4cad5-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4cad5-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4cad5-128">Remarks</span></span>

<span data-ttu-id="4cad5-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4cad5-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4cad5-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4cad5-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4cad5-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4cad5-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4cad5-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4cad5-132">Schema Name</span></span>  <br/> |<span data-ttu-id="4cad5-133">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="4cad5-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4cad5-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4cad5-134">Validation File</span></span>  <br/> |<span data-ttu-id="4cad5-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4cad5-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4cad5-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4cad5-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="4cad5-137">False</span><span class="sxs-lookup"><span data-stu-id="4cad5-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4cad5-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cad5-138">See also</span></span>



[<span data-ttu-id="4cad5-139">Operación GetDelegate</span><span class="sxs-lookup"><span data-stu-id="4cad5-139">GetDelegate operation</span></span>](getdelegate-operation.md)


- [<span data-ttu-id="4cad5-140">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4cad5-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

