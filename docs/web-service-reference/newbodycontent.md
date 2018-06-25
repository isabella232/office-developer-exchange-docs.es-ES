---
title: NewBodyContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NewBodyContent
api_type:
- schema
ms.assetid: 0303600d-16d8-4685-88f2-980c5ca7e9a6
description: El elemento NewBodyContent representa el nuevo contenido del cuerpo de un mensaje.
ms.openlocfilehash: b87393e460b1eee1c13efebf38e898d17915bd71
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836516"
---
# <a name="newbodycontent"></a><span data-ttu-id="f930f-103">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="f930f-103">NewBodyContent</span></span>

<span data-ttu-id="f930f-104">El elemento **NewBodyContent** representa el nuevo contenido del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f930f-104">The **NewBodyContent** element represents the new body content of a message.</span></span> 
  
```xml
<NewBodyContent BodyType=""/>
```

 <span data-ttu-id="f930f-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="f930f-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f930f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f930f-106">Attributes and elements</span></span>

<span data-ttu-id="f930f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f930f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f930f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f930f-108">Attributes</span></span>

|<span data-ttu-id="f930f-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f930f-109">**Attribute**</span></span>|<span data-ttu-id="f930f-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f930f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f930f-111">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="f930f-111">**BodyType**</span></span> <br/> |<span data-ttu-id="f930f-112">Representa el contenido real del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f930f-112">Represents the actual body content of a message.</span></span>  <br/> |
   
#### <a name="bodytype-attribute"></a><span data-ttu-id="f930f-113">Atributo BodyType</span><span class="sxs-lookup"><span data-stu-id="f930f-113">BodyType Attribute</span></span>

|<span data-ttu-id="f930f-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f930f-114">**Value**</span></span>|<span data-ttu-id="f930f-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f930f-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f930f-116">**HTML**</span><span class="sxs-lookup"><span data-stu-id="f930f-116">**HTML**</span></span> <br/> |<span data-ttu-id="f930f-117">Convierte todos los cuerpos en HTML.</span><span class="sxs-lookup"><span data-stu-id="f930f-117">Converts all bodies to HTML.</span></span>  <br/> |
|<span data-ttu-id="f930f-118">**Text**</span><span class="sxs-lookup"><span data-stu-id="f930f-118">**Text**</span></span> <br/> |<span data-ttu-id="f930f-119">Todos los cuerpos se convierte en texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="f930f-119">Converts all bodies to plain text.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f930f-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f930f-120">Child elements</span></span>

<span data-ttu-id="f930f-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f930f-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f930f-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f930f-122">Parent elements</span></span>

|<span data-ttu-id="f930f-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="f930f-123">**Element**</span></span>|<span data-ttu-id="f930f-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f930f-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f930f-125">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="f930f-125">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="f930f-126">Contiene una respuesta al remitente de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f930f-126">Contains a reply to the sender of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f930f-127">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="f930f-127">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="f930f-128">Contiene una respuesta para el remitente y el identificado todos los destinatarios de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f930f-128">Contains a reply to the sender and all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f930f-129">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="f930f-129">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="f930f-130">Contiene un elemento del almacén de Exchange reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="f930f-130">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="f930f-131">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="f930f-131">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="f930f-132">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="f930f-132">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="f930f-133">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="f930f-133">PostReplyItem</span></span>](postreplyitem.md) <br/> |<span data-ttu-id="f930f-134">Contiene una respuesta a un elemento para exponer.</span><span class="sxs-lookup"><span data-stu-id="f930f-134">Contains a reply to a post item.</span></span> <span data-ttu-id="f930f-135">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f930f-135">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f930f-136">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f930f-136">Text value</span></span>

<span data-ttu-id="f930f-137">El valor de texto representa el nuevo contenido del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f930f-137">The text value represents the new body content of a message.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f930f-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f930f-138">Remarks</span></span>

<span data-ttu-id="f930f-139">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del servidor Exchange que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="f930f-139">The schema that describes this element is located in the EWS virtual directory of the Exchange server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f930f-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f930f-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f930f-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f930f-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f930f-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f930f-142">Schema Name</span></span>  <br/> |<span data-ttu-id="f930f-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f930f-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="f930f-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f930f-144">Validation File</span></span>  <br/> |<span data-ttu-id="f930f-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f930f-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f930f-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f930f-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="f930f-147">False</span><span class="sxs-lookup"><span data-stu-id="f930f-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f930f-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="f930f-148">See also</span></span>



- [<span data-ttu-id="f930f-149">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f930f-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

