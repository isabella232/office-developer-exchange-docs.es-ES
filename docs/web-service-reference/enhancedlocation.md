---
title: EnhancedLocation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4fdfb74f-f33c-46ae-a7c7-451a5b0c6a59
description: El elemento EnhancedLocation especifica información de ubicación, como el nombre, la dirección y las notas opcionales de una ubicación.
ms.openlocfilehash: 06ec800b763ef61af51da03ca8a340f6ac4d2a8e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462960"
---
# <a name="enhancedlocation"></a><span data-ttu-id="3c6af-103">EnhancedLocation</span><span class="sxs-lookup"><span data-stu-id="3c6af-103">EnhancedLocation</span></span>

<span data-ttu-id="3c6af-104">El elemento **EnhancedLocation** especifica información de ubicación, como el nombre, la dirección y las notas opcionales de una ubicación.</span><span class="sxs-lookup"><span data-stu-id="3c6af-104">The **EnhancedLocation** element specifies location information such as the name, address, and optional notes about a location.</span></span> 
  
```XML
<EnhancedLocation>
    <DisplayName/>
    <Annotation/>
    <PostalAddress/>
</EnhancedLocation>
```

 <span data-ttu-id="3c6af-105">**EnhancedLocationType**</span><span class="sxs-lookup"><span data-stu-id="3c6af-105">**EnhancedLocationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3c6af-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3c6af-106">Attributes and elements</span></span>

<span data-ttu-id="3c6af-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3c6af-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c6af-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3c6af-108">Attributes</span></span>

<span data-ttu-id="3c6af-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3c6af-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3c6af-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3c6af-110">Child elements</span></span>

|<span data-ttu-id="3c6af-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3c6af-111">**Element**</span></span>|<span data-ttu-id="3c6af-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3c6af-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c6af-113">DisplayName (cadena)</span><span class="sxs-lookup"><span data-stu-id="3c6af-113">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="3c6af-114">Define el nombre para mostrar de una carpeta, un contacto, una lista de distribución, un usuario delegado, una ubicación o una regla.</span><span class="sxs-lookup"><span data-stu-id="3c6af-114">Defines the display name of a folder, contact, distribution list, delegate user, location, or rule.</span></span>  <br/> |
|[<span data-ttu-id="3c6af-115">Anotación</span><span class="sxs-lookup"><span data-stu-id="3c6af-115">Annotation</span></span>](annotation.md) <br/> |<span data-ttu-id="3c6af-116">Contiene las notas opcionales agregadas por un usuario.</span><span class="sxs-lookup"><span data-stu-id="3c6af-116">Contains optional notes added by a user.</span></span>  <br/> |
|[<span data-ttu-id="3c6af-117">PostalAddress (PersonaPostalAddressType)</span><span class="sxs-lookup"><span data-stu-id="3c6af-117">PostalAddress (PersonaPostalAddressType)</span></span>](postaladdress-personapostaladdresstype.md) <br/> |<span data-ttu-id="3c6af-118">Especifica la dirección postal de un rol.</span><span class="sxs-lookup"><span data-stu-id="3c6af-118">Specifies the postal address for a persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3c6af-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3c6af-119">Parent elements</span></span>

|<span data-ttu-id="3c6af-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3c6af-120">**Element**</span></span>|<span data-ttu-id="3c6af-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3c6af-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c6af-122">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="3c6af-122">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="3c6af-123">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3c6af-123">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="3c6af-124">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="3c6af-124">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="3c6af-125">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3c6af-125">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3c6af-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="3c6af-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="3c6af-127">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3c6af-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c6af-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3c6af-128">Remarks</span></span>

<span data-ttu-id="3c6af-129">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3c6af-129">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3c6af-130">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3c6af-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c6af-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3c6af-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c6af-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c6af-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3c6af-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3c6af-133">Schema Name</span></span>  <br/> |<span data-ttu-id="3c6af-134">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="3c6af-134">Type schema</span></span>  <br/> |
|<span data-ttu-id="3c6af-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3c6af-135">Validation File</span></span>  <br/> |<span data-ttu-id="3c6af-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="3c6af-136">types.xsd</span></span>  <br/> |
|<span data-ttu-id="3c6af-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3c6af-137">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3c6af-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c6af-138">See also</span></span>



- [<span data-ttu-id="3c6af-139">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3c6af-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

