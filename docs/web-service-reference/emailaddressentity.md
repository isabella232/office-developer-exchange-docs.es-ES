---
title: EmailAddressEntity
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20049467-c01a-4c7d-8ada-ca1801cc95ed
description: El elemento EmailAddressEntity especifica una entidad de dirección de correo electrónico única.
ms.openlocfilehash: c149ee69c1ed08c33d0341c8dfdac3bcda040afb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764348"
---
# <a name="emailaddressentity"></a><span data-ttu-id="2e31a-103">EmailAddressEntity</span><span class="sxs-lookup"><span data-stu-id="2e31a-103">EmailAddressEntity</span></span>

<span data-ttu-id="2e31a-104">El elemento **EmailAddressEntity** especifica una entidad de dirección de correo electrónico única.</span><span class="sxs-lookup"><span data-stu-id="2e31a-104">The **EmailAddressEntity** element specifies a single email address entity.</span></span> 
  
```XML
<EmailAddressEntity>
    <EmailAddress></EmailAddress>
</EmailAddressEntity>
```

 <span data-ttu-id="2e31a-105">**EmailAddressEntityType**</span><span class="sxs-lookup"><span data-stu-id="2e31a-105">**EmailAddressEntityType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2e31a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2e31a-106">Attributes and elements</span></span>

<span data-ttu-id="2e31a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2e31a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e31a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2e31a-108">Attributes</span></span>

<span data-ttu-id="2e31a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2e31a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2e31a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2e31a-110">Child elements</span></span>

|<span data-ttu-id="2e31a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2e31a-111">**Element**</span></span>|<span data-ttu-id="2e31a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e31a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e31a-113">EmailAddress (cadena)</span><span class="sxs-lookup"><span data-stu-id="2e31a-113">EmailAddress (string)</span></span>](emailaddress-string.md) <br/> |<span data-ttu-id="2e31a-114">Especifica una dirección de correo electrónico única.</span><span class="sxs-lookup"><span data-stu-id="2e31a-114">Specifies a single email address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2e31a-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2e31a-115">Parent elements</span></span>

|<span data-ttu-id="2e31a-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="2e31a-116">**Element**</span></span>|<span data-ttu-id="2e31a-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e31a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e31a-118">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="2e31a-118">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span></span>](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |<span data-ttu-id="2e31a-119">Especifica una matriz de entidades de la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="2e31a-119">Specifies an array of email address entities.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e31a-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2e31a-120">Remarks</span></span>

<span data-ttu-id="2e31a-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2e31a-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2e31a-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2e31a-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2e31a-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2e31a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e31a-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2e31a-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2e31a-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2e31a-125">Schema Name</span></span>  <br/> |<span data-ttu-id="2e31a-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="2e31a-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="2e31a-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2e31a-127">Validation File</span></span>  <br/> |<span data-ttu-id="2e31a-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2e31a-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2e31a-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2e31a-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2e31a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e31a-130">See also</span></span>



- [<span data-ttu-id="2e31a-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2e31a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

