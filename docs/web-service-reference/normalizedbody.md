---
title: NormalizedBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfb813e4-642d-4f1b-9e91-1fee89dbd083
description: El elemento NormalizedBody especifica una representación HTML de la propiedad Body de un elemento como un fragmento que se puede insertar en otro cuerpo HTML.
ms.openlocfilehash: fb249794bccfeed198e7a3230ab53c66893dcf96
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462671"
---
# <a name="normalizedbody"></a><span data-ttu-id="a6082-103">NormalizedBody</span><span class="sxs-lookup"><span data-stu-id="a6082-103">NormalizedBody</span></span>

<span data-ttu-id="a6082-104">El elemento **NormalizedBody** especifica una representación HTML de la propiedad **Body** de un elemento como un fragmento que se puede insertar en otro cuerpo HTML.</span><span class="sxs-lookup"><span data-stu-id="a6082-104">The **NormalizedBody** element specifies an HTML representation of the **Body** property of an item as a fragment that can be inserted into another HTML body.</span></span> 
  
```XML
<NormalizedBody BodyType="Text | HTML" IsTruncated="true | false"></NormalizedBody>
```

 <span data-ttu-id="a6082-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="a6082-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a6082-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a6082-106">Attributes and elements</span></span>

<span data-ttu-id="a6082-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a6082-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a6082-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a6082-108">Attributes</span></span>

|<span data-ttu-id="a6082-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a6082-109">**Attribute**</span></span>|<span data-ttu-id="a6082-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a6082-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a6082-111">BodyType</span><span class="sxs-lookup"><span data-stu-id="a6082-111">BodyType</span></span>  <br/> |<span data-ttu-id="a6082-112">Indica el tipo de cuerpo.</span><span class="sxs-lookup"><span data-stu-id="a6082-112">Indicates the body type.</span></span> <span data-ttu-id="a6082-113">El valor de **Text** para el atributo **BodyType** indica que el cuerpo está en forma de texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="a6082-113">The value of **Text** for the **BodyType** attribute indicates that the body is in plain text form.</span></span> <span data-ttu-id="a6082-114">El valor de **HTML** para el atributo **BodyType** indica que el cuerpo está en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="a6082-114">The value of **HTML** for the **BodyType** attribute indicates that the body is in HTML form.</span></span> <span data-ttu-id="a6082-115">El atributo **BodyType** es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a6082-115">The **BodyType** attribute is required.</span></span>  <br/> |
|<span data-ttu-id="a6082-116">IsTruncated</span><span class="sxs-lookup"><span data-stu-id="a6082-116">IsTruncated</span></span>  <br/> |<span data-ttu-id="a6082-117">Indica que se ha truncado el contenido del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="a6082-117">Indicates that the body contents have been truncated.</span></span> <span data-ttu-id="a6082-118">Un valor de texto **falso** para el atributo **IsTruncated** indica que el contenido del cuerpo no se ha truncado.</span><span class="sxs-lookup"><span data-stu-id="a6082-118">A text value of **false** for the **IsTruncated** attribute indicates that the body contents have not been truncated.</span></span> <span data-ttu-id="a6082-119">El cuerpo normalizado se truncará si la longitud del cuerpo normalizado es mayor que el valor establecido en el elemento [MaximumBodySize](maximumbodysize.md) .</span><span class="sxs-lookup"><span data-stu-id="a6082-119">The normalized body will be truncated if the normalized body length is longer than the value set in the [MaximumBodySize](maximumbodysize.md) element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a6082-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a6082-120">Child elements</span></span>

<span data-ttu-id="a6082-121">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a6082-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a6082-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a6082-122">Parent elements</span></span>

<span data-ttu-id="a6082-123">[Elemento](item.md)  |  [Mensaje de error](message-ex15websvcsotherref.md)  |  [MeetingMessage](meetingmessage.md)  |  Propiedad [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md)  |  [MeetingCancellation](meetingcancellation.md)  |  [Tarea](task.md)  |  [PostItem](postitem.md)  |  [CalendarItem](calendaritem.md)  |  [Contacto](contact.md)  |  [DistributionList](distributionlist.md)</span><span class="sxs-lookup"><span data-stu-id="a6082-123">[Item](item.md) | [Message](message-ex15websvcsotherref.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [Task](task.md) | [PostItem](postitem.md) | [CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="a6082-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a6082-124">Text value</span></span>

<span data-ttu-id="a6082-125">El valor de texto del elemento **NormalizedBody** es el cuerpo normalizado del elemento.</span><span class="sxs-lookup"><span data-stu-id="a6082-125">The text value of the **NormalizedBody** element is the normalized body of the item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a6082-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a6082-126">Remarks</span></span>

<span data-ttu-id="a6082-127">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a6082-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a6082-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a6082-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a6082-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a6082-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6082-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="a6082-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a6082-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a6082-131">Schema name</span></span>  <br/> |<span data-ttu-id="a6082-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a6082-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="a6082-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a6082-133">Validation file</span></span>  <br/> |<span data-ttu-id="a6082-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a6082-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a6082-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a6082-135">Can be empty</span></span>  <br/> ||
   

