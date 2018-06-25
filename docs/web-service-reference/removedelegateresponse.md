---
title: RemoveDelegateResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveDelegateResponse
api_type:
- schema
ms.assetid: eef56c53-d0a7-4342-9ce6-4dbb6b1a1369
description: El elemento RemoveDelegateResponse contiene el estado y el resultado de una solicitud de operación RemoveDelegate.
ms.openlocfilehash: 45d0bcfaeb4d453f50cce8449f5cb7fdb70512a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837092"
---
# <a name="removedelegateresponse"></a><span data-ttu-id="0ec1e-103">RemoveDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="0ec1e-103">RemoveDelegateResponse</span></span>

<span data-ttu-id="0ec1e-104">El elemento **RemoveDelegateResponse** contiene el estado y el resultado de una solicitud de [operación RemoveDelegate](removedelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="0ec1e-104">The **RemoveDelegateResponse** element contains the status and result of a [RemoveDelegate operation](removedelegate-operation.md) request.</span></span> 
  
```xml
<RemoveDelegateResponse>
   <ResponseMessages/>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</RemoveDelegateResponse>
```

 <span data-ttu-id="0ec1e-105">**RemoveDelegateResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="0ec1e-105">**RemoveDelegateResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0ec1e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0ec1e-106">Attributes and elements</span></span>

<span data-ttu-id="0ec1e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0ec1e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0ec1e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0ec1e-108">Attributes</span></span>

<span data-ttu-id="0ec1e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0ec1e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0ec1e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0ec1e-110">Child elements</span></span>

|<span data-ttu-id="0ec1e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0ec1e-111">**Element**</span></span>|<span data-ttu-id="0ec1e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0ec1e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0ec1e-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="0ec1e-113">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>](responsemessages-arrayofdelegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="0ec1e-114">Contiene los mensajes de respuesta para una solicitud de administración de servicios Web de Exchange delegado.</span><span class="sxs-lookup"><span data-stu-id="0ec1e-114">Contains the response messages for an Exchange Web Services delegate management request.</span></span>  <br/> |
|[<span data-ttu-id="0ec1e-115">MessageText</span><span class="sxs-lookup"><span data-stu-id="0ec1e-115">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="0ec1e-116">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0ec1e-116">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="0ec1e-117">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="0ec1e-117">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="0ec1e-118">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0ec1e-118">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="0ec1e-119">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="0ec1e-119">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="0ec1e-120">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0ec1e-120">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="0ec1e-121">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="0ec1e-121">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="0ec1e-122">MessageXml</span><span class="sxs-lookup"><span data-stu-id="0ec1e-122">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="0ec1e-123">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="0ec1e-123">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0ec1e-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0ec1e-124">Parent elements</span></span>

<span data-ttu-id="0ec1e-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0ec1e-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0ec1e-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0ec1e-126">Remarks</span></span>

<span data-ttu-id="0ec1e-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="0ec1e-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0ec1e-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0ec1e-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ec1e-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0ec1e-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0ec1e-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0ec1e-130">Schema Name</span></span>  <br/> |<span data-ttu-id="0ec1e-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0ec1e-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0ec1e-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0ec1e-132">Validation File</span></span>  <br/> |<span data-ttu-id="0ec1e-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0ec1e-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0ec1e-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0ec1e-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="0ec1e-135">False</span><span class="sxs-lookup"><span data-stu-id="0ec1e-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0ec1e-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ec1e-136">See also</span></span>



[<span data-ttu-id="0ec1e-137">Operación RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="0ec1e-137">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="0ec1e-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0ec1e-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

