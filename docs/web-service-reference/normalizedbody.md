---
title: NormalizedBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfb813e4-642d-4f1b-9e91-1fee89dbd083
description: El elemento NormalizedBody especifica una representación HTML de la propiedad de cuerpo de un elemento como un fragmento que puede insertarse en otro cuerpo HTML.
ms.openlocfilehash: 07c2176d2c8a7473c06b7e42f8bcbbe6670581ef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836548"
---
# <a name="normalizedbody"></a><span data-ttu-id="f8b5c-103">NormalizedBody</span><span class="sxs-lookup"><span data-stu-id="f8b5c-103">NormalizedBody</span></span>

<span data-ttu-id="f8b5c-104">El elemento **NormalizedBody** especifica una representación HTML de la propiedad de **cuerpo** de un elemento como un fragmento que puede insertarse en otro cuerpo HTML.</span><span class="sxs-lookup"><span data-stu-id="f8b5c-104">The **NormalizedBody** element specifies an HTML representation of the **Body** property of an item as a fragment that can be inserted into another HTML body.</span></span> 
  
```XML
<NormalizedBody BodyType="Text | HTML" IsTruncated="true | false"></NormalizedBody>
```

 <span data-ttu-id="f8b5c-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="f8b5c-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f8b5c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f8b5c-106">Attributes and elements</span></span>

<span data-ttu-id="f8b5c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f8b5c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f8b5c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f8b5c-108">Attributes</span></span>

|<span data-ttu-id="f8b5c-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f8b5c-109">**Attribute**</span></span>|<span data-ttu-id="f8b5c-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f8b5c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f8b5c-111">BodyType</span><span class="sxs-lookup"><span data-stu-id="f8b5c-111">BodyType</span></span>  <br/> |<span data-ttu-id="f8b5c-112">Indica el tipo de cuerpo.</span><span class="sxs-lookup"><span data-stu-id="f8b5c-112">Indicates the body type.</span></span> <span data-ttu-id="f8b5c-113">El valor de **texto** para el atributo **BodyType** indica que el cuerpo tiene formato de texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="f8b5c-113">The value of **Text** for the **BodyType** attribute indicates that the body is in plain text form.</span></span> <span data-ttu-id="f8b5c-114">El valor de **HTML** para el atributo **BodyType** indica que el cuerpo está en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="f8b5c-114">The value of **HTML** for the **BodyType** attribute indicates that the body is in HTML form.</span></span> <span data-ttu-id="f8b5c-115">El atributo **BodyType** es necesario.</span><span class="sxs-lookup"><span data-stu-id="f8b5c-115">The **BodyType** attribute is required.</span></span>  <br/> |
|<span data-ttu-id="f8b5c-116">IsTruncated</span><span class="sxs-lookup"><span data-stu-id="f8b5c-116">IsTruncated</span></span>  <br/> |<span data-ttu-id="f8b5c-117">Indica que el contenido del cuerpo se ha truncado.</span><span class="sxs-lookup"><span data-stu-id="f8b5c-117">Indicates that the body contents have been truncated.</span></span> <span data-ttu-id="f8b5c-118">Un valor de texto de **false** para el atributo **IsTruncated** indica que no se ha truncado el contenido del cuerpo.</span><span class="sxs-lookup"><span data-stu-id="f8b5c-118">A text value of **false** for the **IsTruncated** attribute indicates that the body contents have not been truncated.</span></span> <span data-ttu-id="f8b5c-119">Si la longitud del cuerpo normalizado es mayor que el valor establecido en el elemento [MaximumBodySize](maximumbodysize.md) , se truncará el cuerpo normalizado.</span><span class="sxs-lookup"><span data-stu-id="f8b5c-119">The normalized body will be truncated if the normalized body length is longer than the value set in the [MaximumBodySize](maximumbodysize.md) element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f8b5c-120">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f8b5c-120">Child elements</span></span>

<span data-ttu-id="f8b5c-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f8b5c-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f8b5c-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f8b5c-122">Parent elements</span></span>

<span data-ttu-id="f8b5c-123">[Elemento](item.md) | [mensaje](message-ex15websvcsotherref.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [tarea](task.md) | [PostItem ](postitem.md)  |  [CalendarItem](calendaritem.md) | [contacto](contact.md) | [DistributionList](distributionlist.md)</span><span class="sxs-lookup"><span data-stu-id="f8b5c-123">[Item](item.md) | [Message](message-ex15websvcsotherref.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [Task](task.md) | [PostItem](postitem.md) | [CalendarItem](calendaritem.md) | [Contact](contact.md) | [DistributionList](distributionlist.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="f8b5c-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f8b5c-124">Text value</span></span>

<span data-ttu-id="f8b5c-125">El valor de texto del elemento **NormalizedBody** es el cuerpo del elemento normalizado.</span><span class="sxs-lookup"><span data-stu-id="f8b5c-125">The text value of the **NormalizedBody** element is the normalized body of the item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f8b5c-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f8b5c-126">Remarks</span></span>

<span data-ttu-id="f8b5c-127">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f8b5c-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f8b5c-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f8b5c-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f8b5c-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f8b5c-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8b5c-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f8b5c-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f8b5c-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f8b5c-131">Schema name</span></span>  <br/> |<span data-ttu-id="f8b5c-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f8b5c-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="f8b5c-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f8b5c-133">Validation file</span></span>  <br/> |<span data-ttu-id="f8b5c-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f8b5c-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f8b5c-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f8b5c-135">Can be empty</span></span>  <br/> ||
   

