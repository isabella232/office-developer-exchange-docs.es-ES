---
title: EmailAddresses (ArrayOfEmailAddressesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 95084659-aa5a-4bac-8977-00db3b87883e
description: El elemento EmailAddresses especifica una matriz de todas las direcciones de correo electrónico del rol asociado.
ms.openlocfilehash: e6132e9ef4ed13ea2546783f65d184fafeed5530
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463422"
---
# <a name="emailaddresses-arrayofemailaddressestype"></a><span data-ttu-id="384cd-103">EmailAddresses (ArrayOfEmailAddressesType)</span><span class="sxs-lookup"><span data-stu-id="384cd-103">EmailAddresses (ArrayOfEmailAddressesType)</span></span>

<span data-ttu-id="384cd-104">El elemento **EmailAddresses** especifica una matriz de todas las direcciones de correo electrónico del rol asociado.</span><span class="sxs-lookup"><span data-stu-id="384cd-104">The **EmailAddresses** element specifies an array of all email addresses of the associated persona.</span></span> 
  
```XML
<EmailAddresses>
    <Address></Address>
</EmailAddresses>
```

 <span data-ttu-id="384cd-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="384cd-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="384cd-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="384cd-106">Attributes and elements</span></span>

<span data-ttu-id="384cd-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="384cd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="384cd-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="384cd-108">Attributes</span></span>

<span data-ttu-id="384cd-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="384cd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="384cd-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="384cd-110">Child elements</span></span>

|<span data-ttu-id="384cd-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="384cd-111">**Element**</span></span>|<span data-ttu-id="384cd-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="384cd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="384cd-113">Dirección (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="384cd-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="384cd-114">Representa una dirección de correo electrónico completamente resuelta.</span><span class="sxs-lookup"><span data-stu-id="384cd-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="384cd-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="384cd-115">Parent elements</span></span>

|<span data-ttu-id="384cd-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="384cd-116">**Element**</span></span>|<span data-ttu-id="384cd-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="384cd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="384cd-118">Rol</span><span class="sxs-lookup"><span data-stu-id="384cd-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="384cd-119">Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="384cd-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="384cd-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="384cd-120">Remarks</span></span>

<span data-ttu-id="384cd-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="384cd-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="384cd-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="384cd-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="384cd-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="384cd-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="384cd-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="384cd-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="384cd-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="384cd-125">Schema Name</span></span>  <br/> |<span data-ttu-id="384cd-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="384cd-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="384cd-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="384cd-127">Validation File</span></span>  <br/> |<span data-ttu-id="384cd-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="384cd-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="384cd-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="384cd-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="384cd-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="384cd-130">See also</span></span>



- [<span data-ttu-id="384cd-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="384cd-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

