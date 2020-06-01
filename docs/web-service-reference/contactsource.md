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
description: El elemento ContactSource describe si el contacto se encuentra en el almacén de Exchange o en los servicios de dominio de Active Directory (AD DS).
ms.openlocfilehash: 5447dedf199c5ad6b944aa33e6dca03e83a3c340
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462713"
---
# <a name="contactsource"></a><span data-ttu-id="c0b4d-103">ContactSource</span><span class="sxs-lookup"><span data-stu-id="c0b4d-103">ContactSource</span></span>

<span data-ttu-id="c0b4d-104">El elemento **ContactSource** describe si el contacto se encuentra en el almacén de Exchange o en los servicios de dominio de Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="c0b4d-104">The **ContactSource** element describes whether the contact is located in the Exchange store or Active Directory Domain Services (AD DS).</span></span> 
  
```xml
<ContactSource/>
```

 <span data-ttu-id="c0b4d-105">**ContactSourceType**</span><span class="sxs-lookup"><span data-stu-id="c0b4d-105">**ContactSourceType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c0b4d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c0b4d-106">Attributes and elements</span></span>

<span data-ttu-id="c0b4d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c0b4d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0b4d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c0b4d-108">Attributes</span></span>

<span data-ttu-id="c0b4d-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c0b4d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c0b4d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c0b4d-110">Child elements</span></span>

<span data-ttu-id="c0b4d-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c0b4d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c0b4d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c0b4d-112">Parent elements</span></span>

|<span data-ttu-id="c0b4d-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c0b4d-113">**Element**</span></span>|<span data-ttu-id="c0b4d-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c0b4d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0b4d-115">Contacto</span><span class="sxs-lookup"><span data-stu-id="c0b4d-115">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="c0b4d-116">Representa un elemento de contacto en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c0b4d-116">Represents a contact item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c0b4d-117">DistributionList</span><span class="sxs-lookup"><span data-stu-id="c0b4d-117">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="c0b4d-118">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="c0b4d-118">Represents a distribution list.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c0b4d-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c0b4d-119">Text value</span></span>

<span data-ttu-id="c0b4d-120">A continuación se muestran los valores posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="c0b4d-120">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="c0b4d-121">Directory</span><span class="sxs-lookup"><span data-stu-id="c0b4d-121">ActiveDirectory</span></span>
    
- <span data-ttu-id="c0b4d-122">Tienda</span><span class="sxs-lookup"><span data-stu-id="c0b4d-122">Store</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0b4d-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c0b4d-123">Remarks</span></span>

<span data-ttu-id="c0b4d-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c0b4d-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0b4d-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c0b4d-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0b4d-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="c0b4d-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c0b4d-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c0b4d-127">Schema name</span></span>  <br/> |<span data-ttu-id="c0b4d-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c0b4d-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="c0b4d-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c0b4d-129">Validation file</span></span>  <br/> |<span data-ttu-id="c0b4d-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c0b4d-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c0b4d-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c0b4d-131">Can be empty</span></span>  <br/> |<span data-ttu-id="c0b4d-132">Falso</span><span class="sxs-lookup"><span data-stu-id="c0b4d-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0b4d-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0b4d-133">See also</span></span>



- [<span data-ttu-id="c0b4d-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c0b4d-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

