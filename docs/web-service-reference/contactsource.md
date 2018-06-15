---
title: ContactSource
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContactSource
api_type:
- schema
ms.assetid: 500b0423-864e-4cde-a39b-6b5b06d1aa6a
description: El elemento ContactSource describe si el contacto se encuentra en el almacén de Exchange o los servicios de dominio de Active Directory (AD DS).
ms.openlocfilehash: a82b766fc81b9397fc707415ea82e2f2d63d952d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763799"
---
# <a name="contactsource"></a><span data-ttu-id="f3c28-103">ContactSource</span><span class="sxs-lookup"><span data-stu-id="f3c28-103">ContactSource</span></span>

<span data-ttu-id="f3c28-104">El elemento **ContactSource** describe si el contacto se encuentra en el almacén de Exchange o los servicios de dominio de Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="f3c28-104">The **ContactSource** element describes whether the contact is located in the Exchange store or Active Directory Domain Services (AD DS).</span></span> 
  
```xml
<ContactSource/>
```

 <span data-ttu-id="f3c28-105">**ContactSourceType**</span><span class="sxs-lookup"><span data-stu-id="f3c28-105">**ContactSourceType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f3c28-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f3c28-106">Attributes and elements</span></span>

<span data-ttu-id="f3c28-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f3c28-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f3c28-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f3c28-108">Attributes</span></span>

<span data-ttu-id="f3c28-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f3c28-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f3c28-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f3c28-110">Child elements</span></span>

<span data-ttu-id="f3c28-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f3c28-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f3c28-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f3c28-112">Parent elements</span></span>

|<span data-ttu-id="f3c28-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f3c28-113">**Element**</span></span>|<span data-ttu-id="f3c28-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f3c28-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f3c28-115">Contact</span><span class="sxs-lookup"><span data-stu-id="f3c28-115">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="f3c28-116">Representa un elemento de contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f3c28-116">Represents a contact item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f3c28-117">DistributionList</span><span class="sxs-lookup"><span data-stu-id="f3c28-117">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="f3c28-118">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="f3c28-118">Represents a distribution list.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f3c28-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f3c28-119">Text value</span></span>

<span data-ttu-id="f3c28-120">Los siguientes son los valores posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="f3c28-120">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="f3c28-121">ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="f3c28-121">ActiveDirectory</span></span>
    
- <span data-ttu-id="f3c28-122">Tienda</span><span class="sxs-lookup"><span data-stu-id="f3c28-122">Store</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f3c28-123">Notas</span><span class="sxs-lookup"><span data-stu-id="f3c28-123">Remarks</span></span>

<span data-ttu-id="f3c28-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f3c28-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f3c28-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f3c28-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3c28-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f3c28-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f3c28-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f3c28-127">Schema name</span></span>  <br/> |<span data-ttu-id="f3c28-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f3c28-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="f3c28-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f3c28-129">Validation file</span></span>  <br/> |<span data-ttu-id="f3c28-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f3c28-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f3c28-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f3c28-131">Can be empty</span></span>  <br/> |<span data-ttu-id="f3c28-132">False</span><span class="sxs-lookup"><span data-stu-id="f3c28-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f3c28-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="f3c28-133">See also</span></span>



- [<span data-ttu-id="f3c28-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f3c28-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
