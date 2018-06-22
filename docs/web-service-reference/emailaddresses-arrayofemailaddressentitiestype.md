---
title: EmailAddresses (ArrayOfEmailAddressEntitiesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2fc4a8e8-5377-4059-8fb4-3fdabfd30fe3
description: El elemento EmailAddresses especifica una matriz de entidades de la dirección de correo electrónico.
ms.openlocfilehash: 8d96d49ef2420f269197e47577efb956daa64e53
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764347"
---
# <a name="emailaddresses-arrayofemailaddressentitiestype"></a><span data-ttu-id="12954-103">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="12954-103">EmailAddresses (ArrayOfEmailAddressEntitiesType)</span></span>

<span data-ttu-id="12954-104">El elemento **EmailAddresses** especifica una matriz de entidades de la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="12954-104">The **EmailAddresses** element specifies an array of email address entities.</span></span> 
  
```XML
<EmailAddresses>
    <EmailAddressEntity></EmailAddressEntity>
</EmailAddresses>
```

 <span data-ttu-id="12954-105">**ArrayOfEmailAddressEntitiesType**</span><span class="sxs-lookup"><span data-stu-id="12954-105">**ArrayOfEmailAddressEntitiesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="12954-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="12954-106">Attributes and elements</span></span>

<span data-ttu-id="12954-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="12954-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="12954-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="12954-108">Attributes</span></span>

<span data-ttu-id="12954-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="12954-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="12954-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="12954-110">Child elements</span></span>

|<span data-ttu-id="12954-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="12954-111">**Element**</span></span>|<span data-ttu-id="12954-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="12954-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12954-113">EmailAddressEntity</span><span class="sxs-lookup"><span data-stu-id="12954-113">EmailAddressEntity</span></span>](emailaddressentity.md) <br/> |<span data-ttu-id="12954-114">Especifica una entidad de dirección de correo electrónico única.</span><span class="sxs-lookup"><span data-stu-id="12954-114">Specifies a single email address entity.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="12954-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="12954-115">Parent elements</span></span>

|<span data-ttu-id="12954-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="12954-116">**Element**</span></span>|<span data-ttu-id="12954-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="12954-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12954-118">EntityExtractionResult</span><span class="sxs-lookup"><span data-stu-id="12954-118">EntityExtractionResult</span></span>](entityextractionresult.md) <br/> |<span data-ttu-id="12954-119">Especifica la propiedad **EntityExtractionResult** de un elemento.</span><span class="sxs-lookup"><span data-stu-id="12954-119">Specifies the **EntityExtractionResult** property of an item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12954-120">Notas</span><span class="sxs-lookup"><span data-stu-id="12954-120">Remarks</span></span>

<span data-ttu-id="12954-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="12954-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="12954-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="12954-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="12954-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="12954-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12954-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="12954-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="12954-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="12954-125">Schema Name</span></span>  <br/> |<span data-ttu-id="12954-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="12954-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="12954-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="12954-127">Validation File</span></span>  <br/> |<span data-ttu-id="12954-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="12954-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="12954-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="12954-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="12954-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="12954-130">See also</span></span>



- [<span data-ttu-id="12954-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="12954-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

