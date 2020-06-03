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
ms.openlocfilehash: 235664b7baeceeccb14135fd346123f0f7d99346
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527064"
---
# <a name="createitem"></a><span data-ttu-id="9cf5a-103">CreateItem</span><span class="sxs-lookup"><span data-stu-id="9cf5a-103">CreateItem</span></span>

<span data-ttu-id="9cf5a-104">El elemento **CreateItem** define una solicitud para crear un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-104">The **CreateItem** element defines a request to create an item in the Exchange store.</span></span> 
  
```xml
<CreateItem MessageDisposition="" SendMeetingInvitations="">
   <SavedItemFolderId/>
   <Items/>
</CreateItem>
```

<span data-ttu-id="9cf5a-105">**CreateItemType**</span><span class="sxs-lookup"><span data-stu-id="9cf5a-105">**CreateItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9cf5a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9cf5a-106">Attributes and elements</span></span>

<span data-ttu-id="9cf5a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9cf5a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9cf5a-108">Attributes</span></span>

|<span data-ttu-id="9cf5a-109">Atributo</span><span class="sxs-lookup"><span data-stu-id="9cf5a-109">Attribute</span></span>|<span data-ttu-id="9cf5a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9cf5a-110">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="9cf5a-111">**MessageDisposition**</span><span class="sxs-lookup"><span data-stu-id="9cf5a-111">**MessageDisposition**</span></span> <br/> |<span data-ttu-id="9cf5a-112">Describe cómo se controlará el elemento una vez creado.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-112">Describes how the item will be handled after it is created.</span></span> <span data-ttu-id="9cf5a-113">El atributo es necesario para los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-113">The attribute is required for e-mail messages.</span></span> <span data-ttu-id="9cf5a-114">Este atributo solo es aplicable a los mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-114">This attribute is only applicable to e-mail messages.</span></span>  <br/> |
|<span data-ttu-id="9cf5a-115">**SendMeetingInvitations**</span><span class="sxs-lookup"><span data-stu-id="9cf5a-115">**SendMeetingInvitations**</span></span> <br/> |<span data-ttu-id="9cf5a-116">Describe cómo se controlan las convocatorias de reunión después de su creación.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-116">Describes how meeting requests are handled after they are created.</span></span> <span data-ttu-id="9cf5a-117">Este atributo es necesario para los elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-117">This attribute is required for calendar items.</span></span>  <br/> |
   
#### <a name="messagedisposition-attribute"></a><span data-ttu-id="9cf5a-118">Atributo MessageDisposition</span><span class="sxs-lookup"><span data-stu-id="9cf5a-118">MessageDisposition Attribute</span></span>

|<span data-ttu-id="9cf5a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9cf5a-119">Value</span></span>|<span data-ttu-id="9cf5a-120">Description</span><span class="sxs-lookup"><span data-stu-id="9cf5a-120">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="9cf5a-121">SaveOnly</span><span class="sxs-lookup"><span data-stu-id="9cf5a-121">SaveOnly</span></span>  <br/> |<span data-ttu-id="9cf5a-122">El elemento de mensaje se guarda en la carpeta especificada por el elemento [SavedItemFolderId](saveditemfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="9cf5a-122">The message item is saved in the folder that is specified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span> <span data-ttu-id="9cf5a-123">Los mensajes se pueden enviar más tarde mediante la [operación SendItem](senditem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="9cf5a-123">Messages can be sent later by using the [SendItem operation](senditem-operation.md).</span></span> <span data-ttu-id="9cf5a-124">Se devuelve un identificador de elemento en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-124">An item identifier is returned in the response.</span></span> <span data-ttu-id="9cf5a-125">Los identificadores de elemento no se devuelven para ningún tipo de elemento excepto para los elementos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-125">Item identifiers are not returned for any item types except for message items.</span></span> <span data-ttu-id="9cf5a-126">Esto incluye los objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-126">This includes response objects.</span></span>  <br/> |
|<span data-ttu-id="9cf5a-127">SendOnly</span><span class="sxs-lookup"><span data-stu-id="9cf5a-127">SendOnly</span></span>  <br/> |<span data-ttu-id="9cf5a-128">El elemento se envía, pero no se guarda ninguna copia en la carpeta elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-128">The item is sent but no copy is saved in the Sent Items folder.</span></span> <span data-ttu-id="9cf5a-129">No se devuelve un identificador de elemento en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-129">An item identifier is not returned in the response.</span></span><br/><br/><span data-ttu-id="9cf5a-130">**Nota**: **CreateItem** no admite el acceso delegado cuando se usa la opción SendOnly porque no se puede especificar una carpeta de destino con esta opción.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-130">**NOTE**: **CreateItem** does not support delegate access when the SendOnly option is used because a destination folder cannot be specified with this option.</span></span> <span data-ttu-id="9cf5a-131">La solución alternativa es crear el elemento, obtener el identificador del elemento y, a continuación, usar la operación SendItem para enviar el elemento.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-131">The workaround is to create the item, get the item identifier, and then use the SendItem operation to send the item.</span></span>           |
|<span data-ttu-id="9cf5a-132">SendAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="9cf5a-132">SendAndSaveCopy</span></span>  <br/> |<span data-ttu-id="9cf5a-133">El elemento se envía y se guarda una copia en la carpeta identificada por el elemento [SavedItemFolderId](saveditemfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="9cf5a-133">The item is sent and a copy is saved in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span> <span data-ttu-id="9cf5a-134">No se devuelve un identificador de elemento en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-134">An item identifier is not returned in the response.</span></span><br/><br/><span data-ttu-id="9cf5a-135">**Nota**: las convocatorias de reunión no se guardan en la carpeta identificada por la propiedad [SavedItemFolderId](saveditemfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="9cf5a-135">**NOTE**: Meeting requests are not saved to the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) property.</span></span> <span data-ttu-id="9cf5a-136">En el caso de los calendarios, la propiedad **SavedItemFolderId** solo puede especificar la ubicación en la que se guardan los elementos del calendario.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-136">For calendaring, only the save location for calendar items can be specified by the **SavedItemFolderId** property.</span></span> <span data-ttu-id="9cf5a-137">No puede controlar dónde se guarda un elemento de convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-137">You cannot control where a meeting request item is saved.</span></span> <span data-ttu-id="9cf5a-138">Solo los elementos de calendario asociados se copian y se guardan en la carpeta identificada por la propiedad **SavedItemFolderId** .</span><span class="sxs-lookup"><span data-stu-id="9cf5a-138">Only the associated calendar items are copied and saved into the folder that is identified by the **SavedItemFolderId** property.</span></span>           |
   
#### <a name="sendmeetinginvitations-attribute"></a><span data-ttu-id="9cf5a-139">Atributo SendMeetingInvitations</span><span class="sxs-lookup"><span data-stu-id="9cf5a-139">SendMeetingInvitations Attribute</span></span>

|<span data-ttu-id="9cf5a-140">Valor</span><span class="sxs-lookup"><span data-stu-id="9cf5a-140">Value</span></span>|<span data-ttu-id="9cf5a-141">Description</span><span class="sxs-lookup"><span data-stu-id="9cf5a-141">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="9cf5a-142">SendToNone</span><span class="sxs-lookup"><span data-stu-id="9cf5a-142">SendToNone</span></span>  <br/> |<span data-ttu-id="9cf5a-143">Si el elemento es una convocatoria de reunión, se guarda como un elemento de calendario pero no se envía.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-143">If the item is a meeting request, it is saved as a calendar item but not sent.</span></span>  <br/> |
|<span data-ttu-id="9cf5a-144">SendOnlyToAll</span><span class="sxs-lookup"><span data-stu-id="9cf5a-144">SendOnlyToAll</span></span>  <br/> |<span data-ttu-id="9cf5a-145">La convocatoria de reunión se envía a todos los asistentes, pero no se guarda en la carpeta elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-145">The meeting request is sent to all attendees but is not saved in the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="9cf5a-146">SendToAllAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="9cf5a-146">SendToAllAndSaveCopy</span></span>  <br/> |<span data-ttu-id="9cf5a-147">La convocatoria de reunión se envía a todos los asistentes y se guarda una copia en la carpeta identificada por el elemento [SavedItemFolderId](saveditemfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="9cf5a-147">The meeting request is sent to all attendees and a copy is saved in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9cf5a-148">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9cf5a-148">Child elements</span></span>

|<span data-ttu-id="9cf5a-149">Elemento</span><span class="sxs-lookup"><span data-stu-id="9cf5a-149">Element</span></span>|<span data-ttu-id="9cf5a-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="9cf5a-150">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9cf5a-151">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="9cf5a-151">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> |<span data-ttu-id="9cf5a-152">Identifica la carpeta de destino en la que se puede crear un nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-152">Identifies the target folder where a new item can be created.</span></span> <span data-ttu-id="9cf5a-153">Si el atributo **MessageDisposition** se establece en SendOnly, solo se enviará un mensaje creado.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-153">If the **MessageDisposition** attribute is set to SendOnly, a created message will only be sent.</span></span> <span data-ttu-id="9cf5a-154">El mensaje no se colocará en la carpeta identificada por el elemento [SavedItemFolderId](saveditemfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="9cf5a-154">The message will not be put in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="9cf5a-155">Elementos (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="9cf5a-155">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="9cf5a-156">Contiene una matriz de elementos que se van a crear en la carpeta identificada por el elemento [SavedItemFolderId](saveditemfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="9cf5a-156">Contains an array of items to create in the folder that is identified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9cf5a-157">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9cf5a-157">Parent elements</span></span>

<span data-ttu-id="9cf5a-158">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-158">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9cf5a-159">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9cf5a-159">Remarks</span></span>

<span data-ttu-id="9cf5a-160">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="9cf5a-160">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9cf5a-161">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9cf5a-161">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9cf5a-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="9cf5a-162">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9cf5a-163">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9cf5a-163">Schema Name</span></span>  <br/> |<span data-ttu-id="9cf5a-164">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="9cf5a-164">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9cf5a-165">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9cf5a-165">Validation File</span></span>  <br/> |<span data-ttu-id="9cf5a-166">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9cf5a-166">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9cf5a-167">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9cf5a-167">Can be Empty</span></span>  <br/> |<span data-ttu-id="9cf5a-168">Falso</span><span class="sxs-lookup"><span data-stu-id="9cf5a-168">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9cf5a-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="9cf5a-169">See also</span></span>

- [<span data-ttu-id="9cf5a-170">CreateItemResponse</span><span class="sxs-lookup"><span data-stu-id="9cf5a-170">CreateItemResponse</span></span>](createitemresponse.md)  
- [<span data-ttu-id="9cf5a-171">Operación CreateItem</span><span class="sxs-lookup"><span data-stu-id="9cf5a-171">CreateItem operation</span></span>](createitem-operation.md)
- [<span data-ttu-id="9cf5a-172">Crear mensajes de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="9cf5a-172">Creating E-mail Messages</span></span>](https://msdn.microsoft.com/library/05bfb83c-2866-427d-a9fe-14ba3cb02793%28Office.15%29.aspx) 
- [<span data-ttu-id="9cf5a-173">Creación de contactos (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="9cf5a-173">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [<span data-ttu-id="9cf5a-174">Creación de tareas</span><span class="sxs-lookup"><span data-stu-id="9cf5a-174">Creating Tasks</span></span>](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx) 
- [<span data-ttu-id="9cf5a-175">Crear citas</span><span class="sxs-lookup"><span data-stu-id="9cf5a-175">Creating Appointments</span></span>](https://msdn.microsoft.com/library/2385391e-c9e7-4d45-b803-c4ff94d5c94e%28Office.15%29.aspx)

