---
title: EntityExtractionResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 643b99ab-ff90-4411-864c-1077623028d6
description: El elemento EntityExtractionResult especifica la propiedad EntityExtractionResult de un elemento.
ms.openlocfilehash: ef99629beb95f1e1123569fa99e3f495c1b56e95
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764429"
---
# <a name="entityextractionresult"></a><span data-ttu-id="ad4b7-103">EntityExtractionResult</span><span class="sxs-lookup"><span data-stu-id="ad4b7-103">EntityExtractionResult</span></span>

<span data-ttu-id="ad4b7-104">El elemento **EntityExtractionResult** especifica la propiedad **EntityExtractionResult** de un elemento.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-104">The **EntityExtractionResult** element specifies the **EntityExtractionResult** property of an item.</span></span> 
  
```XML
<EntityExtractionResult>
    <Addresses/>
    <MeetingSuggestions/>
    <TaskSuggestions/>
    <EmailAddresses/>
    <Contacts/>
    <Urls/>
    <PhoneNumbers/>
</EntityExtractionResult>
```

 <span data-ttu-id="ad4b7-105">**EntityExtractionResultType**</span><span class="sxs-lookup"><span data-stu-id="ad4b7-105">**EntityExtractionResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ad4b7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ad4b7-106">Attributes and elements</span></span>

<span data-ttu-id="ad4b7-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad4b7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ad4b7-108">Attributes</span></span>

<span data-ttu-id="ad4b7-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ad4b7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ad4b7-110">Child elements</span></span>

|<span data-ttu-id="ad4b7-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad4b7-111">**Element**</span></span>|<span data-ttu-id="ad4b7-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad4b7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad4b7-113">Direcciones (ArrayOfAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="ad4b7-113">Addresses (ArrayOfAddressEntitiesType)</span></span>](addresses-arrayofaddressentitiestype.md) <br/> |<span data-ttu-id="ad4b7-114">Especifica una matriz de elementos de **AddressEntity** .</span><span class="sxs-lookup"><span data-stu-id="ad4b7-114">Specifies an array of **AddressEntity** elements.</span></span>  <br/> |
|[<span data-ttu-id="ad4b7-115">MeetingSuggestions</span><span class="sxs-lookup"><span data-stu-id="ad4b7-115">MeetingSuggestions</span></span>](meetingsuggestions.md) <br/> |<span data-ttu-id="ad4b7-116">Especifica una matriz de elementos de **MeetingSuggestion** .</span><span class="sxs-lookup"><span data-stu-id="ad4b7-116">Specifies an array of **MeetingSuggestion** elements.</span></span>  <br/> |
|[<span data-ttu-id="ad4b7-117">TaskSuggestions</span><span class="sxs-lookup"><span data-stu-id="ad4b7-117">TaskSuggestions</span></span>](tasksuggestions.md) <br/> |<span data-ttu-id="ad4b7-118">Especifica una matriz de elementos de **TaskSuggestion** .</span><span class="sxs-lookup"><span data-stu-id="ad4b7-118">Specifies an array of **TaskSuggestion** elements.</span></span>  <br/> |
|[<span data-ttu-id="ad4b7-119">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="ad4b7-119">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span></span>](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |<span data-ttu-id="ad4b7-120">Especifica una matriz de entidades de la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-120">Specifies an array of email address entities.</span></span>  <br/> |
|[<span data-ttu-id="ad4b7-121">Contactos (ArrayOfContactsType)</span><span class="sxs-lookup"><span data-stu-id="ad4b7-121">Contacts (ArrayOfContactsType)</span></span>](contacts-arrayofcontactstype.md) <br/> |<span data-ttu-id="ad4b7-122">Especifica una matriz de los contactos.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-122">Specifies an array of contacts.</span></span>  <br/> |
|[<span data-ttu-id="ad4b7-123">Direcciones URL (ArrayOfUrlEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="ad4b7-123">Urls (ArrayOfUrlEntitiesType)</span></span>](urls-arrayofurlentitiestype.md) <br/> |<span data-ttu-id="ad4b7-124">Especifica una matriz de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-124">Specifies an array of URLs.</span></span>  <br/> |
|[<span data-ttu-id="ad4b7-125">PhoneNumbers (ArrayOfPhoneEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="ad4b7-125">PhoneNumbers (ArrayOfPhoneEntitiesType)</span></span>](phonenumbers-arrayofphoneentitiestype.md) <br/> |<span data-ttu-id="ad4b7-126">Especifica una matriz de números de teléfono.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-126">Specifies an array of phone numbers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ad4b7-127">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ad4b7-127">Parent elements</span></span>

|<span data-ttu-id="ad4b7-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad4b7-128">**Element**</span></span>|<span data-ttu-id="ad4b7-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad4b7-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad4b7-130">Item</span><span class="sxs-lookup"><span data-stu-id="ad4b7-130">Item</span></span>](item.md) <br/> |<span data-ttu-id="ad4b7-131">Representa un elemento genérico en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-131">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad4b7-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad4b7-132">Remarks</span></span>

<span data-ttu-id="ad4b7-133">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-133">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ad4b7-134">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ad4b7-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad4b7-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ad4b7-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad4b7-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ad4b7-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ad4b7-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ad4b7-137">Schema Name</span></span>  <br/> |<span data-ttu-id="ad4b7-138">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="ad4b7-138">Type schema</span></span>  <br/> |
|<span data-ttu-id="ad4b7-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ad4b7-139">Validation File</span></span>  <br/> |<span data-ttu-id="ad4b7-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ad4b7-140">types.xsd</span></span>  <br/> |
|<span data-ttu-id="ad4b7-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ad4b7-141">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ad4b7-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad4b7-142">See also</span></span>



- [<span data-ttu-id="ad4b7-143">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ad4b7-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

