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
ms.openlocfilehash: f2f069717a5862adff3349090c35f95499d135f8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456958"
---
# <a name="entityextractionresult"></a><span data-ttu-id="af5eb-103">EntityExtractionResult</span><span class="sxs-lookup"><span data-stu-id="af5eb-103">EntityExtractionResult</span></span>

<span data-ttu-id="af5eb-104">El elemento **EntityExtractionResult** especifica la propiedad **EntityExtractionResult** de un elemento.</span><span class="sxs-lookup"><span data-stu-id="af5eb-104">The **EntityExtractionResult** element specifies the **EntityExtractionResult** property of an item.</span></span> 
  
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

 <span data-ttu-id="af5eb-105">**EntityExtractionResultType**</span><span class="sxs-lookup"><span data-stu-id="af5eb-105">**EntityExtractionResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="af5eb-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="af5eb-106">Attributes and elements</span></span>

<span data-ttu-id="af5eb-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="af5eb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af5eb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="af5eb-108">Attributes</span></span>

<span data-ttu-id="af5eb-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="af5eb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="af5eb-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="af5eb-110">Child elements</span></span>

|<span data-ttu-id="af5eb-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="af5eb-111">**Element**</span></span>|<span data-ttu-id="af5eb-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="af5eb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af5eb-113">Direcciones (ArrayOfAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="af5eb-113">Addresses (ArrayOfAddressEntitiesType)</span></span>](addresses-arrayofaddressentitiestype.md) <br/> |<span data-ttu-id="af5eb-114">Especifica una matriz de elementos **AddressEntity** .</span><span class="sxs-lookup"><span data-stu-id="af5eb-114">Specifies an array of **AddressEntity** elements.</span></span>  <br/> |
|[<span data-ttu-id="af5eb-115">MeetingSuggestions</span><span class="sxs-lookup"><span data-stu-id="af5eb-115">MeetingSuggestions</span></span>](meetingsuggestions.md) <br/> |<span data-ttu-id="af5eb-116">Especifica una matriz de elementos **MeetingSuggestion** .</span><span class="sxs-lookup"><span data-stu-id="af5eb-116">Specifies an array of **MeetingSuggestion** elements.</span></span>  <br/> |
|[<span data-ttu-id="af5eb-117">TaskSuggestions</span><span class="sxs-lookup"><span data-stu-id="af5eb-117">TaskSuggestions</span></span>](tasksuggestions.md) <br/> |<span data-ttu-id="af5eb-118">Especifica una matriz de elementos **TaskSuggestion** .</span><span class="sxs-lookup"><span data-stu-id="af5eb-118">Specifies an array of **TaskSuggestion** elements.</span></span>  <br/> |
|[<span data-ttu-id="af5eb-119">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="af5eb-119">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span></span>](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |<span data-ttu-id="af5eb-120">Especifica una matriz de entidades de direcciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="af5eb-120">Specifies an array of email address entities.</span></span>  <br/> |
|[<span data-ttu-id="af5eb-121">Contactos (ArrayOfContactsType)</span><span class="sxs-lookup"><span data-stu-id="af5eb-121">Contacts (ArrayOfContactsType)</span></span>](contacts-arrayofcontactstype.md) <br/> |<span data-ttu-id="af5eb-122">Especifica una matriz de contactos.</span><span class="sxs-lookup"><span data-stu-id="af5eb-122">Specifies an array of contacts.</span></span>  <br/> |
|[<span data-ttu-id="af5eb-123">Direcciones URL (ArrayOfUrlEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="af5eb-123">Urls (ArrayOfUrlEntitiesType)</span></span>](urls-arrayofurlentitiestype.md) <br/> |<span data-ttu-id="af5eb-124">Especifica una matriz de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="af5eb-124">Specifies an array of URLs.</span></span>  <br/> |
|[<span data-ttu-id="af5eb-125">PhoneNumbers (ArrayOfPhoneEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="af5eb-125">PhoneNumbers (ArrayOfPhoneEntitiesType)</span></span>](phonenumbers-arrayofphoneentitiestype.md) <br/> |<span data-ttu-id="af5eb-126">Especifica una matriz de números de teléfono.</span><span class="sxs-lookup"><span data-stu-id="af5eb-126">Specifies an array of phone numbers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="af5eb-127">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="af5eb-127">Parent elements</span></span>

|<span data-ttu-id="af5eb-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="af5eb-128">**Element**</span></span>|<span data-ttu-id="af5eb-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="af5eb-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af5eb-130">Item</span><span class="sxs-lookup"><span data-stu-id="af5eb-130">Item</span></span>](item.md) <br/> |<span data-ttu-id="af5eb-131">Representa un elemento genérico del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="af5eb-131">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af5eb-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="af5eb-132">Remarks</span></span>

<span data-ttu-id="af5eb-133">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="af5eb-133">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="af5eb-134">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="af5eb-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="af5eb-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="af5eb-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af5eb-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="af5eb-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="af5eb-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="af5eb-137">Schema Name</span></span>  <br/> |<span data-ttu-id="af5eb-138">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="af5eb-138">Type schema</span></span>  <br/> |
|<span data-ttu-id="af5eb-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="af5eb-139">Validation File</span></span>  <br/> |<span data-ttu-id="af5eb-140">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="af5eb-140">types.xsd</span></span>  <br/> |
|<span data-ttu-id="af5eb-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="af5eb-141">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="af5eb-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="af5eb-142">See also</span></span>



- [<span data-ttu-id="af5eb-143">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="af5eb-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

