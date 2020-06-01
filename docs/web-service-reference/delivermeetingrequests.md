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
description: El elemento DeliverMeetingRequests define cómo se administran las convocatorias de reunión entre el delegado y la entidad de la identidad. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 3998443613437bca2267678f7bc2c5584b779135
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463681"
---
# <a name="delivermeetingrequests"></a><span data-ttu-id="3732b-104">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="3732b-104">DeliverMeetingRequests</span></span>

<span data-ttu-id="3732b-105">El elemento **DeliverMeetingRequests** define cómo se administran las convocatorias de reunión entre el delegado y la entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="3732b-105">The **DeliverMeetingRequests** element defines how meeting requests are handled between the delegate and the principal.</span></span> <span data-ttu-id="3732b-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="3732b-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```XML
<DeliverMeetingRequests>DelegatesOnly or DelegatesAndMe or DelegatesAndSendInformationToMe or NoForward</DeliverMeetingRequests>
```

 <span data-ttu-id="3732b-107">**DeliverMeetingRequestsType**</span><span class="sxs-lookup"><span data-stu-id="3732b-107">**DeliverMeetingRequestsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3732b-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3732b-108">Attributes and elements</span></span>

<span data-ttu-id="3732b-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3732b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3732b-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="3732b-110">Attributes</span></span>

<span data-ttu-id="3732b-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3732b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3732b-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3732b-112">Child elements</span></span>

<span data-ttu-id="3732b-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3732b-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3732b-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3732b-114">Parent elements</span></span>

|<span data-ttu-id="3732b-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3732b-115">**Element**</span></span>|<span data-ttu-id="3732b-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3732b-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3732b-117">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="3732b-117">AddDelegate</span></span>](adddelegate.md) <br/> |<span data-ttu-id="3732b-118">Define una solicitud para agregar delegados a un buzón.</span><span class="sxs-lookup"><span data-stu-id="3732b-118">Defines a request to add delegates to a mailbox.</span></span> <span data-ttu-id="3732b-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="3732b-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="3732b-120">UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="3732b-120">UpdateDelegate</span></span>](updatedelegate.md) <br/> |<span data-ttu-id="3732b-121">Define una solicitud para actualizar delegados en un buzón.</span><span class="sxs-lookup"><span data-stu-id="3732b-121">Defines a request to update delegates in a mailbox.</span></span> <span data-ttu-id="3732b-122">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="3732b-122">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="3732b-123">GetDelegateResponse</span><span class="sxs-lookup"><span data-stu-id="3732b-123">GetDelegateResponse</span></span>](getdelegateresponse.md) <br/> |<span data-ttu-id="3732b-124">Contiene el estado y el resultado de una solicitud GetDelegate.</span><span class="sxs-lookup"><span data-stu-id="3732b-124">Contains the status and result of a GetDelegate request.</span></span> <span data-ttu-id="3732b-125">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="3732b-125">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3732b-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3732b-126">Text value</span></span>

<span data-ttu-id="3732b-127">En la siguiente tabla se enumeran los valores posibles para el elemento **DeliverMeetingRequests** .</span><span class="sxs-lookup"><span data-stu-id="3732b-127">The following table lists the possible values for the **DeliverMeetingRequests** element.</span></span> 
  
<span data-ttu-id="3732b-128">**Valores del elemento DeliverMeetingRequests**</span><span class="sxs-lookup"><span data-stu-id="3732b-128">**DeliverMeetingRequests element values**</span></span>

|<span data-ttu-id="3732b-129">**Valor**</span><span class="sxs-lookup"><span data-stu-id="3732b-129">**Value**</span></span>|<span data-ttu-id="3732b-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3732b-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3732b-131">DelegatesOnly</span><span class="sxs-lookup"><span data-stu-id="3732b-131">DelegatesOnly</span></span>  <br/> |<span data-ttu-id="3732b-132">Las convocatorias de reunión se reenvían al delegado y se mueven a la carpeta elementos eliminados en el buzón de la entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="3732b-132">Meeting requests are forwarded to the delegate and moved to the Deleted Items folder in the principal's mailbox.</span></span>  <br/> |
|<span data-ttu-id="3732b-133">DelegatesAndMe</span><span class="sxs-lookup"><span data-stu-id="3732b-133">DelegatesAndMe</span></span>  <br/> |<span data-ttu-id="3732b-134">Las convocatorias de reunión se reenvían al delegado y permanecen en la carpeta Bandeja de entrada en el buzón de la entidad.</span><span class="sxs-lookup"><span data-stu-id="3732b-134">Meeting requests are forwarded to the delegate and remain in the Inbox folder in the principal's mailbox.</span></span>  <br/> |
|<span data-ttu-id="3732b-135">DelegatesAndSendInformationToMe</span><span class="sxs-lookup"><span data-stu-id="3732b-135">DelegatesAndSendInformationToMe</span></span>  <br/> |<span data-ttu-id="3732b-136">Las convocatorias de reunión se reenvían al delegado y permanecen en la carpeta Bandeja de entrada en el buzón de correo de la entidad de la identidad, pero los botones aceptar, provisional y rechazar no aparecen en el panel de lectura de Microsoft Office Outlook.</span><span class="sxs-lookup"><span data-stu-id="3732b-136">Meeting requests are forwarded to the delegate and remain in the Inbox folder in the principal's mailbox, but the Accept, Tentative, and Decline buttons do not appear in the Microsoft Office Outlook reading pane.</span></span>  <br/> |
|<span data-ttu-id="3732b-137">No reenviar</span><span class="sxs-lookup"><span data-stu-id="3732b-137">NoForward</span></span>  <br/> |<span data-ttu-id="3732b-138">Las convocatorias de reunión no se reenvían al delegado.</span><span class="sxs-lookup"><span data-stu-id="3732b-138">Meeting requests are not forwarded to the delegate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3732b-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3732b-139">Remarks</span></span>

<span data-ttu-id="3732b-140">La configuración **DeliverMeetingRequests** afecta a todos los delegados del buzón de una entidad de identidad.</span><span class="sxs-lookup"><span data-stu-id="3732b-140">The **DeliverMeetingRequests** setting affects all delegates in a principal's mailbox.</span></span> 
  
<span data-ttu-id="3732b-141">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3732b-141">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3732b-142">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3732b-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3732b-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="3732b-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3732b-144">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3732b-144">Schema Name</span></span>  <br/> |<span data-ttu-id="3732b-145">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3732b-145">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3732b-146">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3732b-146">Validation File</span></span>  <br/> |<span data-ttu-id="3732b-147">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3732b-147">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3732b-148">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3732b-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="3732b-149">Falso</span><span class="sxs-lookup"><span data-stu-id="3732b-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3732b-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="3732b-150">See also</span></span>

- [<span data-ttu-id="3732b-151">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="3732b-151">AddDelegate operation</span></span>](adddelegate-operation.md)  
- [<span data-ttu-id="3732b-152">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="3732b-152">UpdateDelegate operation</span></span>](updatedelegate-operation.md)  
- [<span data-ttu-id="3732b-153">Operación GetDelegate</span><span class="sxs-lookup"><span data-stu-id="3732b-153">GetDelegate operation</span></span>](getdelegate-operation.md)
- [<span data-ttu-id="3732b-154">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3732b-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="3732b-155">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="3732b-155">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

