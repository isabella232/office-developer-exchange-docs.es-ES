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
description: El elemento MimeContent contiene la secuencia MIME ASCII de un objeto representado en formato base64Binary y compatible con [RFC2045].
ms.openlocfilehash: 039ef1245d48e4cf13141970921dd210f4bd7d06
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530439"
---
# <a name="mimecontent"></a><span data-ttu-id="82c81-103">MimeContent</span><span class="sxs-lookup"><span data-stu-id="82c81-103">MimeContent</span></span>

<span data-ttu-id="82c81-104">El elemento **MimeContent** contiene la secuencia MIME ASCII de un objeto representado en formato base64Binary y compatible con [[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt).</span><span class="sxs-lookup"><span data-stu-id="82c81-104">The **MimeContent** element contains the ASCII MIME stream of an object that is represented in base64Binary format and supports [[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt).</span></span>
  
```xml
<MimeContent CharacterSet="" />
```

 <span data-ttu-id="82c81-105">**MimeContentType**</span><span class="sxs-lookup"><span data-stu-id="82c81-105">**MimeContentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="82c81-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="82c81-106">Attributes and elements</span></span>

<span data-ttu-id="82c81-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="82c81-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82c81-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="82c81-108">Attributes</span></span>

|<span data-ttu-id="82c81-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="82c81-109">**Attribute**</span></span>|<span data-ttu-id="82c81-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="82c81-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="82c81-111">**CharacterSet**</span><span class="sxs-lookup"><span data-stu-id="82c81-111">**CharacterSet**</span></span> <br/> |<span data-ttu-id="82c81-112">Si se establece, el valor de este atributo es ignorado por el servidor.</span><span class="sxs-lookup"><span data-stu-id="82c81-112">If set, the value for this attribute is ignored by the server.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="82c81-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="82c81-113">Child elements</span></span>

<span data-ttu-id="82c81-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="82c81-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="82c81-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="82c81-115">Parent elements</span></span>

<span data-ttu-id="82c81-116">[CalendarItem](calendaritem.md)  |  [Contacto](contact.md)  |  [DistributionList](distributionlist.md)  |  [Elemento](item.md)  |  [MeetingCancellation](meetingcancellation.md)  |  [MeetingMessage](meetingmessage.md)  |  Propiedad [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md)  |  [Mensaje de error](message-ex15websvcsotherref.md)  |  [RemoveItem](removeitem.md)  |  [Tarea](task.md)</span><span class="sxs-lookup"><span data-stu-id="82c81-116">[CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Item](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [Message](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="82c81-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="82c81-117">Text value</span></span>

<span data-ttu-id="82c81-118">Si se usa este elemento, se necesita un valor de texto que represente una secuencia MIME base64Binary.</span><span class="sxs-lookup"><span data-stu-id="82c81-118">A text value that represents a base64Binary MIME stream is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="82c81-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="82c81-119">Remarks</span></span>

<span data-ttu-id="82c81-120">El contenido del mensaje pasa por los tres niveles siguientes de codificación antes de almacenarse en el valor **MimeContent** :</span><span class="sxs-lookup"><span data-stu-id="82c81-120">The message content goes through the following three levels of encoding before it is stored in the **MimeContent** value:</span></span> 
  
1. <span data-ttu-id="82c81-121">Texto del mensaje: esta es la codificación del cuerpo, como ISO-2022-JP para caracteres japoneses.</span><span class="sxs-lookup"><span data-stu-id="82c81-121">Message text — This is the body encoding, such as iso-2022-jp for Japanese characters.</span></span>
    
2. <span data-ttu-id="82c81-122">Secuencia MIME: es la codificación ASCII del texto del mensaje para el elemento **MimeContent** , o la codificación UTF8 del texto del mensaje para el elemento [MimeContentUTF8](mimecontentutf8.md) .</span><span class="sxs-lookup"><span data-stu-id="82c81-122">MIME stream — This is the ASCII encoding of the message text for the **MimeContent** element, or the UTF8 encoding of the message text for the [MimeContentUTF8](mimecontentutf8.md) element.</span></span> 
    
3. <span data-ttu-id="82c81-123">Documento XML: siempre es la secuencia ASCII codificada en Base64 de la secuencia MIME, donde los caracteres como ' \< ', que son significativos para XML, están ocultos a los analizadores XML.</span><span class="sxs-lookup"><span data-stu-id="82c81-123">XML document — This is always the base64-encoded ASCII stream of the MIME stream, where characters such as '\<', which are meaningful to XML, are hidden from XML parsers.</span></span>
    
<span data-ttu-id="82c81-124">Cada nivel es independiente del nivel que le precede.</span><span class="sxs-lookup"><span data-stu-id="82c81-124">Each level is independent of the level that precedes it.</span></span>
  
<span data-ttu-id="82c81-125">El elemento **MimeContent** puede contener los mismos datos que contienen otras propiedades que se devuelven con un elemento.</span><span class="sxs-lookup"><span data-stu-id="82c81-125">The **MimeContent** element might contain the same data that other properties that are returned with an item contain.</span></span> 
  
<span data-ttu-id="82c81-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="82c81-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="82c81-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="82c81-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82c81-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="82c81-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="82c81-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="82c81-129">Schema Name</span></span>  <br/> |<span data-ttu-id="82c81-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="82c81-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="82c81-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="82c81-131">Validation File</span></span>  <br/> |<span data-ttu-id="82c81-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="82c81-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="82c81-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="82c81-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="82c81-134">Falso</span><span class="sxs-lookup"><span data-stu-id="82c81-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82c81-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="82c81-135">See also</span></span>



- [<span data-ttu-id="82c81-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="82c81-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

