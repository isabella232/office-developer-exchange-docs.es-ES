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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836466"
---
# <a name="mimecontentutf8"></a><span data-ttu-id="1a742-103">MimeContentUTF8</span><span class="sxs-lookup"><span data-stu-id="1a742-103">MimeContentUTF8</span></span>

<span data-ttu-id="1a742-104">El elemento **MimeContentUTF8** contiene la secuencia de UTF-8 MIME de un objeto que se representa en formato base64Binary y admite internalización de dirección de correo electrónico y [[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt).</span><span class="sxs-lookup"><span data-stu-id="1a742-104">The **MimeContentUTF8** element contains the UTF-8 MIME stream of an object that is represented in base64Binary format and supports email address internationalization and [[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt).</span></span>
  
```XML
<MimeContentUTF8 CharacterSet="" />
```

 <span data-ttu-id="1a742-105">**MimeContentType**</span><span class="sxs-lookup"><span data-stu-id="1a742-105">**MimeContentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1a742-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1a742-106">Attributes and elements</span></span>

<span data-ttu-id="1a742-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1a742-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1a742-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1a742-108">Attributes</span></span>

|<span data-ttu-id="1a742-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="1a742-109">**Attribute**</span></span>|<span data-ttu-id="1a742-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1a742-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1a742-111">**Conjunto de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a742-111">**CharacterSet**</span></span> <br/> |<span data-ttu-id="1a742-112">Si se establece, el valor para este atributo se omite el servidor.</span><span class="sxs-lookup"><span data-stu-id="1a742-112">If set, the value for this attribute is ignored by the server.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1a742-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1a742-113">Child elements</span></span>

<span data-ttu-id="1a742-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1a742-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1a742-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1a742-115">Parent elements</span></span>

<span data-ttu-id="1a742-116">[CalendarItem](calendaritem.md) | [contacto](contact.md) | [DistributionList](distributionlist.md) | [elemento](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md)  |  [ MeetingResponse](meetingresponse.md) | [mensaje](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [tarea](task.md)</span><span class="sxs-lookup"><span data-stu-id="1a742-116">[CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Item](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [Message](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="1a742-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1a742-117">Text value</span></span>

<span data-ttu-id="1a742-118">Un valor de texto que representa una secuencia MIME base64binary es necesario si se usa este elemento.</span><span class="sxs-lookup"><span data-stu-id="1a742-118">A text value that represents a base64binary MIME stream is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1a742-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1a742-119">Remarks</span></span>

<span data-ttu-id="1a742-120">El contenido del mensaje circula a través de los tres niveles siguientes de codificación antes de que se almacene en el valor de **MimeContentUTF8** :</span><span class="sxs-lookup"><span data-stu-id="1a742-120">The message content goes through the following three levels of encoding before it is stored in the **MimeContentUTF8** value:</span></span> 
  
1. <span data-ttu-id="1a742-121">Texto del mensaje: este es el cuerpo de la codificación, como iso-2022-jp para caracteres en japonés.</span><span class="sxs-lookup"><span data-stu-id="1a742-121">Message text — This is the body encoding, such as iso-2022-jp for Japanese characters.</span></span>
    
2. <span data-ttu-id="1a742-122">Secuencia MIME: se trata de la codificación UTF8 del texto del mensaje para el elemento de **MimeContentUTF8** o la codificación ASCII del texto del mensaje para el elemento [MimeContent](mimecontent.md) .</span><span class="sxs-lookup"><span data-stu-id="1a742-122">MIME stream — This is the UTF8 encoding of the message text for the **MimeContentUTF8** element, or the ASCII encoding of the message text for the [MimeContent](mimecontent.md) element.</span></span> 
    
3. <span data-ttu-id="1a742-123">Documento XML — siempre es la secuencia de ASCII con codificación base64 de la secuencia MIME, donde caracteres como '\<', que son significativas para XML, están ocultos de los analizadores XML.</span><span class="sxs-lookup"><span data-stu-id="1a742-123">XML document — This is always the base64-encoded ASCII stream of the MIME stream, where characters such as '\<', which are meaningful to XML, are hidden from XML parsers.</span></span>
    
<span data-ttu-id="1a742-124">Cada nivel es independiente del nivel que le precede.</span><span class="sxs-lookup"><span data-stu-id="1a742-124">Each level is independent of the level that precedes it.</span></span>
  
<span data-ttu-id="1a742-125">El elemento **MimeContentUTF8** podría contener los mismos datos que contienen otras propiedades que se devuelven con un elemento.</span><span class="sxs-lookup"><span data-stu-id="1a742-125">The **MimeContentUTF8** element might contain the same data that other properties that are returned with an item contain.</span></span> 
  
<span data-ttu-id="1a742-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1a742-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="1a742-127">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="1a742-127">Version differences</span></span>

<span data-ttu-id="1a742-128">Este elemento está disponible en las versiones de Exchange a partir de compilación 15.00.0986.00.</span><span class="sxs-lookup"><span data-stu-id="1a742-128">This element is available in versions of Exchange starting with build 15.00.0986.00.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1a742-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1a742-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a742-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1a742-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1a742-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1a742-131">Schema Name</span></span>  <br/> |<span data-ttu-id="1a742-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1a742-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="1a742-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1a742-133">Validation File</span></span>  <br/> |<span data-ttu-id="1a742-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1a742-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1a742-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1a742-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="1a742-136">False</span><span class="sxs-lookup"><span data-stu-id="1a742-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1a742-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a742-137">See also</span></span>



- [<span data-ttu-id="1a742-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="1a742-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

