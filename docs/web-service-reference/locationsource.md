---
title: LocationSource
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fc4d77d5-6200-4cf3-848a-1088fec0e0d6
description: El elemento LocationSource especifica información sobre el origen de la dirección postal asociada, por ejemplo, un contacto o una libreta de teléfonos.
ms.openlocfilehash: 7f5cf5fcca0a72287593349fcf5090a74225d012
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836248"
---
# <a name="locationsource"></a><span data-ttu-id="6f33d-103">LocationSource</span><span class="sxs-lookup"><span data-stu-id="6f33d-103">LocationSource</span></span>

<span data-ttu-id="6f33d-104">El elemento **LocationSource** especifica información sobre el origen de la dirección postal asociada, por ejemplo, un contacto o una libreta de teléfonos.</span><span class="sxs-lookup"><span data-stu-id="6f33d-104">The **LocationSource** element specifies information about the origin of the associated postal address, for example, a contact or a telephone book.</span></span> 
  
```XML
<LocationSource> None | LocationServices | PhonebookServices | Device | Contact | Resource </LocationSource>
```

 <span data-ttu-id="6f33d-105">**LocationSourceType**</span><span class="sxs-lookup"><span data-stu-id="6f33d-105">**LocationSourceType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f33d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6f33d-106">Attributes and elements</span></span>

<span data-ttu-id="6f33d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6f33d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f33d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6f33d-108">Attributes</span></span>

<span data-ttu-id="6f33d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6f33d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f33d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6f33d-110">Child elements</span></span>

<span data-ttu-id="6f33d-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6f33d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6f33d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6f33d-112">Parent elements</span></span>

<span data-ttu-id="6f33d-113">[Valor (PersonaPostalAddressType)](value-personapostaladdresstype.md) | [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)</span><span class="sxs-lookup"><span data-stu-id="6f33d-113">[Value (PersonaPostalAddressType)](value-personapostaladdresstype.md) | [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="6f33d-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6f33d-114">Text value</span></span>

<span data-ttu-id="6f33d-115">Los valores de texto para el elemento de **LocationSource** se enumeran en la siguiente tabla:</span><span class="sxs-lookup"><span data-stu-id="6f33d-115">The text values for the **LocationSource** element are listed in the following table:</span></span> 
  
<span data-ttu-id="6f33d-116">**Valores de texto de elemento LocationSource**</span><span class="sxs-lookup"><span data-stu-id="6f33d-116">**LocationSource element text values**</span></span>

|<span data-ttu-id="6f33d-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6f33d-117">**Value**</span></span>|<span data-ttu-id="6f33d-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f33d-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6f33d-119">None</span><span class="sxs-lookup"><span data-stu-id="6f33d-119">None</span></span>  <br/> |<span data-ttu-id="6f33d-120">No hay ningún origen de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="6f33d-120">There is no location source.</span></span>  <br/> |
|<span data-ttu-id="6f33d-121">LocationServices</span><span class="sxs-lookup"><span data-stu-id="6f33d-121">LocationServices</span></span>  <br/> |<span data-ttu-id="6f33d-122">La información obtenida de los servicios de ubicación.</span><span class="sxs-lookup"><span data-stu-id="6f33d-122">The information was obtained from location services.</span></span>  <br/> |
|<span data-ttu-id="6f33d-123">PhonebookServices</span><span class="sxs-lookup"><span data-stu-id="6f33d-123">PhonebookServices</span></span>  <br/> |<span data-ttu-id="6f33d-124">La información obtenida de los servicios de libreta de teléfonos.</span><span class="sxs-lookup"><span data-stu-id="6f33d-124">The information was obtained from phonebook services.</span></span>  <br/> |
|<span data-ttu-id="6f33d-125">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="6f33d-125">Device</span></span>  <br/> |<span data-ttu-id="6f33d-126">Se obtuvo la información desde el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6f33d-126">The information was obtained from the device.</span></span>  <br/> |
|<span data-ttu-id="6f33d-127">Contacto</span><span class="sxs-lookup"><span data-stu-id="6f33d-127">Contact</span></span>  <br/> |<span data-ttu-id="6f33d-128">La información obtenida de un contacto.</span><span class="sxs-lookup"><span data-stu-id="6f33d-128">The information was obtained from a contact.</span></span>  <br/> |
|<span data-ttu-id="6f33d-129">Recurso</span><span class="sxs-lookup"><span data-stu-id="6f33d-129">Resource</span></span>  <br/> |<span data-ttu-id="6f33d-130">La información obtenida de un recurso.</span><span class="sxs-lookup"><span data-stu-id="6f33d-130">The information was obtained from a resource.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f33d-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6f33d-131">Remarks</span></span>

<span data-ttu-id="6f33d-132">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6f33d-132">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6f33d-133">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6f33d-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  

