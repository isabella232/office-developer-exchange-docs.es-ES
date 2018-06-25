---
title: EnhancedLocation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4fdfb74f-f33c-46ae-a7c7-451a5b0c6a59
description: El elemento EnhancedLocation especifica la información de ubicación, como el nombre, dirección y notas opcionales sobre una ubicación.
ms.openlocfilehash: 90397cfc622fed40c561d30c13d6617eb979a68a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764419"
---
# <a name="enhancedlocation"></a><span data-ttu-id="98dc6-103">EnhancedLocation</span><span class="sxs-lookup"><span data-stu-id="98dc6-103">EnhancedLocation</span></span>

<span data-ttu-id="98dc6-104">El elemento **EnhancedLocation** especifica la información de ubicación, como el nombre, dirección y notas opcionales sobre una ubicación.</span><span class="sxs-lookup"><span data-stu-id="98dc6-104">The **EnhancedLocation** element specifies location information such as the name, address, and optional notes about a location.</span></span> 
  
```XML
<EnhancedLocation>
    <DisplayName/>
    <Annotation/>
    <PostalAddress/>
</EnhancedLocation>
```

 <span data-ttu-id="98dc6-105">**EnhancedLocationType**</span><span class="sxs-lookup"><span data-stu-id="98dc6-105">**EnhancedLocationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="98dc6-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="98dc6-106">Attributes and elements</span></span>

<span data-ttu-id="98dc6-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="98dc6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="98dc6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="98dc6-108">Attributes</span></span>

<span data-ttu-id="98dc6-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="98dc6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="98dc6-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="98dc6-110">Child elements</span></span>

|<span data-ttu-id="98dc6-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="98dc6-111">**Element**</span></span>|<span data-ttu-id="98dc6-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="98dc6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98dc6-113">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="98dc6-113">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="98dc6-114">Define el nombre para mostrar de una carpeta, contacto, lista de distribución, usuario delegado, ubicación o regla.</span><span class="sxs-lookup"><span data-stu-id="98dc6-114">Defines the display name of a folder, contact, distribution list, delegate user, location, or rule.</span></span>  <br/> |
|[<span data-ttu-id="98dc6-115">Anotación</span><span class="sxs-lookup"><span data-stu-id="98dc6-115">Annotation</span></span>](annotation.md) <br/> |<span data-ttu-id="98dc6-116">Contiene notas opcionales agregadas por un usuario.</span><span class="sxs-lookup"><span data-stu-id="98dc6-116">Contains optional notes added by a user.</span></span>  <br/> |
|[<span data-ttu-id="98dc6-117">PostalAddress (PersonaPostalAddressType)</span><span class="sxs-lookup"><span data-stu-id="98dc6-117">PostalAddress (PersonaPostalAddressType)</span></span>](postaladdress-personapostaladdresstype.md) <br/> |<span data-ttu-id="98dc6-118">Especifica la dirección postal para un rol.</span><span class="sxs-lookup"><span data-stu-id="98dc6-118">Specifies the postal address for a persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="98dc6-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="98dc6-119">Parent elements</span></span>

|<span data-ttu-id="98dc6-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="98dc6-120">**Element**</span></span>|<span data-ttu-id="98dc6-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="98dc6-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98dc6-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="98dc6-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="98dc6-123">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="98dc6-123">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="98dc6-124">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="98dc6-124">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="98dc6-125">Representa la cancelación de la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="98dc6-125">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="98dc6-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="98dc6-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="98dc6-127">Representa una respuesta a la reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="98dc6-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98dc6-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="98dc6-128">Remarks</span></span>

<span data-ttu-id="98dc6-129">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="98dc6-129">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="98dc6-130">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="98dc6-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="98dc6-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="98dc6-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98dc6-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="98dc6-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="98dc6-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="98dc6-133">Schema Name</span></span>  <br/> |<span data-ttu-id="98dc6-134">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="98dc6-134">Type schema</span></span>  <br/> |
|<span data-ttu-id="98dc6-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="98dc6-135">Validation File</span></span>  <br/> |<span data-ttu-id="98dc6-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="98dc6-136">types.xsd</span></span>  <br/> |
|<span data-ttu-id="98dc6-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="98dc6-137">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="98dc6-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="98dc6-138">See also</span></span>



- [<span data-ttu-id="98dc6-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="98dc6-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

