---
title: DeliverMeetingRequests
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeliverMeetingRequests
api_type:
- schema
ms.assetid: 04b999af-0b27-4e6d-a8b1-400955a1afaa
description: El elemento DeliverMeetingRequests define cómo se controlan las convocatorias de reunión entre el delegado y la entidad de seguridad. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 803bd2da72bdb21b507a59cc11635a40d4431acf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764121"
---
# <a name="delivermeetingrequests"></a><span data-ttu-id="db454-104">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="db454-104">DeliverMeetingRequests</span></span>

<span data-ttu-id="db454-105">El elemento **DeliverMeetingRequests** define cómo se controlan las convocatorias de reunión entre el delegado y la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="db454-105">The **DeliverMeetingRequests** element defines how meeting requests are handled between the delegate and the principal.</span></span> <span data-ttu-id="db454-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="db454-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```XML
<DeliverMeetingRequests>DelegatesOnly or DelegatesAndMe or DelegatesAndSendInformationToMe or NoForward</DeliverMeetingRequests>
```

 <span data-ttu-id="db454-107">**DeliverMeetingRequestsType**</span><span class="sxs-lookup"><span data-stu-id="db454-107">**DeliverMeetingRequestsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="db454-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="db454-108">Attributes and elements</span></span>

<span data-ttu-id="db454-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="db454-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="db454-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="db454-110">Attributes</span></span>

<span data-ttu-id="db454-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="db454-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="db454-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="db454-112">Child elements</span></span>

<span data-ttu-id="db454-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="db454-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="db454-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="db454-114">Parent elements</span></span>

|<span data-ttu-id="db454-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="db454-115">**Element**</span></span>|<span data-ttu-id="db454-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="db454-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="db454-117">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="db454-117">AddDelegate</span></span>](adddelegate.md) <br/> |<span data-ttu-id="db454-118">Define una solicitud para agregar delegados a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="db454-118">Defines a request to add delegates to a mailbox.</span></span> <span data-ttu-id="db454-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="db454-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="db454-120">UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="db454-120">UpdateDelegate</span></span>](updatedelegate.md) <br/> |<span data-ttu-id="db454-121">Define una solicitud para actualizar los delegados en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="db454-121">Defines a request to update delegates in a mailbox.</span></span> <span data-ttu-id="db454-122">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="db454-122">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="db454-123">GetDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="db454-123">GetDelegateResponse</span></span>](getdelegateresponse.md) <br/> |<span data-ttu-id="db454-124">Contiene el estado y el resultado de una solicitud de GetDelegate.</span><span class="sxs-lookup"><span data-stu-id="db454-124">Contains the status and result of a GetDelegate request.</span></span> <span data-ttu-id="db454-125">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="db454-125">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="db454-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="db454-126">Text value</span></span>

<span data-ttu-id="db454-127">En la siguiente tabla se enumera los valores posibles para el elemento **DeliverMeetingRequests** .</span><span class="sxs-lookup"><span data-stu-id="db454-127">The following table lists the possible values for the **DeliverMeetingRequests** element.</span></span> 
  
<span data-ttu-id="db454-128">**Valores de elemento DeliverMeetingRequests**</span><span class="sxs-lookup"><span data-stu-id="db454-128">**DeliverMeetingRequests element values**</span></span>

|<span data-ttu-id="db454-129">**Valor**</span><span class="sxs-lookup"><span data-stu-id="db454-129">**Value**</span></span>|<span data-ttu-id="db454-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="db454-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="db454-131">DelegatesOnly</span><span class="sxs-lookup"><span data-stu-id="db454-131">DelegatesOnly</span></span>  <br/> |<span data-ttu-id="db454-132">Las convocatorias de reunión se transfieren al delegado y movidas a la carpeta Elementos eliminados en el buzón de la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="db454-132">Meeting requests are forwarded to the delegate and moved to the Deleted Items folder in the principal's mailbox.</span></span>  <br/> |
|<span data-ttu-id="db454-133">DelegatesAndMe</span><span class="sxs-lookup"><span data-stu-id="db454-133">DelegatesAndMe</span></span>  <br/> |<span data-ttu-id="db454-134">Las convocatorias de reunión se transfieren al delegado y permanecerán en la carpeta Bandeja de entrada en el buzón de la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="db454-134">Meeting requests are forwarded to the delegate and remain in the Inbox folder in the principal's mailbox.</span></span>  <br/> |
|<span data-ttu-id="db454-135">DelegatesAndSendInformationToMe</span><span class="sxs-lookup"><span data-stu-id="db454-135">DelegatesAndSendInformationToMe</span></span>  <br/> |<span data-ttu-id="db454-136">Las convocatorias de reunión se transfieren al delegado y permanecerán en la carpeta Bandeja de entrada en el buzón de la entidad de seguridad, pero los botones Aceptar, provisional y rechazar no aparecen en el panel de lectura de Microsoft Office Outlook.</span><span class="sxs-lookup"><span data-stu-id="db454-136">Meeting requests are forwarded to the delegate and remain in the Inbox folder in the principal's mailbox, but the Accept, Tentative, and Decline buttons do not appear in the Microsoft Office Outlook reading pane.</span></span>  <br/> |
|<span data-ttu-id="db454-137">NoForward</span><span class="sxs-lookup"><span data-stu-id="db454-137">NoForward</span></span>  <br/> |<span data-ttu-id="db454-138">Las convocatorias de reunión no se transfieren al delegado.</span><span class="sxs-lookup"><span data-stu-id="db454-138">Meeting requests are not forwarded to the delegate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db454-139">Notas</span><span class="sxs-lookup"><span data-stu-id="db454-139">Remarks</span></span>

<span data-ttu-id="db454-140">La configuración de **DeliverMeetingRequests** afecta a todos los delegados en el buzón de correo de una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="db454-140">The **DeliverMeetingRequests** setting affects all delegates in a principal's mailbox.</span></span> 
  
<span data-ttu-id="db454-141">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="db454-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="db454-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="db454-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db454-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="db454-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="db454-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="db454-144">Schema Name</span></span>  <br/> |<span data-ttu-id="db454-145">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="db454-145">Messages schema</span></span>  <br/> |
|<span data-ttu-id="db454-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="db454-146">Validation File</span></span>  <br/> |<span data-ttu-id="db454-147">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="db454-147">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="db454-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="db454-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="db454-149">False</span><span class="sxs-lookup"><span data-stu-id="db454-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="db454-150">Ver también</span><span class="sxs-lookup"><span data-stu-id="db454-150">See also</span></span>

- [<span data-ttu-id="db454-151">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="db454-151">AddDelegate operation</span></span>](adddelegate-operation.md)  
- [<span data-ttu-id="db454-152">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="db454-152">UpdateDelegate operation</span></span>](updatedelegate-operation.md)  
- [<span data-ttu-id="db454-153">Operación GetDelegate</span><span class="sxs-lookup"><span data-stu-id="db454-153">GetDelegate operation</span></span>](getdelegate-operation.md)
- [<span data-ttu-id="db454-154">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="db454-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="db454-155">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="db454-155">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

