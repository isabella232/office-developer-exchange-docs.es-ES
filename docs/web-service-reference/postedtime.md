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
description: El elemento PostedTime representa la hora a la que se ha registrado un objeto PostItem. Este elemento es de sólo lectura. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 8280fc26c534b280d0f30f663b6cc3a3958036c5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836860"
---
# <a name="postedtime"></a><span data-ttu-id="ad87f-105">PostedTime</span><span class="sxs-lookup"><span data-stu-id="ad87f-105">PostedTime</span></span>

<span data-ttu-id="ad87f-106">El elemento **PostedTime** representa la hora a la que se ha registrado un [objeto PostItem](postitem.md) .</span><span class="sxs-lookup"><span data-stu-id="ad87f-106">The **PostedTime** element represents the time at which a [PostItem](postitem.md) was posted.</span></span> <span data-ttu-id="ad87f-107">Este elemento es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="ad87f-107">This element is read-only.</span></span> <span data-ttu-id="ad87f-108">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ad87f-108">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<PostedTime/>
```

 <span data-ttu-id="ad87f-109">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="ad87f-109">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ad87f-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ad87f-110">Attributes and elements</span></span>

<span data-ttu-id="ad87f-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ad87f-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad87f-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="ad87f-112">Attributes</span></span>

<span data-ttu-id="ad87f-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ad87f-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ad87f-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ad87f-114">Child elements</span></span>

<span data-ttu-id="ad87f-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ad87f-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ad87f-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ad87f-116">Parent elements</span></span>

|<span data-ttu-id="ad87f-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ad87f-117">**Element**</span></span>|<span data-ttu-id="ad87f-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ad87f-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ad87f-119">Objeto postItem</span><span class="sxs-lookup"><span data-stu-id="ad87f-119">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="ad87f-120">Representa un objeto PostItem en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ad87f-120">Represents a PostItem in the Exchange store.</span></span> <span data-ttu-id="ad87f-121">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="ad87f-121">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ad87f-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ad87f-122">Text value</span></span>

<span data-ttu-id="ad87f-123">El valor de texto es un valor de tipo dateTime que representa al registra un **objeto PostItem** .</span><span class="sxs-lookup"><span data-stu-id="ad87f-123">The text value is a dateTime that represents when a **PostItem** was posted.</span></span> <span data-ttu-id="ad87f-124">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="ad87f-124">This property is read-only.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ad87f-125">Notas</span><span class="sxs-lookup"><span data-stu-id="ad87f-125">Remarks</span></span>

<span data-ttu-id="ad87f-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="ad87f-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad87f-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ad87f-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad87f-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ad87f-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ad87f-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ad87f-129">Schema Name</span></span>  <br/> |<span data-ttu-id="ad87f-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ad87f-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="ad87f-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ad87f-131">Validation File</span></span>  <br/> |<span data-ttu-id="ad87f-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ad87f-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ad87f-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ad87f-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="ad87f-134">False</span><span class="sxs-lookup"><span data-stu-id="ad87f-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad87f-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="ad87f-135">See also</span></span>



- [<span data-ttu-id="ad87f-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ad87f-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

