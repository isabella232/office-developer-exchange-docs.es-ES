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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462027"
---
# <a name="getdelegateresponse"></a><span data-ttu-id="b1777-103">GetDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="b1777-103">GetDelegateResponse</span></span>

<span data-ttu-id="b1777-104">El elemento **GetDelegateResponse** contiene el estado y el resultado de una solicitud de [operación GetDelegate](getdelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="b1777-104">The **GetDelegateResponse** element contains the status and result of a [GetDelegate operation](getdelegate-operation.md) request.</span></span> 
  
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

 <span data-ttu-id="b1777-105">**GetDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="b1777-105">**GetDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b1777-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b1777-106">Attributes and elements</span></span>

<span data-ttu-id="b1777-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b1777-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1777-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b1777-108">Attributes</span></span>

<span data-ttu-id="b1777-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b1777-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b1777-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b1777-110">Child elements</span></span>

|<span data-ttu-id="b1777-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b1777-111">**Element**</span></span>|<span data-ttu-id="b1777-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b1777-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1777-113">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="b1777-113">DeliverMeetingRequests</span></span>](delivermeetingrequests.md) <br/> |<span data-ttu-id="b1777-114">Define cómo se administran las convocatorias de reunión entre el delegado y la entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="b1777-114">Defines how meeting requests are handled between the delegate and the principal.</span></span>  <br/> |
|[<span data-ttu-id="b1777-115">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="b1777-115">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="b1777-116">Contiene los mensajes de respuesta para una solicitud de administración de un delegado de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b1777-116">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="b1777-117">MessageText</span><span class="sxs-lookup"><span data-stu-id="b1777-117">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="b1777-118">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b1777-118">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="b1777-119">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="b1777-119">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="b1777-120">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b1777-120">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="b1777-121">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="b1777-121">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="b1777-122">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b1777-122">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="b1777-123">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="b1777-123">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="b1777-124">MessageXml</span><span class="sxs-lookup"><span data-stu-id="b1777-124">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="b1777-125">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="b1777-125">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b1777-126">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b1777-126">Parent elements</span></span>

<span data-ttu-id="b1777-127">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b1777-127">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b1777-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b1777-128">Remarks</span></span>

<span data-ttu-id="b1777-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="b1777-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b1777-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b1777-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1777-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1777-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b1777-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b1777-132">Schema Name</span></span>  <br/> |<span data-ttu-id="b1777-133">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b1777-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b1777-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b1777-134">Validation File</span></span>  <br/> |<span data-ttu-id="b1777-135">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b1777-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b1777-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b1777-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="b1777-137">Falso</span><span class="sxs-lookup"><span data-stu-id="b1777-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b1777-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1777-138">See also</span></span>



[<span data-ttu-id="b1777-139">Operación GetDelegate</span><span class="sxs-lookup"><span data-stu-id="b1777-139">GetDelegate operation</span></span>](getdelegate-operation.md)


- [<span data-ttu-id="b1777-140">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b1777-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

