---
title: MimeContentUTF8
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 31544c95-5231-4b57-958c-2a689464d29b
description: El elemento MimeContentUTF8 contiene la secuencia MIME UTF-8 de un objeto que se representa en formato base64Binary y admite la internacionalización de la dirección de correo electrónico y [RFC6530].
ms.openlocfilehash: a9214bda876c1aadac5b026b3adf38faea8ef17a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530432"
---
# <a name="mimecontentutf8"></a><span data-ttu-id="c4c4a-103">MimeContentUTF8</span><span class="sxs-lookup"><span data-stu-id="c4c4a-103">MimeContentUTF8</span></span>

<span data-ttu-id="c4c4a-104">El elemento **MimeContentUTF8** contiene la secuencia MIME UTF-8 de un objeto que se representa en formato base64Binary y admite la internacionalización de la dirección de correo electrónico y [[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt).</span><span class="sxs-lookup"><span data-stu-id="c4c4a-104">The **MimeContentUTF8** element contains the UTF-8 MIME stream of an object that is represented in base64Binary format and supports email address internationalization and [[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt).</span></span>
  
```XML
<MimeContentUTF8 CharacterSet="" />
```

 <span data-ttu-id="c4c4a-105">**MimeContentType**</span><span class="sxs-lookup"><span data-stu-id="c4c4a-105">**MimeContentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c4c4a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c4c4a-106">Attributes and elements</span></span>

<span data-ttu-id="c4c4a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c4c4a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c4c4a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c4c4a-108">Attributes</span></span>

|<span data-ttu-id="c4c4a-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c4c4a-109">**Attribute**</span></span>|<span data-ttu-id="c4c4a-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c4c4a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c4c4a-111">**CharacterSet**</span><span class="sxs-lookup"><span data-stu-id="c4c4a-111">**CharacterSet**</span></span> <br/> |<span data-ttu-id="c4c4a-112">Si se establece, el valor de este atributo es ignorado por el servidor.</span><span class="sxs-lookup"><span data-stu-id="c4c4a-112">If set, the value for this attribute is ignored by the server.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c4c4a-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c4c4a-113">Child elements</span></span>

<span data-ttu-id="c4c4a-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c4c4a-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c4c4a-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c4c4a-115">Parent elements</span></span>

<span data-ttu-id="c4c4a-116">[CalendarItem](calendaritem.md)  |  [Contacto](contact.md)  |  [DistributionList](distributionlist.md)  |  [Elemento](item.md)  |  [MeetingCancellation](meetingcancellation.md)  |  [MeetingMessage](meetingmessage.md)  |  Propiedad [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md)  |  [Mensaje de error](message-ex15websvcsotherref.md)  |  [RemoveItem](removeitem.md)  |  [Tarea](task.md)</span><span class="sxs-lookup"><span data-stu-id="c4c4a-116">[CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md) | [Item](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [Message](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="c4c4a-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c4c4a-117">Text value</span></span>

<span data-ttu-id="c4c4a-118">Si se usa este elemento, se necesita un valor de texto que represente una secuencia MIME base64Binary.</span><span class="sxs-lookup"><span data-stu-id="c4c4a-118">A text value that represents a base64binary MIME stream is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c4c4a-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c4c4a-119">Remarks</span></span>

<span data-ttu-id="c4c4a-120">El contenido del mensaje pasa por los tres niveles siguientes de codificación antes de almacenarse en el valor **MimeContentUTF8** :</span><span class="sxs-lookup"><span data-stu-id="c4c4a-120">The message content goes through the following three levels of encoding before it is stored in the **MimeContentUTF8** value:</span></span> 
  
1. <span data-ttu-id="c4c4a-121">Texto del mensaje: esta es la codificación del cuerpo, como ISO-2022-JP para caracteres japoneses.</span><span class="sxs-lookup"><span data-stu-id="c4c4a-121">Message text — This is the body encoding, such as iso-2022-jp for Japanese characters.</span></span>
    
2. <span data-ttu-id="c4c4a-122">Secuencia MIME: esta es la codificación UTF8 del texto del mensaje para el elemento **MimeContentUTF8** , o la codificación ASCII del texto del mensaje para el elemento [MimeContent](mimecontent.md) .</span><span class="sxs-lookup"><span data-stu-id="c4c4a-122">MIME stream — This is the UTF8 encoding of the message text for the **MimeContentUTF8** element, or the ASCII encoding of the message text for the [MimeContent](mimecontent.md) element.</span></span> 
    
3. <span data-ttu-id="c4c4a-123">Documento XML: siempre es la secuencia ASCII codificada en Base64 de la secuencia MIME, donde los caracteres como ' \< ', que son significativos para XML, están ocultos a los analizadores XML.</span><span class="sxs-lookup"><span data-stu-id="c4c4a-123">XML document — This is always the base64-encoded ASCII stream of the MIME stream, where characters such as '\<', which are meaningful to XML, are hidden from XML parsers.</span></span>
    
<span data-ttu-id="c4c4a-124">Cada nivel es independiente del nivel que le precede.</span><span class="sxs-lookup"><span data-stu-id="c4c4a-124">Each level is independent of the level that precedes it.</span></span>
  
<span data-ttu-id="c4c4a-125">El elemento **MimeContentUTF8** puede contener los mismos datos que contienen otras propiedades que se devuelven con un elemento.</span><span class="sxs-lookup"><span data-stu-id="c4c4a-125">The **MimeContentUTF8** element might contain the same data that other properties that are returned with an item contain.</span></span> 
  
<span data-ttu-id="c4c4a-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c4c4a-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
### <a name="version-differences"></a><span data-ttu-id="c4c4a-127">Diferencias de versión</span><span class="sxs-lookup"><span data-stu-id="c4c4a-127">Version differences</span></span>

<span data-ttu-id="c4c4a-128">Este elemento está disponible en las versiones de Exchange que comienzan con la compilación 15.00.0986.00.</span><span class="sxs-lookup"><span data-stu-id="c4c4a-128">This element is available in versions of Exchange starting with build 15.00.0986.00.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c4c4a-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c4c4a-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4c4a-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="c4c4a-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c4c4a-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c4c4a-131">Schema Name</span></span>  <br/> |<span data-ttu-id="c4c4a-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c4c4a-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="c4c4a-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c4c4a-133">Validation File</span></span>  <br/> |<span data-ttu-id="c4c4a-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c4c4a-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c4c4a-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c4c4a-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="c4c4a-136">Falso</span><span class="sxs-lookup"><span data-stu-id="c4c4a-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c4c4a-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4c4a-137">See also</span></span>



- [<span data-ttu-id="c4c4a-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c4c4a-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

