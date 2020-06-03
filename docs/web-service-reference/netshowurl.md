---
title: NetShowUrl
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NetShowUrl
api_type:
- schema
ms.assetid: a5d48fc1-b141-422c-bcb0-05d0f9ba90dd
description: El elemento NetShowUrl especifica la dirección URL de una reunión en línea de Microsoft NetShow.
ms.openlocfilehash: 66e288a5e66eecf404698135cc3257085b852034
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466335"
---
# <a name="netshowurl"></a><span data-ttu-id="31e5c-103">NetShowUrl</span><span class="sxs-lookup"><span data-stu-id="31e5c-103">NetShowUrl</span></span>

<span data-ttu-id="31e5c-104">El elemento **NetShowUrl** especifica la dirección URL de una reunión en línea de Microsoft NetShow.</span><span class="sxs-lookup"><span data-stu-id="31e5c-104">The **NetShowUrl** element specifies the URL for a Microsoft NetShow online meeting.</span></span> 
  
```xml
<NetShowUrl/>
```

 <span data-ttu-id="31e5c-105">**string**</span><span class="sxs-lookup"><span data-stu-id="31e5c-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="31e5c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="31e5c-106">Attributes and elements</span></span>

<span data-ttu-id="31e5c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="31e5c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31e5c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="31e5c-108">Attributes</span></span>

<span data-ttu-id="31e5c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="31e5c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="31e5c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="31e5c-110">Child elements</span></span>

<span data-ttu-id="31e5c-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="31e5c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="31e5c-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="31e5c-112">Parent elements</span></span>

|<span data-ttu-id="31e5c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="31e5c-113">**Element**</span></span>|<span data-ttu-id="31e5c-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="31e5c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31e5c-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="31e5c-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="31e5c-116">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="31e5c-116">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="31e5c-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="31e5c-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="31e5c-118">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="31e5c-118">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="31e5c-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="31e5c-119">Text value</span></span>

<span data-ttu-id="31e5c-120">Si se usa este elemento, es necesario un valor de texto que represente una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="31e5c-120">A text value that represents a URL is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31e5c-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31e5c-121">Remarks</span></span>

<span data-ttu-id="31e5c-122">Esta propiedad NetShowUrl es de lectura y escritura para el elemento de calendario del organizador.</span><span class="sxs-lookup"><span data-stu-id="31e5c-122">This NetShowUrl property is read-writable for the organizer's calendar item.</span></span> <span data-ttu-id="31e5c-123">Es de solo lectura para las convocatorias de reunión y para los asistentes.</span><span class="sxs-lookup"><span data-stu-id="31e5c-123">It is read-only for meeting requests and for attendees.</span></span>
  
<span data-ttu-id="31e5c-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="31e5c-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31e5c-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="31e5c-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31e5c-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="31e5c-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="31e5c-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="31e5c-127">Schema name</span></span>  <br/> |<span data-ttu-id="31e5c-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="31e5c-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="31e5c-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="31e5c-129">Validation file</span></span>  <br/> |<span data-ttu-id="31e5c-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="31e5c-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="31e5c-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="31e5c-131">Can be empty</span></span>  <br/> |<span data-ttu-id="31e5c-132">Falso</span><span class="sxs-lookup"><span data-stu-id="31e5c-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31e5c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="31e5c-133">See also</span></span>



- [<span data-ttu-id="31e5c-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="31e5c-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

