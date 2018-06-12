---
title: Operación GetItem (tarea)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: 8265dd06-1752-4470-8074-5f0e3e970f52
description: La operación GetItem se usa para obtener las tareas desde el almacén de Exchange.
ms.openlocfilehash: 412710f32ed8702e1a28a596833c3a7e47e3ed76
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764898"
---
# <a name="getitem-operation-task"></a><span data-ttu-id="bb0ff-103">Operación GetItem (tarea)</span><span class="sxs-lookup"><span data-stu-id="bb0ff-103">GetItem operation (task)</span></span>

<span data-ttu-id="bb0ff-104">La operación GetItem se usa para obtener las tareas desde el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="bb0ff-104">The GetItem operation is used to get tasks from the Exchange store.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bb0ff-105">Notas</span><span class="sxs-lookup"><span data-stu-id="bb0ff-105">Remarks</span></span>

<span data-ttu-id="bb0ff-106">El formato de la solicitud de GetItem para las tareas es el mismo que GetItem para cualquier otro tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="bb0ff-106">The format of the GetItem request for tasks is the same as GetItem for any other item type.</span></span> <span data-ttu-id="bb0ff-107">La única diferencia es que en el que se pueden solicitar propiedades adicionales dentro de la forma de respuesta.</span><span class="sxs-lookup"><span data-stu-id="bb0ff-107">The only difference is in which additional properties can be requested within the response shape.</span></span> <span data-ttu-id="bb0ff-108">Esas propiedades adicionales deben ser propiedades relacionadas con la tarea o las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="bb0ff-108">Such additional properties must either be task-related properties or extended properties.</span></span>
  
## <a name="task-getitem-request-example"></a><span data-ttu-id="bb0ff-109">Ejemplo de solicitud de tarea GetItem</span><span class="sxs-lookup"><span data-stu-id="bb0ff-109">Task GetItem request example</span></span>

### <a name="description"></a><span data-ttu-id="bb0ff-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb0ff-110">Description</span></span>

<span data-ttu-id="bb0ff-111">El siguiente ejemplo de una solicitud de GetItem muestra cómo obtener un elemento de tarea.</span><span class="sxs-lookup"><span data-stu-id="bb0ff-111">The following example of a GetItem request shows how to get a task item.</span></span>
  
### <a name="code"></a><span data-ttu-id="bb0ff-112">Código</span><span class="sxs-lookup"><span data-stu-id="bb0ff-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <ItemShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="AAAtAEFkb..."/>
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="bb0ff-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb0ff-113">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="bb0ff-114">El identificador de elemento y la clave de cambio se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="bb0ff-114">The item identifier and change key have been shortened to preserve readability.</span></span> 
  
### <a name="request-elements"></a><span data-ttu-id="bb0ff-115">Elementos de solicitud</span><span class="sxs-lookup"><span data-stu-id="bb0ff-115">Request elements</span></span>

<span data-ttu-id="bb0ff-116">En la solicitud se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="bb0ff-116">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="bb0ff-117">GetItem</span><span class="sxs-lookup"><span data-stu-id="bb0ff-117">GetItem</span></span>](getitem.md)
    
- [<span data-ttu-id="bb0ff-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="bb0ff-118">ItemShape</span></span>](itemshape.md)
    
- [<span data-ttu-id="bb0ff-119">BaseShape</span><span class="sxs-lookup"><span data-stu-id="bb0ff-119">BaseShape</span></span>](baseshape.md)
    
- [<span data-ttu-id="bb0ff-120">ItemId</span><span class="sxs-lookup"><span data-stu-id="bb0ff-120">ItemIds</span></span>](itemids.md)
    
- [<span data-ttu-id="bb0ff-121">ItemId</span><span class="sxs-lookup"><span data-stu-id="bb0ff-121">ItemId</span></span>](itemid.md)
    
## <a name="task-getitem-response-example"></a><span data-ttu-id="bb0ff-122">Ejemplo de respuesta de tarea GetItem</span><span class="sxs-lookup"><span data-stu-id="bb0ff-122">Task GetItem response example</span></span>

### <a name="description"></a><span data-ttu-id="bb0ff-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb0ff-123">Description</span></span>

<span data-ttu-id="bb0ff-124">En el ejemplo siguiente se muestra una respuesta a una solicitud de GetItem correcta.</span><span class="sxs-lookup"><span data-stu-id="bb0ff-124">The following example shows a successful response to a GetItem request.</span></span>
  
### <a name="code"></a><span data-ttu-id="bb0ff-125">Código</span><span class="sxs-lookup"><span data-stu-id="bb0ff-125">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="662" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                     xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                     xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Task>
              <t:ItemId Id="AAAtAEA=" ChangeKey="EwAAAB"/>
              <t:ParentFolderId Id="AAAtAEFkbWl=" ChangeKey="AQAAAA=="/>
              <t:ItemClass>IPM.Task</t:ItemClass>
              <t:Subject>Buy new shoes</t:Subject>
              <t:Sensitivity>Normal</t:Sensitivity>
              <t:Body BodyType="Text"/>
              <t:DateTimeReceived>2006-09-15T15:23:08Z</t:DateTimeReceived>
              <t:Size>153</t:Size>
              <t:Importance>Normal</t:Importance>
              <t:IsSubmitted>false</t:IsSubmitted>
              <t:IsDraft>true</t:IsDraft>
              <t:IsFromMe>false</t:IsFromMe>
              <t:IsResend>false</t:IsResend>
              <t:IsUnmodified>false</t:IsUnmodified>
              <t:DateTimeSent>2006-09-15T15:23:08Z</t:DateTimeSent>
              <t:DateTimeCreated>2006-09-15T15:23:08Z</t:DateTimeCreated>
              <t:HasAttachments>false</t:HasAttachments>
              <t:Culture>en-US</t:Culture>
              <t:ChangeCount>1</t:ChangeCount>
              <t:IsComplete>false</t:IsComplete>
              <t:IsRecurring>false</t:IsRecurring>
              <t:PercentComplete>0</t:PercentComplete>
              <t:Status>NotStarted</t:Status>
              <t:StatusDescription>Not Started</t:StatusDescription>
            </t:Task>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </GetItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="bb0ff-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb0ff-126">Comments</span></span>

> [!NOTE]
> <span data-ttu-id="bb0ff-127">Los identificadores de elemento y carpeta y cambiar claves se han abreviado para conservar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="bb0ff-127">The item and folder identifiers and change keys have been shortened to preserve readability.</span></span> 
  
### <a name="successful-response-elements"></a><span data-ttu-id="bb0ff-128">Elementos de respuesta correcta</span><span class="sxs-lookup"><span data-stu-id="bb0ff-128">Successful response elements</span></span>

<span data-ttu-id="bb0ff-129">En la respuesta se usan los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="bb0ff-129">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="bb0ff-130">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="bb0ff-130">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="bb0ff-131">GetItemResponse</span><span class="sxs-lookup"><span data-stu-id="bb0ff-131">GetItemResponse</span></span>](getitemresponse.md)
    
- [<span data-ttu-id="bb0ff-132">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="bb0ff-132">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="bb0ff-133">GetItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bb0ff-133">GetItemResponseMessage</span></span>](getitemresponsemessage.md)
    
- [<span data-ttu-id="bb0ff-134">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="bb0ff-134">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="bb0ff-135">Items</span><span class="sxs-lookup"><span data-stu-id="bb0ff-135">Items</span></span>](items.md)
    
- [<span data-ttu-id="bb0ff-136">Tarea</span><span class="sxs-lookup"><span data-stu-id="bb0ff-136">Task</span></span>](task.md)
    
- [<span data-ttu-id="bb0ff-137">ItemId</span><span class="sxs-lookup"><span data-stu-id="bb0ff-137">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="bb0ff-138">Id</span><span class="sxs-lookup"><span data-stu-id="bb0ff-138">ParentFolderId</span></span>](parentfolderid.md)
    
- [<span data-ttu-id="bb0ff-139">ItemClass</span><span class="sxs-lookup"><span data-stu-id="bb0ff-139">ItemClass</span></span>](itemclass.md)
    
- [<span data-ttu-id="bb0ff-140">Subject</span><span class="sxs-lookup"><span data-stu-id="bb0ff-140">Subject</span></span>](subject.md)
    
- [<span data-ttu-id="bb0ff-141">Sensibilidad</span><span class="sxs-lookup"><span data-stu-id="bb0ff-141">Sensitivity</span></span>](sensitivity.md)
    
- [<span data-ttu-id="bb0ff-142">Body</span><span class="sxs-lookup"><span data-stu-id="bb0ff-142">Body</span></span>](body.md)
    
- [<span data-ttu-id="bb0ff-143">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="bb0ff-143">DateTimeReceived</span></span>](datetimereceived.md)
    
- [<span data-ttu-id="bb0ff-144">Size</span><span class="sxs-lookup"><span data-stu-id="bb0ff-144">Size</span></span>](size.md)
    
- [<span data-ttu-id="bb0ff-145">Importancia</span><span class="sxs-lookup"><span data-stu-id="bb0ff-145">Importance</span></span>](importance.md)
    
- [<span data-ttu-id="bb0ff-146">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="bb0ff-146">IsSubmitted</span></span>](issubmitted.md)
    
- [<span data-ttu-id="bb0ff-147">IsDraft</span><span class="sxs-lookup"><span data-stu-id="bb0ff-147">IsDraft</span></span>](isdraft.md)
    
- [<span data-ttu-id="bb0ff-148">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="bb0ff-148">IsFromMe</span></span>](isfromme.md)
    
- [<span data-ttu-id="bb0ff-149">IsResend</span><span class="sxs-lookup"><span data-stu-id="bb0ff-149">IsResend</span></span>](isresend.md)
    
- [<span data-ttu-id="bb0ff-150">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="bb0ff-150">IsUnmodified</span></span>](isunmodified.md)
    
- [<span data-ttu-id="bb0ff-151">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="bb0ff-151">DateTimeSent</span></span>](datetimesent.md)
    
- [<span data-ttu-id="bb0ff-152">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="bb0ff-152">DateTimeCreated</span></span>](datetimecreated.md)
    
- [<span data-ttu-id="bb0ff-153">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="bb0ff-153">HasAttachments</span></span>](hasattachments.md)
    
- [<span data-ttu-id="bb0ff-154">Referencia cultural</span><span class="sxs-lookup"><span data-stu-id="bb0ff-154">Culture</span></span>](culture.md)
    
- [<span data-ttu-id="bb0ff-155">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="bb0ff-155">ChangeCount</span></span>](changecount.md)
    
- [<span data-ttu-id="bb0ff-156">Haya finalizado</span><span class="sxs-lookup"><span data-stu-id="bb0ff-156">IsComplete</span></span>](iscomplete.md)
    
- [<span data-ttu-id="bb0ff-157">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="bb0ff-157">IsRecurring</span></span>](isrecurring.md)
    
- [<span data-ttu-id="bb0ff-158">PercentComplete</span><span class="sxs-lookup"><span data-stu-id="bb0ff-158">PercentComplete</span></span>](percentcomplete.md)
    
- [<span data-ttu-id="bb0ff-159">Status</span><span class="sxs-lookup"><span data-stu-id="bb0ff-159">Status</span></span>](status.md)
    
- [<span data-ttu-id="bb0ff-160">StatusDescription</span><span class="sxs-lookup"><span data-stu-id="bb0ff-160">StatusDescription</span></span>](statusdescription.md)
    
## <a name="see-also"></a><span data-ttu-id="bb0ff-161">Ver también</span><span class="sxs-lookup"><span data-stu-id="bb0ff-161">See also</span></span>



[<span data-ttu-id="bb0ff-162">Operación GetItem</span><span class="sxs-lookup"><span data-stu-id="bb0ff-162">GetItem operation</span></span>](getitem-operation.md)


[<span data-ttu-id="bb0ff-163">Creación de tareas</span><span class="sxs-lookup"><span data-stu-id="bb0ff-163">Creating Tasks</span></span>](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="bb0ff-164">Actualización de tareas</span><span class="sxs-lookup"><span data-stu-id="bb0ff-164">Updating Tasks</span></span>](http://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)
  
[<span data-ttu-id="bb0ff-165">Eliminación de tareas</span><span class="sxs-lookup"><span data-stu-id="bb0ff-165">Deleting Tasks</span></span>](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

