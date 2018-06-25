---
title: CreateAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAttachment
api_type:
- schema
ms.assetid: e33b403a-b7d3-48ee-8d24-6b7abf0d70bc
description: El elemento CreateAttachment define una solicitud para crear un archivo adjunto a un elemento en el almacén de Exchange.
ms.openlocfilehash: d403eb5ca15623d3a973f7b224dbcde5529cf1bc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763915"
---
# <a name="createattachment"></a><span data-ttu-id="df403-103">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="df403-103">CreateAttachment</span></span>

<span data-ttu-id="df403-104">El elemento **CreateAttachment** define una solicitud para crear un archivo adjunto a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="df403-104">The **CreateAttachment** element defines a request to create an attachment to an item in the Exchange store.</span></span> 
  
```xml
<CreateAttachment>
   <ParentItemId/>
   <Attachments/>
</CreateAttachment>
```

 <span data-ttu-id="df403-105">**CreateAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="df403-105">**CreateAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="df403-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="df403-106">Attributes and elements</span></span>

<span data-ttu-id="df403-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="df403-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="df403-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="df403-108">Attributes</span></span>

<span data-ttu-id="df403-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="df403-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="df403-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="df403-110">Child elements</span></span>

|<span data-ttu-id="df403-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="df403-111">**Element**</span></span>|<span data-ttu-id="df403-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="df403-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="df403-113">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="df403-113">ParentItemId</span></span>](parentitemid.md) <br/> |<span data-ttu-id="df403-114">Identifica el elemento primario del almacén de Exchange que contiene los datos adjuntos creado.</span><span class="sxs-lookup"><span data-stu-id="df403-114">Identifies the parent Exchange store item that contains the created attachment.</span></span> <span data-ttu-id="df403-115">El elemento [ParentItemId](parentitemid.md) debe proporcionar el identificador de un intercambio real almacenar el elemento.</span><span class="sxs-lookup"><span data-stu-id="df403-115">The [ParentItemId](parentitemid.md) element must provide the ID of a real Exchange store item.</span></span> <span data-ttu-id="df403-116">Artículos de la tienda real se pueden recuperar mediante el uso de la [operación GetItem](getitem-operation.md); los datos adjuntos se recuperan mediante el uso de la [operación GetAttachment](getattachment-operation.md).</span><span class="sxs-lookup"><span data-stu-id="df403-116">Real store items can be retrieved by using the [GetItem operation](getitem-operation.md); attachments are retrieved by using the [GetAttachment operation](getattachment-operation.md).</span></span> <span data-ttu-id="df403-117">Se produce un error si el [ParentItemId](parentitemid.md) se pasa el identificador de un archivo adjunto.</span><span class="sxs-lookup"><span data-stu-id="df403-117">An error occurs if the [ParentItemId](parentitemid.md) is passed the ID of a file attachment.</span></span> <span data-ttu-id="df403-118">Si el [ParentItemId](parentitemid.md) representa el identificador de datos adjuntos de elemento existente, la [operación CreateAttachment](createattachment-operation.md) agrega los nuevos datos adjuntos a los datos adjuntos existentes.</span><span class="sxs-lookup"><span data-stu-id="df403-118">If the [ParentItemId](parentitemid.md) represents the ID of an existing item attachment, the [CreateAttachment operation](createattachment-operation.md) adds the new attachment to the existing attachment.</span></span>  <br/> <span data-ttu-id="df403-119">Este elemento es necesario para la [operación CreateAttachment](createattachment-operation.md).</span><span class="sxs-lookup"><span data-stu-id="df403-119">This element is required for the [CreateAttachment operation](createattachment-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="df403-120">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="df403-120">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="df403-121">Contiene los elementos o archivos para adjuntar a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="df403-121">Contains the items or files to attach to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="df403-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="df403-122">Parent elements</span></span>

<span data-ttu-id="df403-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="df403-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="df403-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="df403-124">Remarks</span></span>

<span data-ttu-id="df403-125">Un elemento de los datos adjuntos no existe como un elemento del almacén.</span><span class="sxs-lookup"><span data-stu-id="df403-125">An item attachment does not exist as a store item.</span></span> <span data-ttu-id="df403-126">Sólo existe como datos adjuntos a un elemento o en otro objeto attachment.</span><span class="sxs-lookup"><span data-stu-id="df403-126">It only exists as an attachment to an item or another attachment.</span></span> <span data-ttu-id="df403-127">Datos adjuntos de elemento sólo se pueden recuperar mediante el uso de la solicitud de [GetAttachment](getattachment.md) .</span><span class="sxs-lookup"><span data-stu-id="df403-127">Item attachments can only be retrieved by using the [GetAttachment](getattachment.md) request.</span></span> 
  
<span data-ttu-id="df403-128">Pueden crearse los siguientes datos adjuntos de elemento:</span><span class="sxs-lookup"><span data-stu-id="df403-128">The following item attachments can be created:</span></span>
  
- <span data-ttu-id="df403-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="df403-129">Item</span></span>
    
- <span data-ttu-id="df403-130">Message</span><span class="sxs-lookup"><span data-stu-id="df403-130">Message</span></span>
    
- <span data-ttu-id="df403-131">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="df403-131">CalendarItem</span></span>
    
- <span data-ttu-id="df403-132">Contacto</span><span class="sxs-lookup"><span data-stu-id="df403-132">Contact</span></span>
    
- <span data-ttu-id="df403-133">Tarea</span><span class="sxs-lookup"><span data-stu-id="df403-133">Task</span></span>
    
- <span data-ttu-id="df403-134">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="df403-134">MeetingMessage</span></span>
    
- <span data-ttu-id="df403-135">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="df403-135">MeetingRequest</span></span>
    
<span data-ttu-id="df403-136">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="df403-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="df403-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="df403-137">Example</span></span>

<span data-ttu-id="df403-138">En el ejemplo siguiente se muestra cómo crear y adjuntar un elemento a otro elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="df403-138">The following example shows how to create and attach an item to another item in the Exchange store.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <ParentItemId Id="ASkAS"/>
      <Attachments>
        <t:ItemAttachment>
          <t:Name>MyAttachment</t:Name>
          <t:Message>
            <t:ItemClass>IPM>Note</t:ItemClass>
            <t:Subject>My attachment subject</t:Subject>
            <t:Body BodyType="Text">My attachment body</t:Body>
          </t:Message>
        </t:ItemAttachment>
      </Attachments>
    </CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="df403-139">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="df403-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df403-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="df403-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="df403-141">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="df403-141">Schema Name</span></span>  <br/> |<span data-ttu-id="df403-142">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="df403-142">Messages schema</span></span>  <br/> |
|<span data-ttu-id="df403-143">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="df403-143">Validation File</span></span>  <br/> |<span data-ttu-id="df403-144">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="df403-144">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="df403-145">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="df403-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="df403-146">False</span><span class="sxs-lookup"><span data-stu-id="df403-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df403-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="df403-147">See also</span></span>



[<span data-ttu-id="df403-148">Operación CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="df403-148">CreateAttachment operation</span></span>](createattachment-operation.md)
  
[<span data-ttu-id="df403-149">Operación DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="df403-149">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
  
[<span data-ttu-id="df403-150">Operación GetAttachment</span><span class="sxs-lookup"><span data-stu-id="df403-150">GetAttachment operation</span></span>](getattachment-operation.md)

