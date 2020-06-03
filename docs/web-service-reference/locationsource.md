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
ms.openlocfilehash: ceba52c43d1c798bb8f5492b779c7c45d7d00b0b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467105"
---
# <a name="locationsource"></a><span data-ttu-id="316d6-103">LocationSource</span><span class="sxs-lookup"><span data-stu-id="316d6-103">LocationSource</span></span>

<span data-ttu-id="316d6-104">El elemento **LocationSource** especifica información sobre el origen de la dirección postal asociada, por ejemplo, un contacto o una libreta de teléfonos.</span><span class="sxs-lookup"><span data-stu-id="316d6-104">The **LocationSource** element specifies information about the origin of the associated postal address, for example, a contact or a telephone book.</span></span> 
  
```XML
<LocationSource> None | LocationServices | PhonebookServices | Device | Contact | Resource </LocationSource>
```

 <span data-ttu-id="316d6-105">**LocationSourceType**</span><span class="sxs-lookup"><span data-stu-id="316d6-105">**LocationSourceType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="316d6-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="316d6-106">Attributes and elements</span></span>

<span data-ttu-id="316d6-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="316d6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="316d6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="316d6-108">Attributes</span></span>

<span data-ttu-id="316d6-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="316d6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="316d6-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="316d6-110">Child elements</span></span>

<span data-ttu-id="316d6-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="316d6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="316d6-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="316d6-112">Parent elements</span></span>

<span data-ttu-id="316d6-113">[Valor (PersonaPostalAddressType)](value-personapostaladdresstype.md)  |  [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)</span><span class="sxs-lookup"><span data-stu-id="316d6-113">[Value (PersonaPostalAddressType)](value-personapostaladdresstype.md) | [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="316d6-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="316d6-114">Text value</span></span>

<span data-ttu-id="316d6-115">En la tabla siguiente se enumeran los valores de texto para el elemento **LocationSource** :</span><span class="sxs-lookup"><span data-stu-id="316d6-115">The text values for the **LocationSource** element are listed in the following table:</span></span> 
  
<span data-ttu-id="316d6-116">**Valores de texto del elemento LocationSource**</span><span class="sxs-lookup"><span data-stu-id="316d6-116">**LocationSource element text values**</span></span>

|<span data-ttu-id="316d6-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="316d6-117">**Value**</span></span>|<span data-ttu-id="316d6-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="316d6-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="316d6-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="316d6-119">None</span></span>  <br/> |<span data-ttu-id="316d6-120">No hay origen de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="316d6-120">There is no location source.</span></span>  <br/> |
|<span data-ttu-id="316d6-121">LocationServices</span><span class="sxs-lookup"><span data-stu-id="316d6-121">LocationServices</span></span>  <br/> |<span data-ttu-id="316d6-122">La información se obtuvo de los servicios de ubicación.</span><span class="sxs-lookup"><span data-stu-id="316d6-122">The information was obtained from location services.</span></span>  <br/> |
|<span data-ttu-id="316d6-123">PhonebookServices</span><span class="sxs-lookup"><span data-stu-id="316d6-123">PhonebookServices</span></span>  <br/> |<span data-ttu-id="316d6-124">La información se obtuvo de los servicios de la libreta de teléfonos.</span><span class="sxs-lookup"><span data-stu-id="316d6-124">The information was obtained from phonebook services.</span></span>  <br/> |
|<span data-ttu-id="316d6-125">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="316d6-125">Device</span></span>  <br/> |<span data-ttu-id="316d6-126">La información se obtuvo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="316d6-126">The information was obtained from the device.</span></span>  <br/> |
|<span data-ttu-id="316d6-127">Contacto</span><span class="sxs-lookup"><span data-stu-id="316d6-127">Contact</span></span>  <br/> |<span data-ttu-id="316d6-128">La información se obtuvo de un contacto.</span><span class="sxs-lookup"><span data-stu-id="316d6-128">The information was obtained from a contact.</span></span>  <br/> |
|<span data-ttu-id="316d6-129">Resource</span><span class="sxs-lookup"><span data-stu-id="316d6-129">Resource</span></span>  <br/> |<span data-ttu-id="316d6-130">La información se obtuvo de un recurso.</span><span class="sxs-lookup"><span data-stu-id="316d6-130">The information was obtained from a resource.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="316d6-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="316d6-131">Remarks</span></span>

<span data-ttu-id="316d6-132">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="316d6-132">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="316d6-133">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="316d6-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  

