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
description: El elemento ResponseMessages contiene los mensajes de respuesta para una solicitud de administración de delegado de servicios Web de Exchange.
ms.openlocfilehash: 6b035f4ee46af1750a275e2c61b2cddea06b37a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465460"
---
# <a name="responsemessages-arrayofdelegateuserresponsemessagetype"></a><span data-ttu-id="e2176-103">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="e2176-103">ResponseMessages (ArrayOfDelegateUserResponseMessageType)</span></span>

<span data-ttu-id="e2176-104">El elemento **ResponseMessages** contiene los mensajes de respuesta para una solicitud de administración de delegado de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e2176-104">The **ResponseMessages** element contains the response messages for an Exchange Web Services delegate management request.</span></span> 
  
```
<ResponseMessages>
   <DelegateUserResponseMessageType/>
</ResponseMessages>
```

 <span data-ttu-id="e2176-105">**ArrayOfDelegateUserResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e2176-105">**ArrayOfDelegateUserResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e2176-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e2176-106">Attributes and elements</span></span>

<span data-ttu-id="e2176-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e2176-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2176-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e2176-108">Attributes</span></span>

<span data-ttu-id="e2176-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e2176-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e2176-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e2176-110">Child elements</span></span>

|<span data-ttu-id="e2176-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e2176-111">**Element**</span></span>|<span data-ttu-id="e2176-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e2176-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2176-113">DelegateUserResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="e2176-113">DelegateUserResponseMessageType</span></span>](delegateuserresponsemessagetype.md) <br/> |<span data-ttu-id="e2176-114">Contiene mensajes de respuesta para las operaciones de administración de delegado.</span><span class="sxs-lookup"><span data-stu-id="e2176-114">Contains response messages for delegate management operations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e2176-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e2176-115">Parent elements</span></span>

|<span data-ttu-id="e2176-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e2176-116">**Element**</span></span>|<span data-ttu-id="e2176-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e2176-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2176-118">AddDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="e2176-118">AddDelegateResponse</span></span>](adddelegateresponse.md) <br/> |<span data-ttu-id="e2176-119">Contiene el estado y el resultado de una solicitud de [operación AddDelegate](adddelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="e2176-119">Contains the status and result of an [AddDelegate operation](adddelegate-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="e2176-120">GetDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="e2176-120">GetDelegateResponse</span></span>](getdelegateresponse.md) <br/> |<span data-ttu-id="e2176-121">Contiene el estado y el resultado de una solicitud de [operación GetDelegate](getdelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="e2176-121">Contains the status and result of a [GetDelegate operation](getdelegate-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="e2176-122">UpdateDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="e2176-122">UpdateDelegateResponse</span></span>](updatedelegateresponse.md) <br/> |<span data-ttu-id="e2176-123">Contiene el estado y el resultado de una solicitud de [operación UpdateDelegate](updatedelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="e2176-123">Contains the status and result of an [UpdateDelegate operation](updatedelegate-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="e2176-124">RemoveDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="e2176-124">RemoveDelegateResponse</span></span>](removedelegateresponse.md) <br/> |<span data-ttu-id="e2176-125">Contiene el estado y el resultado de una solicitud de [operación RemoveDelegate](removedelegate-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="e2176-125">Contains the status and result of a [RemoveDelegate operation](removedelegate-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2176-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2176-126">Remarks</span></span>

<span data-ttu-id="e2176-127">Este elemento se usa en la [operación AddDelegate](adddelegate-operation.md), en la operación [GetDelegate](getdelegate-operation.md), en la [operación UpdateDelegate](updatedelegate-operation.md)y en la [operación RemoveDelegate](removedelegate-operation.md).</span><span class="sxs-lookup"><span data-stu-id="e2176-127">This element is used in the [AddDelegate operation](adddelegate-operation.md), the [GetDelegate operation](getdelegate-operation.md), the [UpdateDelegate operation](updatedelegate-operation.md), and the [RemoveDelegate operation](removedelegate-operation.md).</span></span> <span data-ttu-id="e2176-128">Las respuestas de la operación de administración de delegado tienen una estructura distinta que otras respuestas.</span><span class="sxs-lookup"><span data-stu-id="e2176-128">The delegate management operation responses are structured differently than other responses.</span></span> <span data-ttu-id="e2176-129">Los mensajes de respuesta de administración de delegado tienen establecimiento inflexible de tipos.</span><span class="sxs-lookup"><span data-stu-id="e2176-129">The delegate management response messages are strongly typed.</span></span>
  
<span data-ttu-id="e2176-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con el rol de servidor acceso de clientes instalado.</span><span class="sxs-lookup"><span data-stu-id="e2176-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e2176-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e2176-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2176-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2176-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e2176-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e2176-133">Schema Name</span></span>  <br/> |<span data-ttu-id="e2176-134">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e2176-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e2176-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e2176-135">Validation File</span></span>  <br/> |<span data-ttu-id="e2176-136">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="e2176-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e2176-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e2176-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="e2176-138">Falso</span><span class="sxs-lookup"><span data-stu-id="e2176-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2176-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2176-139">See also</span></span>



[<span data-ttu-id="e2176-140">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="e2176-140">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="e2176-141">Operación GetDelegate</span><span class="sxs-lookup"><span data-stu-id="e2176-141">GetDelegate operation</span></span>](getdelegate-operation.md)
  
[<span data-ttu-id="e2176-142">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="e2176-142">UpdateDelegate operation</span></span>](updatedelegate-operation.md)
  
[<span data-ttu-id="e2176-143">Operación RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="e2176-143">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="e2176-144">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e2176-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

