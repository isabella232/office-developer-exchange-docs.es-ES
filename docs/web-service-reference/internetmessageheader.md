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
description: El elemento InternetMessageHeader representa el encabezado de un mensaje de Internet para un encabezado determinado dentro de la colección de encabezados. Para obtener toda la colección de encabezados de mensajes de Internet, use la propiedad PR_TRANSPORT_MESSAGE_HEADERS. Para obtener más información acerca de los encabezados de mensajes de Internet y EWS, Consulteobtener los encabezados de mensajes de Internet en EWS, MIME y los encabezados de mensajes de Internet que faltan.
ms.openlocfilehash: 7b662617e0b1a1fcdcce3449b729485ba6e0956b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459310"
---
# <a name="internetmessageheader"></a><span data-ttu-id="4ce12-105">InternetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="4ce12-105">InternetMessageHeader</span></span>

<span data-ttu-id="4ce12-106">El elemento **InternetMessageHeader** representa el encabezado de un mensaje de Internet para un encabezado determinado dentro de la colección de encabezados.</span><span class="sxs-lookup"><span data-stu-id="4ce12-106">The **InternetMessageHeader** element represents the Internet message header for a given header within the headers collection.</span></span> <span data-ttu-id="4ce12-107">Para obtener toda la colección de encabezados de mensajes de Internet, use la propiedad **PR_TRANSPORT_MESSAGE_HEADERS** .</span><span class="sxs-lookup"><span data-stu-id="4ce12-107">To get the entire collection of Internet message headers, use the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> <span data-ttu-id="4ce12-108">Para obtener más información acerca de los encabezados de mensajes de Internet y EWS, consulte "obtener encabezados de mensajes de Internet en [EWS, MIME y los encabezados de mensajes de Internet que faltan](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4ce12-108">For more information about EWS and Internet message headers, see "Getting Internet message headers in [EWS, MIME, and the missing Internet message headers](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx).</span></span>
  
```XML
<InternetMessageHeader HeaderName=""/>
```

 <span data-ttu-id="4ce12-109">**InternetHeaderType**</span><span class="sxs-lookup"><span data-stu-id="4ce12-109">**InternetHeaderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4ce12-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4ce12-110">Attributes and elements</span></span>

<span data-ttu-id="4ce12-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4ce12-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ce12-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="4ce12-112">Attributes</span></span>

|<span data-ttu-id="4ce12-113">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="4ce12-113">**Attribute**</span></span>|<span data-ttu-id="4ce12-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4ce12-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4ce12-115">**HeaderName**</span><span class="sxs-lookup"><span data-stu-id="4ce12-115">**HeaderName**</span></span> <br/> |<span data-ttu-id="4ce12-116">Identifica el nombre del encabezado.</span><span class="sxs-lookup"><span data-stu-id="4ce12-116">Identifies the header name.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4ce12-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4ce12-117">Child elements</span></span>

<span data-ttu-id="4ce12-118">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4ce12-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4ce12-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4ce12-119">Parent elements</span></span>

|<span data-ttu-id="4ce12-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4ce12-120">**Element**</span></span>|<span data-ttu-id="4ce12-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4ce12-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ce12-122">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="4ce12-122">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="4ce12-123">Representa la colección de todos los encabezados de mensajes de Internet que contiene un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="4ce12-123">Represents the collection of all Internet message headers that are contained in an item in a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4ce12-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4ce12-124">Text value</span></span>

<span data-ttu-id="4ce12-125">El valor de texto representa el valor del encabezado.</span><span class="sxs-lookup"><span data-stu-id="4ce12-125">The text value represents the value for the header.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4ce12-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ce12-126">Remarks</span></span>

<span data-ttu-id="4ce12-127">La siguiente es la definición de propiedad extendida de la API administrada de EWS para la propiedad **PR_TRANSPORT_MESSAGE_HEADERS** .</span><span class="sxs-lookup"><span data-stu-id="4ce12-127">The following is the EWS Managed API extended property definition for the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

<span data-ttu-id="4ce12-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="4ce12-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4ce12-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4ce12-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ce12-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ce12-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4ce12-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4ce12-131">Schema Name</span></span>  <br/> |<span data-ttu-id="4ce12-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="4ce12-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="4ce12-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4ce12-133">Validation File</span></span>  <br/> |<span data-ttu-id="4ce12-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="4ce12-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4ce12-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4ce12-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="4ce12-136">Falso</span><span class="sxs-lookup"><span data-stu-id="4ce12-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4ce12-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ce12-137">See also</span></span>



- [<span data-ttu-id="4ce12-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4ce12-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="4ce12-139">EWS, MIME y los encabezados de mensajes de Internet que faltan</span><span class="sxs-lookup"><span data-stu-id="4ce12-139">EWS, MIME, and the missing Internet message headers</span></span>](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)

