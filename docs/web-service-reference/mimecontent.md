---
title: MimeContent
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MimeContent
api_type:
- schema
ms.assetid: 4f472a08-5653-4c54-ba65-831dfe32f20f
description: El elemento MimeContent contiene la secuencia ASCII MIME de un objeto que se representa en formato base64Binary y es compatible con [RFC2045].
ms.openlocfilehash: 60f2d42f09347611559137c494d93036f1192829
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836465"
---
# <a name="mimecontent"></a><span data-ttu-id="28c66-103">MimeContent</span><span class="sxs-lookup"><span data-stu-id="28c66-103">MimeContent</span></span>

<span data-ttu-id="28c66-104">El elemento **MimeContent** contiene la secuencia ASCII MIME de un objeto que se representa en formato base64Binary y es compatible con [[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt).</span><span class="sxs-lookup"><span data-stu-id="28c66-104">The **MimeContent** element contains the ASCII MIME stream of an object that is represented in base64Binary format and supports [[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt).</span></span>
  
```xml
<MimeContent CharacterSet="" />
```

 <span data-ttu-id="28c66-105">**MimeContentType**</span><span class="sxs-lookup"><span data-stu-id="28c66-105">**MimeContentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="28c66-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="28c66-106">Attributes and elements</span></span>

<span data-ttu-id="28c66-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="28c66-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28c66-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="28c66-108">Attributes</span></span>

|<span data-ttu-id="28c66-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="28c66-109">**Attribute**</span></span>|<span data-ttu-id="28c66-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="28c66-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="28c66-111">**Conjunto de caracteres**</span><span class="sxs-lookup"><span data-stu-id="28c66-111">**CharacterSet**</span></span> <br/> |<span data-ttu-id="28c66-112">Si se establece, el valor para este atributo se omite el servidor.</span><span class="sxs-lookup"><span data-stu-id="28c66-112">If set, the value for this attribute is ignored by the server.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="28c66-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="28c66-113">Child elements</span></span>

<span data-ttu-id="28c66-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="28c66-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="28c66-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="28c66-115">Parent elements</span></span>

<span data-ttu-id="28c66-116">[CalendarItem](calendaritem.md) | [contacto](contact.md) | [DistributionList](distributionlist.md) | [elemento](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md)  |  [ MeetingResponse](meetingresponse.md) | [mensaje](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [tarea](task.md)</span><span class="sxs-lookup"><span data-stu-id="28c66-116">[CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Item](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [Message](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="28c66-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="28c66-117">Text value</span></span>

<span data-ttu-id="28c66-118">Un valor de texto que representa una secuencia MIME base64Binary es necesario si se usa este elemento.</span><span class="sxs-lookup"><span data-stu-id="28c66-118">A text value that represents a base64Binary MIME stream is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="28c66-119">Notas</span><span class="sxs-lookup"><span data-stu-id="28c66-119">Remarks</span></span>

<span data-ttu-id="28c66-120">El contenido del mensaje circula a través de los tres niveles siguientes de codificación antes de que se almacene en el valor de **MimeContent** :</span><span class="sxs-lookup"><span data-stu-id="28c66-120">The message content goes through the following three levels of encoding before it is stored in the **MimeContent** value:</span></span> 
  
1. <span data-ttu-id="28c66-121">Texto del mensaje: este es el cuerpo de la codificación, como iso-2022-jp para caracteres en japonés.</span><span class="sxs-lookup"><span data-stu-id="28c66-121">Message text — This is the body encoding, such as iso-2022-jp for Japanese characters.</span></span>
    
2. <span data-ttu-id="28c66-122">Secuencia MIME: se trata de la codificación ASCII del texto del mensaje para el elemento de **MimeContent** o la codificación UTF8 del texto del mensaje para el elemento [MimeContentUTF8](mimecontentutf8.md) .</span><span class="sxs-lookup"><span data-stu-id="28c66-122">MIME stream — This is the ASCII encoding of the message text for the **MimeContent** element, or the UTF8 encoding of the message text for the [MimeContentUTF8](mimecontentutf8.md) element.</span></span> 
    
3. <span data-ttu-id="28c66-123">Documento XML — siempre es la secuencia de ASCII con codificación base64 de la secuencia MIME, donde caracteres como '\<', que son significativas para XML, están ocultos de los analizadores XML.</span><span class="sxs-lookup"><span data-stu-id="28c66-123">XML document — This is always the base64-encoded ASCII stream of the MIME stream, where characters such as '\<', which are meaningful to XML, are hidden from XML parsers.</span></span>
    
<span data-ttu-id="28c66-124">Cada nivel es independiente del nivel que le precede.</span><span class="sxs-lookup"><span data-stu-id="28c66-124">Each level is independent of the level that precedes it.</span></span>
  
<span data-ttu-id="28c66-125">El elemento **MimeContent** podría contener los mismos datos que contienen otras propiedades que se devuelven con un elemento.</span><span class="sxs-lookup"><span data-stu-id="28c66-125">The **MimeContent** element might contain the same data that other properties that are returned with an item contain.</span></span> 
  
<span data-ttu-id="28c66-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="28c66-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="28c66-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="28c66-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28c66-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="28c66-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="28c66-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="28c66-129">Schema Name</span></span>  <br/> |<span data-ttu-id="28c66-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="28c66-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="28c66-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="28c66-131">Validation File</span></span>  <br/> |<span data-ttu-id="28c66-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="28c66-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="28c66-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="28c66-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="28c66-134">False</span><span class="sxs-lookup"><span data-stu-id="28c66-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28c66-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="28c66-135">See also</span></span>



- [<span data-ttu-id="28c66-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="28c66-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

