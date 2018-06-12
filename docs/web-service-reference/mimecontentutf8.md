---
title: MimeContentUTF8
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 31544c95-5231-4b57-958c-2a689464d29b
description: El elemento MimeContentUTF8 contiene la secuencia de UTF-8 MIME de un objeto que se representa en formato base64Binary y admite internalización de dirección de correo electrónico y [RFC6530].
ms.openlocfilehash: 47599b6634738fd488e5b020f69e36d5fcf550a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836466"
---
# <a name="mimecontentutf8"></a><span data-ttu-id="b011e-103">MimeContentUTF8</span><span class="sxs-lookup"><span data-stu-id="b011e-103">MimeContentUTF8</span></span>

<span data-ttu-id="b011e-104">El elemento **MimeContentUTF8** contiene la secuencia de UTF-8 MIME de un objeto que se representa en formato base64Binary y admite internalización de dirección de correo electrónico y [[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt).</span><span class="sxs-lookup"><span data-stu-id="b011e-104">The **MimeContentUTF8** element contains the UTF-8 MIME stream of an object that is represented in base64Binary format and supports email address internationalization and [[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt).</span></span>
  
```XML
<MimeContentUTF8 CharacterSet="" />
```

 <span data-ttu-id="b011e-105">**MimeContentType**</span><span class="sxs-lookup"><span data-stu-id="b011e-105">**MimeContentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b011e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b011e-106">Attributes and elements</span></span>

<span data-ttu-id="b011e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b011e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b011e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b011e-108">Attributes</span></span>

|<span data-ttu-id="b011e-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="b011e-109">**Attribute**</span></span>|<span data-ttu-id="b011e-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b011e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b011e-111">**Conjunto de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b011e-111">**CharacterSet**</span></span> <br/> |<span data-ttu-id="b011e-112">Si se establece, el valor para este atributo se omite el servidor.</span><span class="sxs-lookup"><span data-stu-id="b011e-112">If set, the value for this attribute is ignored by the server.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b011e-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b011e-113">Child elements</span></span>

<span data-ttu-id="b011e-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b011e-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b011e-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b011e-115">Parent elements</span></span>

<span data-ttu-id="b011e-116">[CalendarItem](calendaritem.md) | [contacto](contact.md) | [DistributionList](distributionlist.md) | [elemento](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md)  |  [ MeetingResponse](meetingresponse.md) | [mensaje](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [tarea](task.md)</span><span class="sxs-lookup"><span data-stu-id="b011e-116">[CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Item](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [Message](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="b011e-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b011e-117">Text value</span></span>

<span data-ttu-id="b011e-118">Un valor de texto que representa una secuencia MIME base64binary es necesario si se usa este elemento.</span><span class="sxs-lookup"><span data-stu-id="b011e-118">A text value that represents a base64binary MIME stream is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b011e-119">Notas</span><span class="sxs-lookup"><span data-stu-id="b011e-119">Remarks</span></span>

<span data-ttu-id="b011e-120">El contenido del mensaje circula a través de los tres niveles siguientes de codificación antes de que se almacene en el valor de **MimeContentUTF8** :</span><span class="sxs-lookup"><span data-stu-id="b011e-120">The message content goes through the following three levels of encoding before it is stored in the **MimeContentUTF8** value:</span></span> 
  
1. <span data-ttu-id="b011e-121">Texto del mensaje: este es el cuerpo de la codificación, como iso-2022-jp para caracteres en japonés.</span><span class="sxs-lookup"><span data-stu-id="b011e-121">Message text — This is the body encoding, such as iso-2022-jp for Japanese characters.</span></span>
    
2. <span data-ttu-id="b011e-122">Secuencia MIME: se trata de la codificación UTF8 del texto del mensaje para el elemento de **MimeContentUTF8** o la codificación ASCII del texto del mensaje para el elemento [MimeContent](mimecontent.md) .</span><span class="sxs-lookup"><span data-stu-id="b011e-122">MIME stream — This is the UTF8 encoding of the message text for the **MimeContentUTF8** element, or the ASCII encoding of the message text for the [MimeContent](mimecontent.md) element.</span></span> 
    
3. <span data-ttu-id="b011e-123">Documento XML — siempre es la secuencia de ASCII con codificación base64 de la secuencia MIME, donde caracteres como '\<', que son significativas para XML, están ocultos de los analizadores XML.</span><span class="sxs-lookup"><span data-stu-id="b011e-123">XML document — This is always the base64-encoded ASCII stream of the MIME stream, where characters such as '\<', which are meaningful to XML, are hidden from XML parsers.</span></span>
    
<span data-ttu-id="b011e-124">Cada nivel es independiente del nivel que le precede.</span><span class="sxs-lookup"><span data-stu-id="b011e-124">Each level is independent of the level that precedes it.</span></span>
  
<span data-ttu-id="b011e-125">El elemento **MimeContentUTF8** podría contener los mismos datos que contienen otras propiedades que se devuelven con un elemento.</span><span class="sxs-lookup"><span data-stu-id="b011e-125">The **MimeContentUTF8** element might contain the same data that other properties that are returned with an item contain.</span></span> 
  
<span data-ttu-id="b011e-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b011e-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="b011e-127">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="b011e-127">Version differences</span></span>

<span data-ttu-id="b011e-128">Este elemento está disponible en las versiones de Exchange a partir de compilación 15.00.0986.00.</span><span class="sxs-lookup"><span data-stu-id="b011e-128">This element is available in versions of Exchange starting with build 15.00.0986.00.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b011e-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b011e-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b011e-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b011e-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b011e-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b011e-131">Schema Name</span></span>  <br/> |<span data-ttu-id="b011e-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b011e-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="b011e-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b011e-133">Validation File</span></span>  <br/> |<span data-ttu-id="b011e-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b011e-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b011e-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b011e-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="b011e-136">False</span><span class="sxs-lookup"><span data-stu-id="b011e-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b011e-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="b011e-137">See also</span></span>



- [<span data-ttu-id="b011e-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b011e-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

