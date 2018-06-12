---
title: Contacto (ContactType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7f7119b7-f5b4-484d-a7de-fa74836d9aee
description: El elemento de contacto, especifica un contacto en el almacén de contactos unificados.
ms.openlocfilehash: f1593da78a46851c7db43abc567eb66c0c74e0f2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763784"
---
# <a name="contact-contacttype"></a><span data-ttu-id="3966b-103">Contacto (ContactType)</span><span class="sxs-lookup"><span data-stu-id="3966b-103">Contact (ContactType)</span></span>

<span data-ttu-id="3966b-104">El elemento **de contacto** , especifica un contacto en el almacén de contactos unificados.</span><span class="sxs-lookup"><span data-stu-id="3966b-104">The **Contact** element specifies a contact in the Unified Contact Store.</span></span> 
  
```XML
<Contact>
    <PersonName></PersonName>
    <BusinessName></BusinessName>
    <PhoneNumbers></PhoneNumbers>
    <Urls></Urls>
    <EmailAddresses></EmailAddresses>
    <Addresses></Addesses>    <ContactString></ContactString
</Contact>
```

 <span data-ttu-id="3966b-105">**ContactType**</span><span class="sxs-lookup"><span data-stu-id="3966b-105">**ContactType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3966b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3966b-106">Attributes and elements</span></span>

<span data-ttu-id="3966b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3966b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3966b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3966b-108">Attributes</span></span>

<span data-ttu-id="3966b-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3966b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3966b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3966b-110">Child elements</span></span>

|<span data-ttu-id="3966b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3966b-111">**Element**</span></span>|<span data-ttu-id="3966b-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3966b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3966b-113">PersonName</span><span class="sxs-lookup"><span data-stu-id="3966b-113">PersonName</span></span>](personname.md) <br/> |<span data-ttu-id="3966b-114">Especifica el nombre de un individuo.</span><span class="sxs-lookup"><span data-stu-id="3966b-114">Specifies the name of an individual.</span></span>  <br/> |
|[<span data-ttu-id="3966b-115">BusinessName</span><span class="sxs-lookup"><span data-stu-id="3966b-115">BusinessName</span></span>](businessname.md) <br/> |<span data-ttu-id="3966b-116">Especifica el nombre de una empresa.</span><span class="sxs-lookup"><span data-stu-id="3966b-116">Specifies the name of a business.</span></span>  <br/> |
|[<span data-ttu-id="3966b-117">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="3966b-117">PhoneNumbers</span></span>](phonenumbers.md) <br/> |<span data-ttu-id="3966b-118">Representa una colección de números de teléfono de un contacto.</span><span class="sxs-lookup"><span data-stu-id="3966b-118">Represents a collection of telephone numbers for a contact.</span></span>  <br/> |
|[<span data-ttu-id="3966b-119">Direcciones URL</span><span class="sxs-lookup"><span data-stu-id="3966b-119">Urls</span></span>](urls.md) <br/> |<span data-ttu-id="3966b-120">Especifica una matriz de direcciones URL para un rol.</span><span class="sxs-lookup"><span data-stu-id="3966b-120">Specifies an array of URLs for a persona.</span></span>  <br/> |
|[<span data-ttu-id="3966b-121">EmailAddresses (ArrayOfExtractedEmailAddresses)</span><span class="sxs-lookup"><span data-stu-id="3966b-121">EmailAddresses (ArrayOfExtractedEmailAddresses)</span></span>](emailaddresses-arrayofextractedemailaddresses.md) <br/> |<span data-ttu-id="3966b-122">Especifica una matriz de direcciones de correo electrónico extraídos.</span><span class="sxs-lookup"><span data-stu-id="3966b-122">Specifies an array of extracted email addresses.</span></span>  <br/> |
|[<span data-ttu-id="3966b-123">Direcciones (ArrayOfAddressesType)</span><span class="sxs-lookup"><span data-stu-id="3966b-123">Addresses (ArrayOfAddressesType)</span></span>](addresses-arrayofaddressestype.md) <br/> |<span data-ttu-id="3966b-124">Especifica una matriz de elementos de la **dirección** .</span><span class="sxs-lookup"><span data-stu-id="3966b-124">Specifies an array of **Address** elements.</span></span>  <br/> |
|[<span data-ttu-id="3966b-125">ContactString</span><span class="sxs-lookup"><span data-stu-id="3966b-125">ContactString</span></span>](contactstring.md) <br/> |<span data-ttu-id="3966b-126">Especifica el nombre para mostrar de un contacto.</span><span class="sxs-lookup"><span data-stu-id="3966b-126">Specifies the display name of a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3966b-127">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3966b-127">Parent elements</span></span>

|<span data-ttu-id="3966b-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="3966b-128">**Element**</span></span>|<span data-ttu-id="3966b-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3966b-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3966b-130">Contactos (ArrayOfContactsType)</span><span class="sxs-lookup"><span data-stu-id="3966b-130">Contacts (ArrayOfContactsType)</span></span>](contacts-arrayofcontactstype.md) <br/> |<span data-ttu-id="3966b-131">Especifica una matriz de los contactos.</span><span class="sxs-lookup"><span data-stu-id="3966b-131">Specifies an array of contacts.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3966b-132">Notas</span><span class="sxs-lookup"><span data-stu-id="3966b-132">Remarks</span></span>

<span data-ttu-id="3966b-133">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3966b-133">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3966b-134">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3966b-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3966b-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3966b-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3966b-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3966b-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3966b-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3966b-137">Schema Name</span></span>  <br/> |<span data-ttu-id="3966b-138">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="3966b-138">Type schema</span></span>  <br/> |
|<span data-ttu-id="3966b-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3966b-139">Validation File</span></span>  <br/> |<span data-ttu-id="3966b-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3966b-140">types.xsd</span></span>  <br/> |
|<span data-ttu-id="3966b-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3966b-141">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3966b-142">Ver también</span><span class="sxs-lookup"><span data-stu-id="3966b-142">See also</span></span>



- [<span data-ttu-id="3966b-143">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3966b-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

