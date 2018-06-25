---
title: ResponseMessages (ArrayOfDelegateUserResponseMessageType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseMessages
api_type:
- schema
ms.assetid: 14819975-ce54-4f0e-9f90-d4b275895ea0
description: El elemento ResponseMessages contiene los mensajes de respuesta para una solicitud de administración de servicios Web de Exchange delegado.
ms.openlocfilehash: e4b5567f3ded003e9648eb8ebebfadf8f1748d6c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837193"
---
# <a name="responsemessages-arrayofdelegateuserresponsemessagetype"></a><span data-ttu-id="75541-103">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="75541-103">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>

<span data-ttu-id="75541-104">El elemento **ResponseMessages** contiene los mensajes de respuesta para una solicitud de administración de servicios Web de Exchange delegado.</span><span class="sxs-lookup"><span data-stu-id="75541-104">The **ResponseMessages** element contains the response messages for an Exchange Web Services delegate management request.</span></span> 
  
```
<ResponseMessages>
   <DelegateUserResponseMessageType/>
</ResponseMessages>
```

 <span data-ttu-id="75541-105">**ArrayOfDelegateUserResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="75541-105">**ArrayOfDelegateUserResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="75541-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="75541-106">Attributes and elements</span></span>

<span data-ttu-id="75541-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="75541-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="75541-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="75541-108">Attributes</span></span>

<span data-ttu-id="75541-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="75541-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="75541-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="75541-110">Child elements</span></span>

|<span data-ttu-id="75541-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="75541-111">**Element**</span></span>|<span data-ttu-id="75541-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="75541-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="75541-113">DelegateUserResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="75541-113">DelegateUserResponseMessageType</span></span>](delegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="75541-114">Contiene los mensajes de respuesta para las operaciones de administración de delegado.</span><span class="sxs-lookup"><span data-stu-id="75541-114">Contains response messages for delegate management operations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="75541-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="75541-115">Parent elements</span></span>

|<span data-ttu-id="75541-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="75541-116">**Element**</span></span>|<span data-ttu-id="75541-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="75541-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="75541-118">AddDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="75541-118">AddDelegateResponse</span></span>](adddelegateresponse.md) <br/> |<span data-ttu-id="75541-119">Contiene el estado y el resultado de una solicitud de [operación AddDelegate](adddelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="75541-119">Contains the status and result of an [AddDelegate operation](adddelegate-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="75541-120">GetDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="75541-120">GetDelegateResponse</span></span>](getdelegateresponse.md) <br/> |<span data-ttu-id="75541-121">Contiene el estado y el resultado de una solicitud de [operación GetDelegate](getdelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="75541-121">Contains the status and result of a [GetDelegate operation](getdelegate-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="75541-122">UpdateDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="75541-122">UpdateDelegateResponse</span></span>](updatedelegateresponse.md) <br/> |<span data-ttu-id="75541-123">Contiene el estado y el resultado de una solicitud de [operación UpdateDelegate](updatedelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="75541-123">Contains the status and result of an [UpdateDelegate operation](updatedelegate-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="75541-124">RemoveDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="75541-124">RemoveDelegateResponse</span></span>](removedelegateresponse.md) <br/> |<span data-ttu-id="75541-125">Contiene el estado y el resultado de una solicitud de [operación RemoveDelegate](removedelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="75541-125">Contains the status and result of a [RemoveDelegate operation](removedelegate-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75541-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="75541-126">Remarks</span></span>

<span data-ttu-id="75541-127">Este elemento se usa en la [operación AddDelegate](adddelegate-operation.md), la [operación de GetDelegate](getdelegate-operation.md), la [operación de UpdateDelegate](updatedelegate-operation.md)y la [operación de RemoveDelegate](removedelegate-operation.md).</span><span class="sxs-lookup"><span data-stu-id="75541-127">This element is used in the [AddDelegate operation](adddelegate-operation.md), the [GetDelegate operation](getdelegate-operation.md), the [UpdateDelegate operation](updatedelegate-operation.md), and the [RemoveDelegate operation](removedelegate-operation.md).</span></span> <span data-ttu-id="75541-128">Las respuestas de operación de administración de delegado tienen una estructura diferente de otras respuestas.</span><span class="sxs-lookup"><span data-stu-id="75541-128">The delegate management operation responses are structured differently than other responses.</span></span> <span data-ttu-id="75541-129">Los mensajes de respuesta de la administración de delegado tienen establecimiento inflexible de tipos.</span><span class="sxs-lookup"><span data-stu-id="75541-129">The delegate management response messages are strongly typed.</span></span>
  
<span data-ttu-id="75541-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con la función de servidor de acceso de cliente instalada.</span><span class="sxs-lookup"><span data-stu-id="75541-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="75541-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="75541-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75541-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="75541-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="75541-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="75541-133">Schema Name</span></span>  <br/> |<span data-ttu-id="75541-134">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="75541-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="75541-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="75541-135">Validation File</span></span>  <br/> |<span data-ttu-id="75541-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="75541-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="75541-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="75541-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="75541-138">False</span><span class="sxs-lookup"><span data-stu-id="75541-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="75541-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="75541-139">See also</span></span>



[<span data-ttu-id="75541-140">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="75541-140">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="75541-141">Operación GetDelegate</span><span class="sxs-lookup"><span data-stu-id="75541-141">GetDelegate operation</span></span>](getdelegate-operation.md)
  
[<span data-ttu-id="75541-142">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="75541-142">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
  
[<span data-ttu-id="75541-143">Operación RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="75541-143">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="75541-144">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="75541-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

