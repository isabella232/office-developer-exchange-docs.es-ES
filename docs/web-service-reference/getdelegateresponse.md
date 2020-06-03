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
ms.openlocfilehash: 81c5033cd67b79baa131d71ea0b866c788ae5e82
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462027"
---
# <a name="getdelegateresponse"></a><span data-ttu-id="09008-103">GetDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="09008-103">GetDelegateResponse</span></span>

<span data-ttu-id="09008-104">El elemento **GetDelegateResponse** contiene el estado y el resultado de una solicitud de [operación GetDelegate](getdelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="09008-104">The **GetDelegateResponse** element contains the status and result of a [GetDelegate operation](getdelegate-operation.md) request.</span></span> 
  
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

 <span data-ttu-id="09008-105">**GetDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="09008-105">**GetDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="09008-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="09008-106">Attributes and elements</span></span>

<span data-ttu-id="09008-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="09008-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="09008-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="09008-108">Attributes</span></span>

<span data-ttu-id="09008-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="09008-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="09008-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="09008-110">Child elements</span></span>

|<span data-ttu-id="09008-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="09008-111">**Element**</span></span>|<span data-ttu-id="09008-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="09008-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="09008-113">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="09008-113">DeliverMeetingRequests</span></span>](delivermeetingrequests.md) <br/> |<span data-ttu-id="09008-114">Define cómo se administran las convocatorias de reunión entre el delegado y la entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="09008-114">Defines how meeting requests are handled between the delegate and the principal.</span></span>  <br/> |
|[<span data-ttu-id="09008-115">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="09008-115">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="09008-116">Contiene los mensajes de respuesta para una solicitud de administración de un delegado de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="09008-116">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="09008-117">MessageText</span><span class="sxs-lookup"><span data-stu-id="09008-117">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="09008-118">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="09008-118">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="09008-119">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="09008-119">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="09008-120">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="09008-120">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="09008-121">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="09008-121">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="09008-122">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="09008-122">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="09008-123">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="09008-123">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="09008-124">MessageXml</span><span class="sxs-lookup"><span data-stu-id="09008-124">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="09008-125">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="09008-125">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="09008-126">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="09008-126">Parent elements</span></span>

<span data-ttu-id="09008-127">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="09008-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="09008-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="09008-128">Remarks</span></span>

<span data-ttu-id="09008-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="09008-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="09008-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="09008-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09008-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="09008-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="09008-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="09008-132">Schema Name</span></span>  <br/> |<span data-ttu-id="09008-133">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="09008-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="09008-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="09008-134">Validation File</span></span>  <br/> |<span data-ttu-id="09008-135">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="09008-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="09008-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="09008-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="09008-137">Falso</span><span class="sxs-lookup"><span data-stu-id="09008-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09008-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="09008-138">See also</span></span>



[<span data-ttu-id="09008-139">Operación GetDelegate</span><span class="sxs-lookup"><span data-stu-id="09008-139">GetDelegate operation</span></span>](getdelegate-operation.md)


- [<span data-ttu-id="09008-140">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="09008-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

