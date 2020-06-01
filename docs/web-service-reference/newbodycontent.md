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
ms.openlocfilehash: dcfa927bb284ff00e510d8c7b4b31910a70b3cbb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466860"
---
# <a name="newbodycontent"></a><span data-ttu-id="e587a-103">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="e587a-103">NewBodyContent</span></span>

<span data-ttu-id="e587a-104">El elemento **NewBodyContent** representa el nuevo contenido del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="e587a-104">The **NewBodyContent** element represents the new body content of a message.</span></span> 
  
```xml
<NewBodyContent BodyType=""/>
```

 <span data-ttu-id="e587a-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="e587a-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e587a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e587a-106">Attributes and elements</span></span>

<span data-ttu-id="e587a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e587a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e587a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e587a-108">Attributes</span></span>

|<span data-ttu-id="e587a-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="e587a-109">**Attribute**</span></span>|<span data-ttu-id="e587a-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e587a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e587a-111">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="e587a-111">**BodyType**</span></span> <br/> |<span data-ttu-id="e587a-112">Representa el contenido del cuerpo real de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="e587a-112">Represents the actual body content of a message.</span></span>  <br/> |
   
#### <a name="bodytype-attribute"></a><span data-ttu-id="e587a-113">Atributo BodyType</span><span class="sxs-lookup"><span data-stu-id="e587a-113">BodyType Attribute</span></span>

|<span data-ttu-id="e587a-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e587a-114">**Value**</span></span>|<span data-ttu-id="e587a-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e587a-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e587a-116">**HTML**</span><span class="sxs-lookup"><span data-stu-id="e587a-116">**HTML**</span></span> <br/> |<span data-ttu-id="e587a-117">Convierte todos los cuerpos en HTML.</span><span class="sxs-lookup"><span data-stu-id="e587a-117">Converts all bodies to HTML.</span></span>  <br/> |
|<span data-ttu-id="e587a-118">**Text**</span><span class="sxs-lookup"><span data-stu-id="e587a-118">**Text**</span></span> <br/> |<span data-ttu-id="e587a-119">Convierte todos los cuerpos en texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="e587a-119">Converts all bodies to plain text.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e587a-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e587a-120">Child elements</span></span>

<span data-ttu-id="e587a-121">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e587a-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e587a-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e587a-122">Parent elements</span></span>

|<span data-ttu-id="e587a-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e587a-123">**Element**</span></span>|<span data-ttu-id="e587a-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e587a-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e587a-125">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="e587a-125">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="e587a-126">Contiene una respuesta al remitente de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e587a-126">Contains a reply to the sender of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e587a-127">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="e587a-127">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="e587a-128">Contiene una respuesta al remitente y a todos los destinatarios identificados de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e587a-128">Contains a reply to the sender and all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e587a-129">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="e587a-129">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="e587a-130">Contiene un elemento de almacén de Exchange que se va a reenviar a los destinatarios.</span><span class="sxs-lookup"><span data-stu-id="e587a-130">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="e587a-131">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="e587a-131">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="e587a-132">Representa el objeto de respuesta que se usa para cancelar una reunión.</span><span class="sxs-lookup"><span data-stu-id="e587a-132">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="e587a-133">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="e587a-133">PostReplyItem</span></span>](postreplyitem.md) <br/> |<span data-ttu-id="e587a-134">Contiene una respuesta a un elemento post.</span><span class="sxs-lookup"><span data-stu-id="e587a-134">Contains a reply to a post item.</span></span> <span data-ttu-id="e587a-135">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e587a-135">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e587a-136">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e587a-136">Text value</span></span>

<span data-ttu-id="e587a-137">El valor de texto representa el nuevo contenido del cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="e587a-137">The text value represents the new body content of a message.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e587a-138">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e587a-138">Remarks</span></span>

<span data-ttu-id="e587a-139">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del servidor de Exchange que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="e587a-139">The schema that describes this element is located in the EWS virtual directory of the Exchange server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e587a-140">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e587a-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e587a-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="e587a-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e587a-142">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e587a-142">Schema Name</span></span>  <br/> |<span data-ttu-id="e587a-143">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e587a-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="e587a-144">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e587a-144">Validation File</span></span>  <br/> |<span data-ttu-id="e587a-145">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e587a-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e587a-146">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e587a-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="e587a-147">Falso</span><span class="sxs-lookup"><span data-stu-id="e587a-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e587a-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="e587a-148">See also</span></span>



- [<span data-ttu-id="e587a-149">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e587a-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

