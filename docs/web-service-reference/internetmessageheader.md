---
title: InternetMessageHeader
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InternetMessageHeader
api_type:
- schema
ms.assetid: c70675f8-6feb-4c89-ba48-bce0479b308b
description: El elemento InternetMessageHeader representa el encabezado del mensaje de Internet para un determinado encabezado dentro de la colección de encabezados. Para obtener la colección completa de los encabezados de mensaje de Internet, utilice la propiedad PR_TRANSPORT_MESSAGE_HEADERS. Para obtener más información acerca de los encabezados de mensaje EWS y Internet, seeGetting los encabezados de mensaje de Internet en EWS, MIME y los encabezados de mensaje de Internet que faltan.
ms.openlocfilehash: 9457cdabe99c0adcb8183cbc039cc86db881fec7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835952"
---
# <a name="internetmessageheader"></a><span data-ttu-id="b9ea2-105">InternetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="b9ea2-105">InternetMessageHeader</span></span>

<span data-ttu-id="b9ea2-106">El elemento **InternetMessageHeader** representa el encabezado del mensaje de Internet para un determinado encabezado dentro de la colección de encabezados.</span><span class="sxs-lookup"><span data-stu-id="b9ea2-106">The **InternetMessageHeader** element represents the Internet message header for a given header within the headers collection.</span></span> <span data-ttu-id="b9ea2-107">Para obtener la colección completa de los encabezados de mensaje de Internet, utilice la propiedad **PR_TRANSPORT_MESSAGE_HEADERS** .</span><span class="sxs-lookup"><span data-stu-id="b9ea2-107">To get the entire collection of Internet message headers, use the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> <span data-ttu-id="b9ea2-108">Para obtener más información acerca de los encabezados de mensaje EWS y en Internet, vea "encabezados de mensajes de Internet de introducción de [EWS, MIME y los encabezados de mensaje de Internet que faltan](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b9ea2-108">For more information about EWS and Internet message headers, see "Getting Internet message headers in [EWS, MIME, and the missing Internet message headers](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx).</span></span>
  
```XML
<InternetMessageHeader HeaderName=""/>
```

 <span data-ttu-id="b9ea2-109">**InternetHeaderType**</span><span class="sxs-lookup"><span data-stu-id="b9ea2-109">**InternetHeaderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b9ea2-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b9ea2-110">Attributes and elements</span></span>

<span data-ttu-id="b9ea2-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b9ea2-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b9ea2-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="b9ea2-112">Attributes</span></span>

|<span data-ttu-id="b9ea2-113">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="b9ea2-113">**Attribute**</span></span>|<span data-ttu-id="b9ea2-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b9ea2-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b9ea2-115">**HeaderName**</span><span class="sxs-lookup"><span data-stu-id="b9ea2-115">**HeaderName**</span></span> <br/> |<span data-ttu-id="b9ea2-116">Identifica el nombre de encabezado.</span><span class="sxs-lookup"><span data-stu-id="b9ea2-116">Identifies the header name.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b9ea2-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b9ea2-117">Child elements</span></span>

<span data-ttu-id="b9ea2-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b9ea2-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b9ea2-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b9ea2-119">Parent elements</span></span>

|<span data-ttu-id="b9ea2-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="b9ea2-120">**Element**</span></span>|<span data-ttu-id="b9ea2-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b9ea2-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b9ea2-122">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="b9ea2-122">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="b9ea2-123">Representa la colección de todos los encabezados de mensaje de Internet que están contenidos en un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="b9ea2-123">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b9ea2-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b9ea2-124">Text value</span></span>

<span data-ttu-id="b9ea2-125">El valor de texto representa el valor del encabezado.</span><span class="sxs-lookup"><span data-stu-id="b9ea2-125">The text value represents the value for the header.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b9ea2-126">Notas</span><span class="sxs-lookup"><span data-stu-id="b9ea2-126">Remarks</span></span>

<span data-ttu-id="b9ea2-127">La siguiente es la API administrada de EWS extendido definición de propiedad para la propiedad **PR_TRANSPORT_MESSAGE_HEADERS** .</span><span class="sxs-lookup"><span data-stu-id="b9ea2-127">The following is the EWS Managed API extended property definition for the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

<span data-ttu-id="b9ea2-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b9ea2-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b9ea2-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b9ea2-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9ea2-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b9ea2-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b9ea2-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b9ea2-131">Schema Name</span></span>  <br/> |<span data-ttu-id="b9ea2-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b9ea2-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="b9ea2-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b9ea2-133">Validation File</span></span>  <br/> |<span data-ttu-id="b9ea2-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b9ea2-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b9ea2-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b9ea2-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="b9ea2-136">False</span><span class="sxs-lookup"><span data-stu-id="b9ea2-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b9ea2-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="b9ea2-137">See also</span></span>



- [<span data-ttu-id="b9ea2-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b9ea2-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="b9ea2-139">EWS, MIME y los encabezados de mensaje de Internet que faltan</span><span class="sxs-lookup"><span data-stu-id="b9ea2-139">EWS, MIME, and the missing Internet message headers</span></span>](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx)

