---
title: Contacto (ContactType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7f7119b7-f5b4-484d-a7de-fa74836d9aee
description: El elemento Contact especifica un contacto en el almacén de contactos unificados.
ms.openlocfilehash: e8ebc28456f8bfc26f5d790ac9ff278930041ea0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461523"
---
# <a name="contact-contacttype"></a><span data-ttu-id="822d0-103">Contacto (ContactType)</span><span class="sxs-lookup"><span data-stu-id="822d0-103">Contact (ContactType)</span></span>

<span data-ttu-id="822d0-104">El elemento **Contact** especifica un contacto en el almacén de contactos unificados.</span><span class="sxs-lookup"><span data-stu-id="822d0-104">The **Contact** element specifies a contact in the Unified Contact Store.</span></span> 
  
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

 <span data-ttu-id="822d0-105">**ContactType**</span><span class="sxs-lookup"><span data-stu-id="822d0-105">**ContactType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="822d0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="822d0-106">Attributes and elements</span></span>

<span data-ttu-id="822d0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="822d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="822d0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="822d0-108">Attributes</span></span>

<span data-ttu-id="822d0-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="822d0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="822d0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="822d0-110">Child elements</span></span>

|<span data-ttu-id="822d0-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="822d0-111">**Element**</span></span>|<span data-ttu-id="822d0-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="822d0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="822d0-113">PersonName</span><span class="sxs-lookup"><span data-stu-id="822d0-113">PersonName</span></span>](personname.md) <br/> |<span data-ttu-id="822d0-114">Especifica el nombre de una persona.</span><span class="sxs-lookup"><span data-stu-id="822d0-114">Specifies the name of an individual.</span></span>  <br/> |
|[<span data-ttu-id="822d0-115">BusinessName</span><span class="sxs-lookup"><span data-stu-id="822d0-115">BusinessName</span></span>](businessname.md) <br/> |<span data-ttu-id="822d0-116">Especifica el nombre de una empresa.</span><span class="sxs-lookup"><span data-stu-id="822d0-116">Specifies the name of a business.</span></span>  <br/> |
|[<span data-ttu-id="822d0-117">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="822d0-117">PhoneNumbers</span></span>](phonenumbers.md) <br/> |<span data-ttu-id="822d0-118">Representa una colección de números de teléfono de un contacto.</span><span class="sxs-lookup"><span data-stu-id="822d0-118">Represents a collection of telephone numbers for a contact.</span></span>  <br/> |
|[<span data-ttu-id="822d0-119">Urls</span><span class="sxs-lookup"><span data-stu-id="822d0-119">Urls</span></span>](urls.md) <br/> |<span data-ttu-id="822d0-120">Especifica una matriz de direcciones URL para un rol.</span><span class="sxs-lookup"><span data-stu-id="822d0-120">Specifies an array of URLs for a persona.</span></span>  <br/> |
|[<span data-ttu-id="822d0-121">EmailAddresses (ArrayOfExtractedEmailAddresses)</span><span class="sxs-lookup"><span data-stu-id="822d0-121">EmailAddresses (ArrayOfExtractedEmailAddresses)</span></span>](emailaddresses-arrayofextractedemailaddresses.md) <br/> |<span data-ttu-id="822d0-122">Especifica una matriz de direcciones de correo electrónico extraídas.</span><span class="sxs-lookup"><span data-stu-id="822d0-122">Specifies an array of extracted email addresses.</span></span>  <br/> |
|[<span data-ttu-id="822d0-123">Direcciones (ArrayOfAddressesType)</span><span class="sxs-lookup"><span data-stu-id="822d0-123">Addresses (ArrayOfAddressesType)</span></span>](addresses-arrayofaddressestype.md) <br/> |<span data-ttu-id="822d0-124">Especifica una matriz de elementos **Address** .</span><span class="sxs-lookup"><span data-stu-id="822d0-124">Specifies an array of **Address** elements.</span></span>  <br/> |
|[<span data-ttu-id="822d0-125">ContactString</span><span class="sxs-lookup"><span data-stu-id="822d0-125">ContactString</span></span>](contactstring.md) <br/> |<span data-ttu-id="822d0-126">Especifica el nombre para mostrar de un contacto.</span><span class="sxs-lookup"><span data-stu-id="822d0-126">Specifies the display name of a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="822d0-127">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="822d0-127">Parent elements</span></span>

|<span data-ttu-id="822d0-128">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="822d0-128">**Element**</span></span>|<span data-ttu-id="822d0-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="822d0-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="822d0-130">Contactos (ArrayOfContactsType)</span><span class="sxs-lookup"><span data-stu-id="822d0-130">Contacts (ArrayOfContactsType)</span></span>](contacts-arrayofcontactstype.md) <br/> |<span data-ttu-id="822d0-131">Especifica una matriz de contactos.</span><span class="sxs-lookup"><span data-stu-id="822d0-131">Specifies an array of contacts.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="822d0-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="822d0-132">Remarks</span></span>

<span data-ttu-id="822d0-133">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="822d0-133">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="822d0-134">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="822d0-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="822d0-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="822d0-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="822d0-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="822d0-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="822d0-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="822d0-137">Schema Name</span></span>  <br/> |<span data-ttu-id="822d0-138">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="822d0-138">Type schema</span></span>  <br/> |
|<span data-ttu-id="822d0-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="822d0-139">Validation File</span></span>  <br/> |<span data-ttu-id="822d0-140">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="822d0-140">types.xsd</span></span>  <br/> |
|<span data-ttu-id="822d0-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="822d0-141">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="822d0-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="822d0-142">See also</span></span>



- [<span data-ttu-id="822d0-143">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="822d0-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

