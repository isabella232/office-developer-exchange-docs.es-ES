---
title: Tarea
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Task
api_type:
- schema
ms.assetid: 7c84927e-db28-4c5d-b0b5-cbcc2b88d869
description: El elemento de tarea representa una tarea en el almacén de Exchange.
ms.openlocfilehash: 2c61fca6ac85290e34f1365b0cb9e841e1fe279f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840631"
---
# <a name="task"></a><span data-ttu-id="0dfdf-103">Tarea</span><span class="sxs-lookup"><span data-stu-id="0dfdf-103">Task</span></span>

<span data-ttu-id="0dfdf-104">El elemento de **tarea** representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-104">The **Task** element represents a task in the Exchange store.</span></span> 
  
```xml
<Task>
   <MimeContent/>
   <ItemId/>
   <ParentFolderId/>
   <ItemClass/>
   <Subject/>
   <Sensitivity/>
   <Body/>
   <Attachments/>
   <DateTimeReceived/>
   <Size/>
   <Categories/>
   <InReplyTo/>
   <IsSubmitted/>
   <IsDraft/>
   <IsFromMe/>
   <IsResend/>
   <IsUnmodified/>
   <InternetMessageHeaders/>
   <DateTimeSent/>
   <DateTimeCreated/>
   <ResponseObjects/>
   <ReminderDueBy/>
   <ReminderIsSet/>
   <ReminderMinutesBeforeStart/>
   <DisplayCc/>
   <DisplayTo/>
   <HasAttachments/>
   <ExtendedProperty/>
   <Culture/>
   <ActualWork/>
   <AssignedTime/>
   <BillingInformation/>
   <ChangeCount/>
   <Companies/>
   <CompleteDate/>
   <Contacts/>
   <DelegationState/>
   <Delegator/>
   <DueDate/>
   <IsAssignmentEditable/>
   <IsComplete/>
   <IsRecurring/>
   <IsTeamTask/>
   <Mileage/>
   <Owner/>
   <PercentComplete/>
   <Recurrence/>
   <StartDate/>
   <Status/>
   <StatusDescription/>
   <TotalWork/>
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
</Task>
```

<span data-ttu-id="0dfdf-105">**TaskType**</span><span class="sxs-lookup"><span data-stu-id="0dfdf-105">**TaskType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="0dfdf-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0dfdf-106">Attributes and elements</span></span>

<span data-ttu-id="0dfdf-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0dfdf-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0dfdf-108">Attributes</span></span>

<span data-ttu-id="0dfdf-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0dfdf-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0dfdf-110">Child elements</span></span>

|<span data-ttu-id="0dfdf-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0dfdf-111">**Element**</span></span>|<span data-ttu-id="0dfdf-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0dfdf-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0dfdf-113">MimeContent</span><span class="sxs-lookup"><span data-stu-id="0dfdf-113">MimeContent</span></span>](mimecontent.md) <br/> |<span data-ttu-id="0dfdf-114">Contiene la secuencia de extensiones multipropósito de correo Internet (MIME) nativo de un objeto que se representa en formato base64Binary.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-114">Contains the native Multipurpose Internet Mail Extensions (MIME) stream of an object that is represented in base64Binary format.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="0dfdf-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="0dfdf-116">Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-117">Id</span><span class="sxs-lookup"><span data-stu-id="0dfdf-117">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="0dfdf-118">Representa el identificador de la carpeta primaria que contiene el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-118">Represents the identifier of the parent folder that contains the item or folder.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-119">ItemClass</span><span class="sxs-lookup"><span data-stu-id="0dfdf-119">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="0dfdf-120">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-120">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-121">Subject</span><span class="sxs-lookup"><span data-stu-id="0dfdf-121">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="0dfdf-122">Representa al asunto de los elementos del almacén de Exchange y objetos de respuesta.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-122">Represents the subject for Exchange store items and response objects.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-123">Sensibilidad</span><span class="sxs-lookup"><span data-stu-id="0dfdf-123">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="0dfdf-124">Contiene el estado de confidencialidad de un elemento.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-124">Contains the status for an item's sensitivity.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-125">Body</span><span class="sxs-lookup"><span data-stu-id="0dfdf-125">Body</span></span>](body.md) <br/> |<span data-ttu-id="0dfdf-126">Representa el contenido real del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-126">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-127">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="0dfdf-127">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="0dfdf-128">Contiene los elementos o archivos que se adjuntan a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-128">Contains the items or files that are attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-129">DateTimeReceived</span><span class="sxs-lookup"><span data-stu-id="0dfdf-129">DateTimeReceived</span></span>](datetimereceived.md) <br/> |<span data-ttu-id="0dfdf-130">Representa la fecha y hora en que se recibió un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-130">Represents the date and time that an item in a mailbox was received.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-131">Size</span><span class="sxs-lookup"><span data-stu-id="0dfdf-131">Size</span></span>](size.md) <br/> |<span data-ttu-id="0dfdf-132">Representa el tamaño, en bytes, de un elemento.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-132">Represents the size, in bytes, of an item.</span></span> <span data-ttu-id="0dfdf-133">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-133">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-134">Categories</span><span class="sxs-lookup"><span data-stu-id="0dfdf-134">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="0dfdf-135">Representa una colección de cadenas que identifican a qué categorías pertenece un elemento en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-135">Represents a collection of strings that identify to which categories an item in the mailbox belongs.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-136">Importancia</span><span class="sxs-lookup"><span data-stu-id="0dfdf-136">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="0dfdf-137">Describe la importancia de un elemento.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-137">Describes the importance of an item.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-138">InReplyTo</span><span class="sxs-lookup"><span data-stu-id="0dfdf-138">InReplyTo</span></span>](inreplyto.md) <br/> |<span data-ttu-id="0dfdf-139">Representa el identificador del elemento al que este elemento es una respuesta.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-139">Represents the identifier of the item to which this item is a reply.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-140">IsSubmitted</span><span class="sxs-lookup"><span data-stu-id="0dfdf-140">IsSubmitted</span></span>](issubmitted.md) <br/> |<span data-ttu-id="0dfdf-141">Indica si un elemento se ha enviado a la carpeta predeterminada Bandeja de salida.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-141">Indicates whether an item has been submitted to the Outbox default folder.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-142">IsDraft</span><span class="sxs-lookup"><span data-stu-id="0dfdf-142">IsDraft</span></span>](isdraft.md) <br/> |<span data-ttu-id="0dfdf-143">Representa si un elemento aún no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-143">Represents whether an item has not yet been sent.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-144">IsFromMe</span><span class="sxs-lookup"><span data-stu-id="0dfdf-144">IsFromMe</span></span>](isfromme.md) <br/> |<span data-ttu-id="0dfdf-145">Indica si un usuario envía un elemento a él o a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-145">Indicates whether a user sent an item to him or herself.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-146">IsResend</span><span class="sxs-lookup"><span data-stu-id="0dfdf-146">IsResend</span></span>](isresend.md) <br/> |<span data-ttu-id="0dfdf-147">Indica si el elemento se había enviado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-147">Indicates whether the item had previously been sent.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-148">IsUnmodified</span><span class="sxs-lookup"><span data-stu-id="0dfdf-148">IsUnmodified</span></span>](isunmodified.md) <br/> |<span data-ttu-id="0dfdf-149">Indica si el elemento se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-149">Indicates whether the item has been modified.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-150">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="0dfdf-150">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="0dfdf-151">Representa la colección de todos los encabezados de mensaje de Internet que están contenidos en un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-151">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-152">DateTimeSent</span><span class="sxs-lookup"><span data-stu-id="0dfdf-152">DateTimeSent</span></span>](datetimesent.md) <br/> |<span data-ttu-id="0dfdf-153">Representa la fecha y hora en que se envió un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-153">Represents the date and time that an item in a mailbox was sent.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-154">DateTimeCreated</span><span class="sxs-lookup"><span data-stu-id="0dfdf-154">DateTimeCreated</span></span>](datetimecreated.md) <br/> |<span data-ttu-id="0dfdf-155">Representa la fecha y hora en que se creó un elemento determinado en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-155">Represents the date and time that a given item in the mailbox was created.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-156">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="0dfdf-156">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="0dfdf-157">Contiene una colección de todos los objetos de respuesta que están asociados con un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-157">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-158">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="0dfdf-158">ReminderDueBy</span></span>](reminderdueby.md) <br/> |<span data-ttu-id="0dfdf-159">Representa la fecha y hora cuando se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-159">Represents the date and time when the event occurs.</span></span> <span data-ttu-id="0dfdf-160">Esto se usa en el elemento [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) para determinar cuándo se muestra el aviso.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-160">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-161">ReminderIsSet</span><span class="sxs-lookup"><span data-stu-id="0dfdf-161">ReminderIsSet</span></span>](reminderisset.md) <br/> |<span data-ttu-id="0dfdf-162">Indica si se ha establecido un aviso para un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-162">Indicates whether a reminder has been set for an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-163">ReminderMinutesBeforeStart</span><span class="sxs-lookup"><span data-stu-id="0dfdf-163">ReminderMinutesBeforeStart</span></span>](reminderminutesbeforestart.md) <br/> |<span data-ttu-id="0dfdf-164">Representa el número de minutos antes de un evento cuando se muestra un aviso.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-164">Represents the number of minutes before an event when a reminder is displayed.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-165">DisplayCc</span><span class="sxs-lookup"><span data-stu-id="0dfdf-165">DisplayCc</span></span>](displaycc.md) <br/> |<span data-ttu-id="0dfdf-166">Representa la cadena para mostrar que se usa para el contenido del cuadro Cc.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-166">Represents the display string that is used for the contents of the Cc box.</span></span> <span data-ttu-id="0dfdf-167">Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios de Cc.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-167">This is the concatenated string of all Cc recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-168">DisplayTo</span><span class="sxs-lookup"><span data-stu-id="0dfdf-168">DisplayTo</span></span>](displayto.md) <br/> |<span data-ttu-id="0dfdf-169">Representa la cadena para mostrar que se usa para el contenido del cuadro para.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-169">Represents the display string that is used for the contents of the To box.</span></span> <span data-ttu-id="0dfdf-170">Ésta es la cadena concatenada de todos los nombres de presentación de los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-170">This is the concatenated string of all To recipient display names.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-171">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="0dfdf-171">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="0dfdf-172">Representa una propiedad que se establece en **true** si un elemento tiene al menos un dato adjunto visible.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-172">Represents a property that is set to **true** if an item has at least one visible attachment.</span></span> <span data-ttu-id="0dfdf-173">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-173">This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-174">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="0dfdf-174">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="0dfdf-175">Identifica las propiedades extendidas en carpetas y elementos.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-175">Identifies extended properties on folders and items.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-176">Referencia cultural</span><span class="sxs-lookup"><span data-stu-id="0dfdf-176">Culture</span></span>](culture.md) <br/> |<span data-ttu-id="0dfdf-177">Representa la referencia cultural para un elemento determinado en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-177">Represents the culture for a given item in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-178">ActualWork</span><span class="sxs-lookup"><span data-stu-id="0dfdf-178">ActualWork</span></span>](actualwork.md) <br/> |<span data-ttu-id="0dfdf-179">Representa la cantidad real de tiempo que se invierte en una tarea.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-179">Represents the actual amount of time that is spent on a task.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-180">AssignedTime</span><span class="sxs-lookup"><span data-stu-id="0dfdf-180">AssignedTime</span></span>](assignedtime.md) <br/> |<span data-ttu-id="0dfdf-181">Representa el tiempo cuando se asigna una tarea a un contacto.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-181">Represents the time when a task is assigned to a contact.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-182">BillingInformation</span><span class="sxs-lookup"><span data-stu-id="0dfdf-182">BillingInformation</span></span>](billinginformation.md) <br/> |<span data-ttu-id="0dfdf-183">Contiene información para una tarea de facturación.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-183">Holds billing information for a task.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-184">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="0dfdf-184">ChangeCount</span></span>](changecount.md) <br/> |<span data-ttu-id="0dfdf-185">Especifica la versión de la tarea.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-185">Specifies the version of the task.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-186">Empresas</span><span class="sxs-lookup"><span data-stu-id="0dfdf-186">Companies</span></span>](companies.md) <br/> |<span data-ttu-id="0dfdf-187">Representa la colección de las empresas que están asociados con un contacto o una tarea.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-187">Represents the collection of companies that are associated with a contact or task.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-188">CompleteDate</span><span class="sxs-lookup"><span data-stu-id="0dfdf-188">CompleteDate</span></span>](completedate.md) <br/> |<span data-ttu-id="0dfdf-189">Representa la fecha en la que se complete una tarea.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-189">Represents the date on which a task is completed.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-190">Contacts</span><span class="sxs-lookup"><span data-stu-id="0dfdf-190">Contacts</span></span>](contacts-ex15websvcsotherref.md) <br/> |<span data-ttu-id="0dfdf-191">Contiene una lista de contactos que están asociados con una tarea.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-191">Contains a list of contacts that are associated with a task.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-192">DelegationState</span><span class="sxs-lookup"><span data-stu-id="0dfdf-192">DelegationState</span></span>](delegationstate.md) <br/> |<span data-ttu-id="0dfdf-193">Representa el estado de una tarea delegada.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-193">Represents the status of a delegated task.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-194">Delegator</span><span class="sxs-lookup"><span data-stu-id="0dfdf-194">Delegator</span></span>](delegator.md) <br/> |<span data-ttu-id="0dfdf-195">Contiene el nombre del usuario que ha delegado que asignó la tarea.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-195">Contains the name of the delegator who assigned the task.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-196">DueDate</span><span class="sxs-lookup"><span data-stu-id="0dfdf-196">DueDate</span></span>](duedate.md) <br/> |<span data-ttu-id="0dfdf-197">Representa la fecha de vencimiento de un elemento de tarea.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-197">Represents the date when a task item is due.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-198">IsAssignmentEditable</span><span class="sxs-lookup"><span data-stu-id="0dfdf-198">IsAssignmentEditable</span></span>](isassignmenteditable.md) <br/> |<span data-ttu-id="0dfdf-199">Indica si la tarea es modificable o no.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-199">Indicates whether the task is editable or not.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-200">Haya finalizado</span><span class="sxs-lookup"><span data-stu-id="0dfdf-200">IsComplete</span></span>](iscomplete.md) <br/> |<span data-ttu-id="0dfdf-201">Indica si la tarea se ha completado o no.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-201">Indicates whether the task has been completed or not.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-202">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="0dfdf-202">IsRecurring</span></span>](isrecurring.md) <br/> |<span data-ttu-id="0dfdf-203">Indica si una tarea forma parte de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-203">Indicates whether a task is part of a recurring item.</span></span> <span data-ttu-id="0dfdf-204">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-204">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-205">IsTeamTask</span><span class="sxs-lookup"><span data-stu-id="0dfdf-205">IsTeamTask</span></span>](isteamtask.md) <br/> |<span data-ttu-id="0dfdf-206">Indica si la tarea pertenece a un equipo o no.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-206">Indicates whether the task is owned by a team or not.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-207">Kilometraje</span><span class="sxs-lookup"><span data-stu-id="0dfdf-207">Mileage</span></span>](mileage.md) <br/> |<span data-ttu-id="0dfdf-208">Representa mileage para un elemento de tarea.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-208">Represents mileage for a task item.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-209">Propietario</span><span class="sxs-lookup"><span data-stu-id="0dfdf-209">Owner</span></span>](owner.md) <br/> |<span data-ttu-id="0dfdf-210">Representa el propietario de una tarea.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-210">Represents the owner of a task.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-211">PercentComplete</span><span class="sxs-lookup"><span data-stu-id="0dfdf-211">PercentComplete</span></span>](percentcomplete.md) <br/> |<span data-ttu-id="0dfdf-212">Describe el estado de finalización de una tarea.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-212">Describes the completion status of a task.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-213">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="0dfdf-213">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="0dfdf-214">Contiene información sobre la periodicidad para las tareas repetitivas.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-214">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-215">StartDate</span><span class="sxs-lookup"><span data-stu-id="0dfdf-215">StartDate</span></span>](startdate.md) <br/> |<span data-ttu-id="0dfdf-216">Representa la fecha de inicio de un elemento de tarea.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-216">Represents the start date of a task item.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-217">Status</span><span class="sxs-lookup"><span data-stu-id="0dfdf-217">Status</span></span>](status.md) <br/> |<span data-ttu-id="0dfdf-218">Representa el estado de un elemento de tarea.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-218">Represents the status of a task item.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-219">StatusDescription</span><span class="sxs-lookup"><span data-stu-id="0dfdf-219">StatusDescription</span></span>](statusdescription.md) <br/> |<span data-ttu-id="0dfdf-220">Contiene una explicación sobre el estado de la tarea.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-220">Contains an explanation of the task status.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-221">TotalWork</span><span class="sxs-lookup"><span data-stu-id="0dfdf-221">TotalWork</span></span>](totalwork.md) <br/> |<span data-ttu-id="0dfdf-222">Contiene una descripción de la cantidad de trabajo está asociado a un elemento.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-222">Contains a description of how much work is associated with an item.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-223">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="0dfdf-223">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="0dfdf-224">Contiene los derechos del cliente en función de la configuración de permisos para el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-224">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="0dfdf-225">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-225">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-226">LastModifiedName</span><span class="sxs-lookup"><span data-stu-id="0dfdf-226">LastModifiedName</span></span>](lastmodifiedname.md) <br/> |<span data-ttu-id="0dfdf-227">Contiene el nombre para mostrar del último usuario para modificar un elemento.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-227">Contains the display name of the last user to modify an item.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-228">LastModifiedTime</span><span class="sxs-lookup"><span data-stu-id="0dfdf-228">LastModifiedTime</span></span>](lastmodifiedtime.md) <br/> |<span data-ttu-id="0dfdf-229">Indica cuándo se modificó por última vez un elemento.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-229">Indicates when an item was last modified.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-230">IsAssociated</span><span class="sxs-lookup"><span data-stu-id="0dfdf-230">IsAssociated</span></span>](isassociated.md) <br/> |<span data-ttu-id="0dfdf-231">Indica si el elemento está asociado a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-231">Indicates whether the item is associated with a folder.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-232">WebClientReadFormQueryString</span><span class="sxs-lookup"><span data-stu-id="0dfdf-232">WebClientReadFormQueryString</span></span>](webclientreadformquerystring.md) <br/> |<span data-ttu-id="0dfdf-233">Representa una dirección URL a concatene al extremo de Microsoft Office Outlook Web App para leer un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-233">Represents a URL to concatenate to the Microsoft Office Outlook Web App endpoint to read an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-234">WebClientEditFormQueryString</span><span class="sxs-lookup"><span data-stu-id="0dfdf-234">WebClientEditFormQueryString</span></span>](webclienteditformquerystring.md) <br/> |<span data-ttu-id="0dfdf-235">Representa una dirección URL a concatene al extremo de Outlook Web App para editar un elemento en Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-235">Represents a URL to concatenate to the Outlook Web App endpoint to edit an item in Outlook Web App.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-236">ConversationId</span><span class="sxs-lookup"><span data-stu-id="0dfdf-236">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="0dfdf-237">Contiene el identificador de un elemento o conversación.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-237">Contains the identifier of an item or conversation.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-238">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="0dfdf-238">UniqueBody</span></span>](uniquebody.md) <br/> |<span data-ttu-id="0dfdf-239">Representa un fragmento HTML o texto sin formato que representa el cuerpo único de esta conversación.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-239">Represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0dfdf-240">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0dfdf-240">Parent elements</span></span>

|<span data-ttu-id="0dfdf-241">**Element**</span><span class="sxs-lookup"><span data-stu-id="0dfdf-241">**Element**</span></span>|<span data-ttu-id="0dfdf-242">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0dfdf-242">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0dfdf-243">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="0dfdf-243">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> |<span data-ttu-id="0dfdf-244">Describe todos los elementos de calendario que están junto a una hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-244">Describes all calendar items that are adjacent to a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-245">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="0dfdf-245">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="0dfdf-246">Identifica los datos que se anexará a una propiedad única de una carpeta de elemento durante una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="0dfdf-246">Identifies data to append to a single property of an item/folder during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-247">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="0dfdf-247">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> |<span data-ttu-id="0dfdf-248">Identifica todos los elementos que entran en conflicto con un tiempo de la reunión.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-248">Identifies all items that conflict with a meeting time.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-249">Crear (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="0dfdf-249">Create (ItemSync)</span></span>](create-itemsync.md) <br/> |<span data-ttu-id="0dfdf-250">Identifica un solo elemento para crear en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-250">Identifies a single item to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-251">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="0dfdf-251">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="0dfdf-252">Representa un elemento de Exchange que está vinculado a otro elemento de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-252">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-253">Items</span><span class="sxs-lookup"><span data-stu-id="0dfdf-253">Items</span></span>](items.md) <br/> |<span data-ttu-id="0dfdf-254">Contiene una matriz de elementos.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-254">Contains an array of items.</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-255">SetItemField</span><span class="sxs-lookup"><span data-stu-id="0dfdf-255">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="0dfdf-256">Representa una actualización para una única propiedad de un elemento en una [operación de UpdateItem](updateitem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="0dfdf-256">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="0dfdf-257">Actualización (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="0dfdf-257">Update (ItemSync)</span></span>](update-itemsync.md) <br/> |<span data-ttu-id="0dfdf-258">Identifica un solo elemento que se debe actualizar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-258">Identifies a single item to update in the local client store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0dfdf-259">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0dfdf-259">Text value</span></span>

<span data-ttu-id="0dfdf-260">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-260">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0dfdf-261">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0dfdf-261">Remarks</span></span>

<span data-ttu-id="0dfdf-262">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0dfdf-262">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0dfdf-263">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0dfdf-263">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0dfdf-264">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0dfdf-264">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0dfdf-265">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0dfdf-265">Schema name</span></span>  <br/> |<span data-ttu-id="0dfdf-266">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0dfdf-266">Types schema</span></span>  <br/> |
|<span data-ttu-id="0dfdf-267">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0dfdf-267">Validation file</span></span>  <br/> |<span data-ttu-id="0dfdf-268">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0dfdf-268">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0dfdf-269">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0dfdf-269">Can be empty</span></span>  <br/> |<span data-ttu-id="0dfdf-270">False</span><span class="sxs-lookup"><span data-stu-id="0dfdf-270">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0dfdf-271">Ver también</span><span class="sxs-lookup"><span data-stu-id="0dfdf-271">See also</span></span>

- [<span data-ttu-id="0dfdf-272">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0dfdf-272">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="0dfdf-273">Creación de tareas</span><span class="sxs-lookup"><span data-stu-id="0dfdf-273">Creating Tasks</span></span>](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
- [<span data-ttu-id="0dfdf-274">Eliminación de tareas</span><span class="sxs-lookup"><span data-stu-id="0dfdf-274">Deleting Tasks</span></span>](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

