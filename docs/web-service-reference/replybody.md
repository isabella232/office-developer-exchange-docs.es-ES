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
description: El elemento ReplyBody contiene un mensaje de fuera de oficina (OOF) y el idioma utilizado para el mensaje.
ms.openlocfilehash: 8400dda1ee810781e129fcc44fd3cd5d6c15cbbe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837116"
---
# <a name="replybody"></a><span data-ttu-id="7cec0-103">ReplyBody</span><span class="sxs-lookup"><span data-stu-id="7cec0-103">ReplyBody</span></span>

<span data-ttu-id="7cec0-104">El elemento **ReplyBody** contiene un mensaje de fuera de oficina (OOF) y el idioma utilizado para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="7cec0-104">The **ReplyBody** element contains an Out of Office (OOF) message and the language used for the message.</span></span> 
  
```XML
<ReplyBody xml:lang="">
   <Message/>
</ReplyBody>
```

 <span data-ttu-id="7cec0-105">**ReplyBody**</span><span class="sxs-lookup"><span data-stu-id="7cec0-105">**ReplyBody**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7cec0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7cec0-106">Attributes and elements</span></span>

<span data-ttu-id="7cec0-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7cec0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7cec0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7cec0-108">Attributes</span></span>

|<span data-ttu-id="7cec0-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7cec0-109">**Attribute**</span></span>|<span data-ttu-id="7cec0-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7cec0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7cec0-111">XML: lang</span><span class="sxs-lookup"><span data-stu-id="7cec0-111">xml:lang</span></span>  <br/> |<span data-ttu-id="7cec0-112">Especifica el lenguaje utilizado en el contenido de **ReplyBody** .</span><span class="sxs-lookup"><span data-stu-id="7cec0-112">Specifies the language used in the **ReplyBody** contents.</span></span> <span data-ttu-id="7cec0-113">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="7cec0-113">This attribute is optional.</span></span> <span data-ttu-id="7cec0-114">Los valores posibles de este atributo se definen en IETF RFC 3066.</span><span class="sxs-lookup"><span data-stu-id="7cec0-114">The possible values of this attribute are defined by IETF RFC 3066.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7cec0-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7cec0-115">Child elements</span></span>

|<span data-ttu-id="7cec0-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="7cec0-116">**Element**</span></span>|<span data-ttu-id="7cec0-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7cec0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7cec0-118">Mensaje (disponibilidad)</span><span class="sxs-lookup"><span data-stu-id="7cec0-118">Message (Availability)</span></span>](message-availability.md) <br/> |<span data-ttu-id="7cec0-119">Contiene la espera de respuesta de la oficina (OOF).</span><span class="sxs-lookup"><span data-stu-id="7cec0-119">Contains the out of office (OOF) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7cec0-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7cec0-120">Parent elements</span></span>

|<span data-ttu-id="7cec0-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="7cec0-121">**Element**</span></span>|<span data-ttu-id="7cec0-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7cec0-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7cec0-123">Fuera de la oficina</span><span class="sxs-lookup"><span data-stu-id="7cec0-123">OutOfOffice</span></span>](outofoffice.md) <br/> |<span data-ttu-id="7cec0-124">Define el mensaje de respuesta de fuera de la oficina y un tiempo de duración para enviar el mensaje de respuesta para un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="7cec0-124">Defines the OOF response message and a duration time for sending the response message for a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7cec0-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7cec0-125">Text value</span></span>

<span data-ttu-id="7cec0-126">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7cec0-126">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7cec0-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7cec0-127">Remarks</span></span>

<span data-ttu-id="7cec0-128">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="7cec0-128">This element is required.</span></span>
  
<span data-ttu-id="7cec0-129">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7cec0-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7cec0-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7cec0-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7cec0-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7cec0-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7cec0-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7cec0-132">Schema Name</span></span>  <br/> |<span data-ttu-id="7cec0-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7cec0-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="7cec0-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7cec0-134">Validation File</span></span>  <br/> |<span data-ttu-id="7cec0-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7cec0-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7cec0-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7cec0-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="7cec0-137">False</span><span class="sxs-lookup"><span data-stu-id="7cec0-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7cec0-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="7cec0-138">See also</span></span>



- [<span data-ttu-id="7cec0-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7cec0-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

