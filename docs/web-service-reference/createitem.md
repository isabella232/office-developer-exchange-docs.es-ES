---
title: CreateItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: c3707feb-3fd4-4b8a-a68f-2abadd455163
description: El elemento CreateItem define una solicitud para crear un elemento en el almacén de Exchange.
ms.openlocfilehash: bb5cddd5ea4fa1b73c424275a0b0219ce3e189e3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763956"
---
# <a name="createitem"></a><span data-ttu-id="7fc0e-103">CreateItem</span><span class="sxs-lookup"><span data-stu-id="7fc0e-103">CreateItem</span></span>

<span data-ttu-id="7fc0e-104">El elemento **CreateItem** define una solicitud para crear un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-104">The **CreateItem** element defines a request to create an item in the Exchange store.</span></span> 
  
```xml
<CreateItem MessageDisposition="" SendMeetingInvitations="">
   <SavedItemFolderId/>
   <Items/>
</CreateItem>
```

 <span data-ttu-id="7fc0e-105">**CreateItemType**</span><span class="sxs-lookup"><span data-stu-id="7fc0e-105">**CreateItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7fc0e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7fc0e-106">Attributes and elements</span></span>

<span data-ttu-id="7fc0e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7fc0e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7fc0e-108">Attributes</span></span>

|<span data-ttu-id="7fc0e-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7fc0e-109">**Attribute**</span></span>|<span data-ttu-id="7fc0e-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7fc0e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7fc0e-111">**MessageDisposition**</span><span class="sxs-lookup"><span data-stu-id="7fc0e-111">**MessageDisposition**</span></span> <br/> |<span data-ttu-id="7fc0e-112">Describe cómo se controlarán el elemento después de crearla.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-112">Describes how the item will be handled after it is created.</span></span> <span data-ttu-id="7fc0e-113">El atributo es necesario para los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-113">The attribute is required for e-mail messages.</span></span> <span data-ttu-id="7fc0e-114">Este atributo sólo es aplicable a los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-114">This attribute is only applicable to e-mail messages.</span></span>  <br/> |
|<span data-ttu-id="7fc0e-115">**SendMeetingInvitations**</span><span class="sxs-lookup"><span data-stu-id="7fc0e-115">**SendMeetingInvitations**</span></span> <br/> |<span data-ttu-id="7fc0e-116">Describe cómo se controlan las convocatorias de reunión después de que se crean.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-116">Describes how meeting requests are handled after they are created.</span></span> <span data-ttu-id="7fc0e-117">Este atributo es necesario para los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-117">This attribute is required for calendar items.</span></span>  <br/> |
   
#### <a name="messagedisposition-attribute"></a><span data-ttu-id="7fc0e-118">Atributo MessageDisposition</span><span class="sxs-lookup"><span data-stu-id="7fc0e-118">MessageDisposition Attribute</span></span>

|<span data-ttu-id="7fc0e-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7fc0e-119">**Value**</span></span>|<span data-ttu-id="7fc0e-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7fc0e-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7fc0e-121">SaveOnly</span><span class="sxs-lookup"><span data-stu-id="7fc0e-121">SaveOnly</span></span>  <br/> |<span data-ttu-id="7fc0e-122">El elemento de mensaje se guarda en la carpeta que se especifica mediante el elemento [SavedItemFolderId](saveditemfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="7fc0e-122">The message item is saved in the folder that is specified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span> <span data-ttu-id="7fc0e-123">Los mensajes se pueden enviar más adelante mediante el uso de la [operación de SendItem](senditem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="7fc0e-123">Messages can be sent later by using the [SendItem operation](senditem-operation.md).</span></span> <span data-ttu-id="7fc0e-124">Un identificador de elemento se devuelve en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-124">An item identifier is returned in the response.</span></span> <span data-ttu-id="7fc0e-125">No se devuelven los identificadores de elemento para los tipos de elemento, excepto los elementos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-125">Item identifiers are not returned for any item types except for message items.</span></span> <span data-ttu-id="7fc0e-126">Esto incluye los objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-126">This includes response objects.</span></span>  <br/> |
|<span data-ttu-id="7fc0e-127">SendOnly</span><span class="sxs-lookup"><span data-stu-id="7fc0e-127">SendOnly</span></span>  <br/> |<span data-ttu-id="7fc0e-128">El elemento se envía pero ninguna copia se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-128">The item is sent but no copy is saved in the Sent Items folder.</span></span> <span data-ttu-id="7fc0e-129">Un identificador de elemento no se devuelve en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-129">An item identifier is not returned in the response.</span></span>  <br/> <span data-ttu-id="7fc0e-130">> [!NOTE]> **CreateItem** no admite el acceso de delegado cuando se utiliza la opción SendOnly porque no se puede especificar una carpeta de destino con esta opción.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-130">> [!NOTE]> **CreateItem** does not support delegate access when the SendOnly option is used because a destination folder cannot be specified with this option.</span></span> <span data-ttu-id="7fc0e-131">La solución consiste en crear el elemento, obtener el identificador de elemento y, a continuación, use la operación de SendItem para enviar el elemento.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-131">The workaround is to create the item, get the item identifier, and then use the SendItem operation to send the item.</span></span>           |
|<span data-ttu-id="7fc0e-132">SendAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="7fc0e-132">SendAndSaveCopy</span></span>  <br/> |<span data-ttu-id="7fc0e-133">El elemento se envía y se guarda una copia en la carpeta que se identifica con el elemento [SavedItemFolderId](saveditemfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="7fc0e-133">The item is sent and a copy is saved in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span> <span data-ttu-id="7fc0e-134">Un identificador de elemento no se devuelve en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-134">An item identifier is not returned in the response.</span></span>  <br/> <span data-ttu-id="7fc0e-135">> [!NOTE]> Las convocatorias de reunión no se guardan en la carpeta que se identifica con la propiedad [SavedItemFolderId](saveditemfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="7fc0e-135">> [!NOTE]> Meeting requests are not saved to the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) property.</span></span> <span data-ttu-id="7fc0e-136">Para el calendario, sólo la operación de guardar se puede especificar la ubicación para los elementos de calendario mediante la propiedad **SavedItemFolderId** .</span><span class="sxs-lookup"><span data-stu-id="7fc0e-136">For calendaring, only the save location for calendar items can be specified by the **SavedItemFolderId** property.</span></span> <span data-ttu-id="7fc0e-137">No se puede controlar donde una convocatoria de reunión elemento se ha guardado.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-137">You cannot control where a meeting request item is saved.</span></span> <span data-ttu-id="7fc0e-138">Sólo los elementos de calendario asociadas se copian y guardar los datos en la carpeta que se identifica con la propiedad **SavedItemFolderId** .</span><span class="sxs-lookup"><span data-stu-id="7fc0e-138">Only the associated calendar items are copied and saved into the folder that is identified by the **SavedItemFolderId** property.</span></span>           |
   
#### <a name="sendmeetinginvitations-attribute"></a><span data-ttu-id="7fc0e-139">Atributo SendMeetingInvitations</span><span class="sxs-lookup"><span data-stu-id="7fc0e-139">SendMeetingInvitations Attribute</span></span>

|<span data-ttu-id="7fc0e-140">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7fc0e-140">**Value**</span></span>|<span data-ttu-id="7fc0e-141">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7fc0e-141">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7fc0e-142">SendToNone</span><span class="sxs-lookup"><span data-stu-id="7fc0e-142">SendToNone</span></span>  <br/> |<span data-ttu-id="7fc0e-143">Si el elemento es una convocatoria de reunión, se guarda como un elemento de calendario, aunque no envía.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-143">If the item is a meeting request, it is saved as a calendar item but not sent.</span></span>  <br/> |
|<span data-ttu-id="7fc0e-144">SendOnlyToAll</span><span class="sxs-lookup"><span data-stu-id="7fc0e-144">SendOnlyToAll</span></span>  <br/> |<span data-ttu-id="7fc0e-145">La convocatoria de reunión se envía a todos los asistentes, pero no se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-145">The meeting request is sent to all attendees but is not saved in the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="7fc0e-146">SendToAllAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="7fc0e-146">SendToAllAndSaveCopy</span></span>  <br/> |<span data-ttu-id="7fc0e-147">La convocatoria de reunión se envía a todos los asistentes y se guarda una copia en la carpeta que se identifica con el elemento [SavedItemFolderId](saveditemfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="7fc0e-147">The meeting request is sent to all attendees and a copy is saved in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7fc0e-148">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7fc0e-148">Child elements</span></span>

|<span data-ttu-id="7fc0e-149">**Element**</span><span class="sxs-lookup"><span data-stu-id="7fc0e-149">**Element**</span></span>|<span data-ttu-id="7fc0e-150">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7fc0e-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7fc0e-151">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="7fc0e-151">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> |<span data-ttu-id="7fc0e-152">Identifica la carpeta de destino donde se puede crear un nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-152">Identifies the target folder where a new item can be created.</span></span> <span data-ttu-id="7fc0e-153">Si se establece el atributo **MessageDisposition** en SendOnly, sólo se enviará un mensaje de creación.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-153">If the **MessageDisposition** attribute is set to SendOnly, a created message will only be sent.</span></span> <span data-ttu-id="7fc0e-154">No se va a colocar el mensaje en la carpeta que se identifica con el elemento [SavedItemFolderId](saveditemfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="7fc0e-154">The message will not be put in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="7fc0e-155">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="7fc0e-155">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="7fc0e-156">Contiene una matriz de elementos que desea crear en la carpeta que se identifica con el elemento [SavedItemFolderId](saveditemfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="7fc0e-156">Contains an array of items to create in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7fc0e-157">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7fc0e-157">Parent elements</span></span>

<span data-ttu-id="7fc0e-158">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-158">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7fc0e-159">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fc0e-159">Remarks</span></span>

<span data-ttu-id="7fc0e-160">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="7fc0e-160">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7fc0e-161">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7fc0e-161">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fc0e-162">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7fc0e-162">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7fc0e-163">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7fc0e-163">Schema Name</span></span>  <br/> |<span data-ttu-id="7fc0e-164">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="7fc0e-164">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7fc0e-165">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7fc0e-165">Validation File</span></span>  <br/> |<span data-ttu-id="7fc0e-166">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7fc0e-166">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7fc0e-167">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7fc0e-167">Can be Empty</span></span>  <br/> |<span data-ttu-id="7fc0e-168">False</span><span class="sxs-lookup"><span data-stu-id="7fc0e-168">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7fc0e-169">Ver también</span><span class="sxs-lookup"><span data-stu-id="7fc0e-169">See also</span></span>



[<span data-ttu-id="7fc0e-170">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="7fc0e-170">CreateItemResponse</span></span>](createitemresponse.md)
  
[<span data-ttu-id="7fc0e-171">Operación CreateItem</span><span class="sxs-lookup"><span data-stu-id="7fc0e-171">CreateItem operation</span></span>](createitem-operation.md)
  
 <span data-ttu-id="7fc0e-172">**CreateItemType**</span><span class="sxs-lookup"><span data-stu-id="7fc0e-172">**CreateItemType**</span></span>


[<span data-ttu-id="7fc0e-173">Creación de mensajes de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="7fc0e-173">Creating E-mail Messages</span></span>](http://msdn.microsoft.com/library/05bfb83c-2866-427d-a9fe-14ba3cb02793%28Office.15%29.aspx)
  
[<span data-ttu-id="7fc0e-174">Creación de contactos (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="7fc0e-174">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[<span data-ttu-id="7fc0e-175">Creación de tareas</span><span class="sxs-lookup"><span data-stu-id="7fc0e-175">Creating Tasks</span></span>](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="7fc0e-176">Crear citas</span><span class="sxs-lookup"><span data-stu-id="7fc0e-176">Creating Appointments</span></span>](http://msdn.microsoft.com/library/2385391e-c9e7-4d45-b803-c4ff94d5c94e%28Office.15%29.aspx)

