---
title: FindMailboxStatisticsByKeywords
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cfe0f0ff-5fea-4db8-ac96-a5724c85ed2f
description: El elemento FindMailboxStatisticsByKeywords especifica una solicitud para buscar las estadísticas de buzón de correo por palabra clave.
ms.openlocfilehash: e667f13b66e439dca88d73a5e05d74846183928c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764633"
---
# <a name="findmailboxstatisticsbykeywords"></a><span data-ttu-id="6222c-103">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="6222c-103">FindMailboxStatisticsByKeywords</span></span>

<span data-ttu-id="6222c-104">El elemento **FindMailboxStatisticsByKeywords** especifica una solicitud para buscar las estadísticas de buzón de correo por palabra clave.</span><span class="sxs-lookup"><span data-stu-id="6222c-104">The **FindMailboxStatisticsByKeywords** element specifies a request to search for mailbox statistics by keyword.</span></span> 
  
```XML
<FindMailboxStatisticsByKeywords>
    <Mailboxes/>
    <Keywords/>
    <Language/>
    <Senders/>
    <Recipients/>
    <FromDate/>
    <ToDate/>
    <MessageTypes/>
    <SearchDumpster/>
    <IncludePersonalArchive/>
    <IncludeUnsearchableItems/>
</FindMailboxStatisticsByKeywords>
```

 <span data-ttu-id="6222c-105">**FindMailboxStatisticsByKeywordsType**</span><span class="sxs-lookup"><span data-stu-id="6222c-105">**FindMailboxStatisticsByKeywordsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6222c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6222c-106">Attributes and elements</span></span>

<span data-ttu-id="6222c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6222c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6222c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6222c-108">Attributes</span></span>

<span data-ttu-id="6222c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6222c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6222c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6222c-110">Child elements</span></span>

|<span data-ttu-id="6222c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="6222c-111">**Element**</span></span>|<span data-ttu-id="6222c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6222c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6222c-113">Buzones de correo (ArrayOfUserMailboxesType)</span><span class="sxs-lookup"><span data-stu-id="6222c-113">Mailboxes (ArrayOfUserMailboxesType)</span></span>](mailboxes-arrayofusermailboxestype.md) <br/> |<span data-ttu-id="6222c-114">Contiene una matriz de los buzones afectados por la suspensión.</span><span class="sxs-lookup"><span data-stu-id="6222c-114">Contains an array of mailboxes affected by the hold.</span></span>  <br/> |
|[<span data-ttu-id="6222c-115">Palabras clave</span><span class="sxs-lookup"><span data-stu-id="6222c-115">Keywords</span></span>](keywords-ex15websvcsotherref.md) <br/> |<span data-ttu-id="6222c-116">Especifica las palabras clave para una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6222c-116">Specifies keywords for a search.</span></span>  <br/> |
|[<span data-ttu-id="6222c-117">Idioma</span><span class="sxs-lookup"><span data-stu-id="6222c-117">Language</span></span>](language.md) <br/> |<span data-ttu-id="6222c-118">Contiene el idioma utilizado para la consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6222c-118">Contains the language used for the search query.</span></span>  <br/> |
|[<span data-ttu-id="6222c-119">Remitentes</span><span class="sxs-lookup"><span data-stu-id="6222c-119">Senders</span></span>](senders.md) <br/> |<span data-ttu-id="6222c-120">Especifica una matriz de direcciones SMTP.</span><span class="sxs-lookup"><span data-stu-id="6222c-120">Specifies an array of SMTP addresses.</span></span>  <br/> |
|[<span data-ttu-id="6222c-121">Recipients (ArrayOfSmtpAddressType)</span><span class="sxs-lookup"><span data-stu-id="6222c-121">Recipients (ArrayOfSmtpAddressType)</span></span>](recipients-arrayofsmtpaddresstype.md) <br/> |<span data-ttu-id="6222c-122">Especifica una matriz de destinatarios de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="6222c-122">Specifies an array of recipients of a message.</span></span>  <br/> |
|[<span data-ttu-id="6222c-123">FromDate</span><span class="sxs-lookup"><span data-stu-id="6222c-123">FromDate</span></span>](fromdate.md) <br/> |<span data-ttu-id="6222c-124">Especifica la fecha en que se envió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6222c-124">Specifies the date that the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="6222c-125">ToDate</span><span class="sxs-lookup"><span data-stu-id="6222c-125">ToDate</span></span>](todate.md) <br/> |<span data-ttu-id="6222c-126">Especifica la fecha en que se recibió el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6222c-126">Specifies the date that the message was received.</span></span>  <br/> |
|[<span data-ttu-id="6222c-127">MessageTypes</span><span class="sxs-lookup"><span data-stu-id="6222c-127">MessageTypes</span></span>](messagetypes.md) <br/> |<span data-ttu-id="6222c-128">Especifica una matriz de mensajes para buscar.</span><span class="sxs-lookup"><span data-stu-id="6222c-128">Specifies an array of messages to search.</span></span>  <br/> |
|[<span data-ttu-id="6222c-129">SearchDumpster</span><span class="sxs-lookup"><span data-stu-id="6222c-129">SearchDumpster</span></span>](searchdumpster.md) <br/> |<span data-ttu-id="6222c-130">Especifica si se debe buscar en los elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="6222c-130">Specifies whether to search in deleted items.</span></span>  <br/> |
|[<span data-ttu-id="6222c-131">IncludePersonalArchive</span><span class="sxs-lookup"><span data-stu-id="6222c-131">IncludePersonalArchive</span></span>](includepersonalarchive.md) <br/> |<span data-ttu-id="6222c-132">Especifica si se debe incluir el archivo personal en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6222c-132">Specifies whether to include the personal archive in the search.</span></span>  <br/> |
|[<span data-ttu-id="6222c-133">IncludeUnsearchableItems</span><span class="sxs-lookup"><span data-stu-id="6222c-133">IncludeUnsearchableItems</span></span>](includeunsearchableitems.md) <br/> |<span data-ttu-id="6222c-134">Especifica si se incluyen los elementos que no se puede buscar.</span><span class="sxs-lookup"><span data-stu-id="6222c-134">Specifies whether to include items that cannot be searched.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6222c-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6222c-135">Parent elements</span></span>

<span data-ttu-id="6222c-136">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6222c-136">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6222c-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6222c-137">Remarks</span></span>

<span data-ttu-id="6222c-138">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6222c-138">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6222c-139">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6222c-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6222c-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6222c-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6222c-141">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6222c-141">Schema Name</span></span>  <br/> |<span data-ttu-id="6222c-142">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="6222c-142">Message schema</span></span>  <br/> |
|<span data-ttu-id="6222c-143">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6222c-143">Validation File</span></span>  <br/> |<span data-ttu-id="6222c-144">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6222c-144">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6222c-145">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6222c-145">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="6222c-146">Ver también</span><span class="sxs-lookup"><span data-stu-id="6222c-146">See also</span></span>



- [<span data-ttu-id="6222c-147">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="6222c-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

