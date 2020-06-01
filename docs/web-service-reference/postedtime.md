---
title: PostedTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PostedTime
api_type:
- schema
ms.assetid: e8b3813c-fc7e-4674-a4c6-6818c13d2bcf
description: El elemento PostedTime representa la hora en que se contabilizó un elemento PostItem. Este elemento es de sólo lectura. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 5fc670bfee97a46700bc4442d489696a4489f88a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459198"
---
# <a name="postedtime"></a><span data-ttu-id="fde14-105">PostedTime</span><span class="sxs-lookup"><span data-stu-id="fde14-105">PostedTime</span></span>

<span data-ttu-id="fde14-106">El elemento **PostedTime** representa la hora en que se contabilizó un [elemento PostItem](postitem.md) .</span><span class="sxs-lookup"><span data-stu-id="fde14-106">The **PostedTime** element represents the time at which a [PostItem](postitem.md) was posted.</span></span> <span data-ttu-id="fde14-107">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="fde14-107">This element is read-only.</span></span> <span data-ttu-id="fde14-108">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="fde14-108">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<PostedTime/>
```

 <span data-ttu-id="fde14-109">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="fde14-109">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fde14-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fde14-110">Attributes and elements</span></span>

<span data-ttu-id="fde14-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fde14-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fde14-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="fde14-112">Attributes</span></span>

<span data-ttu-id="fde14-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fde14-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fde14-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fde14-114">Child elements</span></span>

<span data-ttu-id="fde14-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fde14-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fde14-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fde14-116">Parent elements</span></span>

|<span data-ttu-id="fde14-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fde14-117">**Element**</span></span>|<span data-ttu-id="fde14-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fde14-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fde14-119">PostItem</span><span class="sxs-lookup"><span data-stu-id="fde14-119">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="fde14-120">Representa un postelemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fde14-120">Represents a PostItem in the Exchange store.</span></span> <span data-ttu-id="fde14-121">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="fde14-121">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fde14-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fde14-122">Text value</span></span>

<span data-ttu-id="fde14-123">El valor de texto es un dateTime que representa Cuándo se publicó un **elemento PostItem** .</span><span class="sxs-lookup"><span data-stu-id="fde14-123">The text value is a dateTime that represents when a **PostItem** was posted.</span></span> <span data-ttu-id="fde14-124">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="fde14-124">This property is read-only.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fde14-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fde14-125">Remarks</span></span>

<span data-ttu-id="fde14-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="fde14-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fde14-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fde14-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fde14-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="fde14-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fde14-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fde14-129">Schema Name</span></span>  <br/> |<span data-ttu-id="fde14-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fde14-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="fde14-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fde14-131">Validation File</span></span>  <br/> |<span data-ttu-id="fde14-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="fde14-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fde14-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fde14-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="fde14-134">Falso</span><span class="sxs-lookup"><span data-stu-id="fde14-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fde14-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="fde14-135">See also</span></span>



- [<span data-ttu-id="fde14-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fde14-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

