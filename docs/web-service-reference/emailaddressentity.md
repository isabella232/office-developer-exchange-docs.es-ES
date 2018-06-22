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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764348"
---
# <a name="emailaddressentity"></a><span data-ttu-id="0d57f-103">EmailAddressEntity</span><span class="sxs-lookup"><span data-stu-id="0d57f-103">EmailAddressEntity</span></span>

<span data-ttu-id="0d57f-104">El elemento **EmailAddressEntity** especifica una entidad de dirección de correo electrónico única.</span><span class="sxs-lookup"><span data-stu-id="0d57f-104">The **EmailAddressEntity** element specifies a single email address entity.</span></span> 
  
```XML
<EmailAddressEntity>
    <EmailAddress></EmailAddress>
</EmailAddressEntity>
```

 <span data-ttu-id="0d57f-105">**EmailAddressEntityType**</span><span class="sxs-lookup"><span data-stu-id="0d57f-105">**EmailAddressEntityType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0d57f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0d57f-106">Attributes and elements</span></span>

<span data-ttu-id="0d57f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0d57f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d57f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0d57f-108">Attributes</span></span>

<span data-ttu-id="0d57f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0d57f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0d57f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0d57f-110">Child elements</span></span>

|<span data-ttu-id="0d57f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d57f-111">**Element**</span></span>|<span data-ttu-id="0d57f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0d57f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d57f-113">EmailAddress (cadena)</span><span class="sxs-lookup"><span data-stu-id="0d57f-113">EmailAddress (string)</span></span>](emailaddress-string.md) <br/> |<span data-ttu-id="0d57f-114">Especifica una dirección de correo electrónico única.</span><span class="sxs-lookup"><span data-stu-id="0d57f-114">Specifies a single email address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0d57f-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0d57f-115">Parent elements</span></span>

|<span data-ttu-id="0d57f-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d57f-116">**Element**</span></span>|<span data-ttu-id="0d57f-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0d57f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d57f-118">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="0d57f-118">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span></span>](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |<span data-ttu-id="0d57f-119">Especifica una matriz de entidades de la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="0d57f-119">Specifies an array of email address entities.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d57f-120">Notas</span><span class="sxs-lookup"><span data-stu-id="0d57f-120">Remarks</span></span>

<span data-ttu-id="0d57f-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0d57f-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0d57f-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0d57f-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0d57f-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0d57f-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d57f-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0d57f-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0d57f-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0d57f-125">Schema Name</span></span>  <br/> |<span data-ttu-id="0d57f-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="0d57f-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="0d57f-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0d57f-127">Validation File</span></span>  <br/> |<span data-ttu-id="0d57f-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0d57f-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="0d57f-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0d57f-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0d57f-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="0d57f-130">See also</span></span>



- [<span data-ttu-id="0d57f-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0d57f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

