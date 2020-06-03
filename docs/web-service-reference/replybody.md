---
title: ReplyBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReplyBody
api_type:
- schema
ms.assetid: bb184144-3e4b-4419-a883-cc9fab1085e6
description: El elemento ReplyBody contiene un mensaje de fuera de la oficina (OOF) y el idioma usado para el mensaje.
ms.openlocfilehash: 496d336d1f87d9ea493ba7da362eef5a416fd899
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465306"
---
# <a name="replybody"></a><span data-ttu-id="06237-103">ReplyBody</span><span class="sxs-lookup"><span data-stu-id="06237-103">ReplyBody</span></span>

<span data-ttu-id="06237-104">El elemento **ReplyBody** contiene un mensaje de fuera de la oficina (OOF) y el idioma usado para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="06237-104">The **ReplyBody** element contains an Out of Office (OOF) message and the language used for the message.</span></span> 
  
```XML
<ReplyBody xml:lang="">
   <Message/>
</ReplyBody>
```

 <span data-ttu-id="06237-105">**ReplyBody**</span><span class="sxs-lookup"><span data-stu-id="06237-105">**ReplyBody**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="06237-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="06237-106">Attributes and elements</span></span>

<span data-ttu-id="06237-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="06237-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06237-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="06237-108">Attributes</span></span>

|<span data-ttu-id="06237-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="06237-109">**Attribute**</span></span>|<span data-ttu-id="06237-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="06237-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="06237-111">XML: lang</span><span class="sxs-lookup"><span data-stu-id="06237-111">xml:lang</span></span>  <br/> |<span data-ttu-id="06237-112">Especifica el idioma usado en el contenido de **ReplyBody** .</span><span class="sxs-lookup"><span data-stu-id="06237-112">Specifies the language used in the **ReplyBody** contents.</span></span> <span data-ttu-id="06237-113">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="06237-113">This attribute is optional.</span></span> <span data-ttu-id="06237-114">Los valores posibles de este atributo los define el documento RFC 3066 de IETF.</span><span class="sxs-lookup"><span data-stu-id="06237-114">The possible values of this attribute are defined by IETF RFC 3066.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="06237-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="06237-115">Child elements</span></span>

|<span data-ttu-id="06237-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="06237-116">**Element**</span></span>|<span data-ttu-id="06237-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="06237-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06237-118">Mensaje (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="06237-118">Message (Availability)</span></span>](message-availability.md) <br/> |<span data-ttu-id="06237-119">Contiene la respuesta de fuera de la oficina (OOF).</span><span class="sxs-lookup"><span data-stu-id="06237-119">Contains the out of office (OOF) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="06237-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="06237-120">Parent elements</span></span>

|<span data-ttu-id="06237-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="06237-121">**Element**</span></span>|<span data-ttu-id="06237-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="06237-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="06237-123">Oficina</span><span class="sxs-lookup"><span data-stu-id="06237-123">OutOfOffice</span></span>](outofoffice.md) <br/> |<span data-ttu-id="06237-124">Define el mensaje de respuesta OOF y un tiempo de duración para enviar el mensaje de respuesta de un buzón.</span><span class="sxs-lookup"><span data-stu-id="06237-124">Defines the OOF response message and a duration time for sending the response message for a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="06237-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="06237-125">Text value</span></span>

<span data-ttu-id="06237-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="06237-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="06237-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="06237-127">Remarks</span></span>

<span data-ttu-id="06237-128">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="06237-128">This element is required.</span></span>
  
<span data-ttu-id="06237-129">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="06237-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="06237-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="06237-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06237-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="06237-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="06237-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="06237-132">Schema Name</span></span>  <br/> |<span data-ttu-id="06237-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="06237-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="06237-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="06237-134">Validation File</span></span>  <br/> |<span data-ttu-id="06237-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="06237-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="06237-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="06237-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="06237-137">Falso</span><span class="sxs-lookup"><span data-stu-id="06237-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="06237-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="06237-138">See also</span></span>



- [<span data-ttu-id="06237-139">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="06237-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

