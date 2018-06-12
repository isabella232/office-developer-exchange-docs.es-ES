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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836516"
---
# <a name="newbodycontent"></a><span data-ttu-id="15f0c-103">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="15f0c-103">NewBodyContent</span></span>

<span data-ttu-id="15f0c-104">El elemento **NewBodyContent** representa el nuevo contenido del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="15f0c-104">The **NewBodyContent** element represents the new body content of a message.</span></span> 
  
```xml
<NewBodyContent BodyType=""/>
```

 <span data-ttu-id="15f0c-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="15f0c-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="15f0c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="15f0c-106">Attributes and elements</span></span>

<span data-ttu-id="15f0c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="15f0c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="15f0c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="15f0c-108">Attributes</span></span>

|<span data-ttu-id="15f0c-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="15f0c-109">**Attribute**</span></span>|<span data-ttu-id="15f0c-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="15f0c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="15f0c-111">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="15f0c-111">**BodyType**</span></span> <br/> |<span data-ttu-id="15f0c-112">Representa el contenido real del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="15f0c-112">Represents the actual body content of a message.</span></span>  <br/> |
   
#### <a name="bodytype-attribute"></a><span data-ttu-id="15f0c-113">Atributo BodyType</span><span class="sxs-lookup"><span data-stu-id="15f0c-113">BodyType Attribute</span></span>

|<span data-ttu-id="15f0c-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="15f0c-114">**Value**</span></span>|<span data-ttu-id="15f0c-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="15f0c-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="15f0c-116">**HTML**</span><span class="sxs-lookup"><span data-stu-id="15f0c-116">**HTML**</span></span> <br/> |<span data-ttu-id="15f0c-117">Convierte todos los cuerpos en HTML.</span><span class="sxs-lookup"><span data-stu-id="15f0c-117">Converts all bodies to HTML.</span></span>  <br/> |
|<span data-ttu-id="15f0c-118">**Text**</span><span class="sxs-lookup"><span data-stu-id="15f0c-118">**Text**</span></span> <br/> |<span data-ttu-id="15f0c-119">Todos los cuerpos se convierte en texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="15f0c-119">Converts all bodies to plain text.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="15f0c-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="15f0c-120">Child elements</span></span>

<span data-ttu-id="15f0c-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="15f0c-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="15f0c-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="15f0c-122">Parent elements</span></span>

|<span data-ttu-id="15f0c-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="15f0c-123">**Element**</span></span>|<span data-ttu-id="15f0c-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="15f0c-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15f0c-125">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="15f0c-125">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="15f0c-126">Contiene una respuesta al remitente de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="15f0c-126">Contains a reply to the sender of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="15f0c-127">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="15f0c-127">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="15f0c-128">Contiene una respuesta para el remitente y el identificado todos los destinatarios de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="15f0c-128">Contains a reply to the sender and all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="15f0c-129">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="15f0c-129">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="15f0c-130">Contiene un elemento del almacén de Exchange reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="15f0c-130">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="15f0c-131">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="15f0c-131">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="15f0c-132">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="15f0c-132">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="15f0c-133">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="15f0c-133">PostReplyItem</span></span>](postreplyitem.md) <br/> |<span data-ttu-id="15f0c-134">Contiene una respuesta a un elemento para exponer.</span><span class="sxs-lookup"><span data-stu-id="15f0c-134">Contains a reply to a post item.</span></span> <span data-ttu-id="15f0c-135">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="15f0c-135">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="15f0c-136">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="15f0c-136">Text value</span></span>

<span data-ttu-id="15f0c-137">El valor de texto representa el nuevo contenido del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="15f0c-137">The text value represents the new body content of a message.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="15f0c-138">Notas</span><span class="sxs-lookup"><span data-stu-id="15f0c-138">Remarks</span></span>

<span data-ttu-id="15f0c-139">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del servidor Exchange que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="15f0c-139">The schema that describes this element is located in the EWS virtual directory of the Exchange server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="15f0c-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="15f0c-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="15f0c-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="15f0c-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="15f0c-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="15f0c-142">Schema Name</span></span>  <br/> |<span data-ttu-id="15f0c-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="15f0c-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="15f0c-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="15f0c-144">Validation File</span></span>  <br/> |<span data-ttu-id="15f0c-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="15f0c-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="15f0c-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="15f0c-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="15f0c-147">False</span><span class="sxs-lookup"><span data-stu-id="15f0c-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="15f0c-148">Ver también</span><span class="sxs-lookup"><span data-stu-id="15f0c-148">See also</span></span>



- [<span data-ttu-id="15f0c-149">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="15f0c-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

