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
description: El elemento CreateAttachment define una solicitud para crear datos adjuntos a un elemento en el almacén de Exchange.
ms.openlocfilehash: 4cba1b8865dae5da58b9617b249a29314c67331a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466440"
---
# <a name="createattachment"></a><span data-ttu-id="5f627-103">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="5f627-103">CreateAttachment</span></span>

<span data-ttu-id="5f627-104">El elemento **CreateAttachment** define una solicitud para crear datos adjuntos a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5f627-104">The **CreateAttachment** element defines a request to create an attachment to an item in the Exchange store.</span></span> 
  
```xml
<CreateAttachment>
   <ParentItemId/>
   <Attachments/>
</CreateAttachment>
```

 <span data-ttu-id="5f627-105">**CreateAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="5f627-105">**CreateAttachmentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5f627-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5f627-106">Attributes and elements</span></span>

<span data-ttu-id="5f627-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5f627-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f627-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5f627-108">Attributes</span></span>

<span data-ttu-id="5f627-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5f627-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5f627-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5f627-110">Child elements</span></span>

|<span data-ttu-id="5f627-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5f627-111">**Element**</span></span>|<span data-ttu-id="5f627-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f627-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f627-113">ParentItemId</span><span class="sxs-lookup"><span data-stu-id="5f627-113">ParentItemId</span></span>](parentitemid.md) <br/> |<span data-ttu-id="5f627-114">Identifica el elemento de almacén de Exchange primario que contiene los datos adjuntos creados.</span><span class="sxs-lookup"><span data-stu-id="5f627-114">Identifies the parent Exchange store item that contains the created attachment.</span></span> <span data-ttu-id="5f627-115">El elemento [ParentItemId](parentitemid.md) debe proporcionar el identificador de un elemento real del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5f627-115">The [ParentItemId](parentitemid.md) element must provide the ID of a real Exchange store item.</span></span> <span data-ttu-id="5f627-116">Los elementos de almacenamiento reales se pueden recuperar mediante la [operación GetItem](getitem-operation.md); los datos adjuntos se recuperan mediante la [operación GetAttachment](getattachment-operation.md).</span><span class="sxs-lookup"><span data-stu-id="5f627-116">Real store items can be retrieved by using the [GetItem operation](getitem-operation.md); attachments are retrieved by using the [GetAttachment operation](getattachment-operation.md).</span></span> <span data-ttu-id="5f627-117">Se produce un error si se pasa el identificador de un archivo adjunto a [ParentItemId](parentitemid.md) .</span><span class="sxs-lookup"><span data-stu-id="5f627-117">An error occurs if the [ParentItemId](parentitemid.md) is passed the ID of a file attachment.</span></span> <span data-ttu-id="5f627-118">Si el [ParentItemId](parentitemid.md) representa el identificador de un dato adjunto del elemento existente, la [operación CreateAttachment](createattachment-operation.md) agrega los nuevos datos adjuntos a los datos adjuntos existentes.</span><span class="sxs-lookup"><span data-stu-id="5f627-118">If the [ParentItemId](parentitemid.md) represents the ID of an existing item attachment, the [CreateAttachment operation](createattachment-operation.md) adds the new attachment to the existing attachment.</span></span>  <br/> <span data-ttu-id="5f627-119">Este elemento es obligatorio para la [operación CreateAttachment](createattachment-operation.md).</span><span class="sxs-lookup"><span data-stu-id="5f627-119">This element is required for the [CreateAttachment operation](createattachment-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="5f627-120">Datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="5f627-120">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5f627-121">Contiene los elementos o archivos que se van a adjuntar a un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5f627-121">Contains the items or files to attach to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5f627-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5f627-122">Parent elements</span></span>

<span data-ttu-id="5f627-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5f627-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f627-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f627-124">Remarks</span></span>

<span data-ttu-id="5f627-125">No existe un elemento adjunto como elemento de almacén.</span><span class="sxs-lookup"><span data-stu-id="5f627-125">An item attachment does not exist as a store item.</span></span> <span data-ttu-id="5f627-126">Sólo existe como datos adjuntos a un elemento u otros datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="5f627-126">It only exists as an attachment to an item or another attachment.</span></span> <span data-ttu-id="5f627-127">Los datos adjuntos de elemento solo se pueden recuperar mediante la solicitud [GetAttachment](getattachment.md) .</span><span class="sxs-lookup"><span data-stu-id="5f627-127">Item attachments can only be retrieved by using the [GetAttachment](getattachment.md) request.</span></span> 
  
<span data-ttu-id="5f627-128">Se pueden crear los siguientes datos adjuntos de elementos:</span><span class="sxs-lookup"><span data-stu-id="5f627-128">The following item attachments can be created:</span></span>
  
- <span data-ttu-id="5f627-129">Elemento</span><span class="sxs-lookup"><span data-stu-id="5f627-129">Item</span></span>
    
- <span data-ttu-id="5f627-130">Mensaje</span><span class="sxs-lookup"><span data-stu-id="5f627-130">Message</span></span>
    
- <span data-ttu-id="5f627-131">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="5f627-131">CalendarItem</span></span>
    
- <span data-ttu-id="5f627-132">Contacto</span><span class="sxs-lookup"><span data-stu-id="5f627-132">Contact</span></span>
    
- <span data-ttu-id="5f627-133">Tarea</span><span class="sxs-lookup"><span data-stu-id="5f627-133">Task</span></span>
    
- <span data-ttu-id="5f627-134">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="5f627-134">MeetingMessage</span></span>
    
- <span data-ttu-id="5f627-135">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="5f627-135">MeetingRequest</span></span>
    
<span data-ttu-id="5f627-136">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="5f627-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="5f627-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5f627-137">Example</span></span>

<span data-ttu-id="5f627-138">En el siguiente ejemplo, se muestra cómo crear y adjuntar un elemento a otro elemento del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5f627-138">The following example shows how to create and attach an item to another item in the Exchange store.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="5f627-139">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5f627-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f627-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f627-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5f627-141">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5f627-141">Schema Name</span></span>  <br/> |<span data-ttu-id="5f627-142">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="5f627-142">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5f627-143">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5f627-143">Validation File</span></span>  <br/> |<span data-ttu-id="5f627-144">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="5f627-144">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5f627-145">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5f627-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="5f627-146">Falso</span><span class="sxs-lookup"><span data-stu-id="5f627-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5f627-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f627-147">See also</span></span>



[<span data-ttu-id="5f627-148">Operación CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="5f627-148">CreateAttachment operation</span></span>](createattachment-operation.md)
  
[<span data-ttu-id="5f627-149">Operación DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="5f627-149">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
  
[<span data-ttu-id="5f627-150">Operación GetAttachment</span><span class="sxs-lookup"><span data-stu-id="5f627-150">GetAttachment operation</span></span>](getattachment-operation.md)

