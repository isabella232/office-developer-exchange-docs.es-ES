---
title: ProposeNewTime
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6d5977ac-484e-4e53-92ba-58a868eb3395
description: El elemento ProposeNewTime especifica un objeto de respuesta que indica que el Asistente de la reunión puede proponer una nueva hora de reunión.
ms.openlocfilehash: 4a0238d94b29993def8009fae62380bb2c02e8b6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836904"
---
# <a name="proposenewtime"></a><span data-ttu-id="0b98d-103">ProposeNewTime</span><span class="sxs-lookup"><span data-stu-id="0b98d-103">ProposeNewTime</span></span>

<span data-ttu-id="0b98d-104">El elemento **ProposeNewTime** especifica un objeto de respuesta que indica que el Asistente de la reunión puede proponer una nueva hora de reunión.</span><span class="sxs-lookup"><span data-stu-id="0b98d-104">The **ProposeNewTime** element specifies a response object that indicates that the meeting attendee can propose a new meeting time.</span></span> 
  
```XML
<ProposeNewTime ObjectName=""></ProposeNewTime>
```

 <span data-ttu-id="0b98d-105">**ProposeNewTimeType**</span><span class="sxs-lookup"><span data-stu-id="0b98d-105">**ProposeNewTimeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0b98d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0b98d-106">Attributes and elements</span></span>

<span data-ttu-id="0b98d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0b98d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0b98d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0b98d-108">Attributes</span></span>

****

|<span data-ttu-id="0b98d-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="0b98d-109">**Attribute**</span></span>|<span data-ttu-id="0b98d-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0b98d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0b98d-111">ObjectName</span><span class="sxs-lookup"><span data-stu-id="0b98d-111">ObjectName</span></span>  <br/> |<span data-ttu-id="0b98d-112">El nombre del objeto de respuesta.</span><span class="sxs-lookup"><span data-stu-id="0b98d-112">The name of the response object.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0b98d-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0b98d-113">Child elements</span></span>

<span data-ttu-id="0b98d-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0b98d-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0b98d-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0b98d-115">Parent elements</span></span>

[<span data-ttu-id="0b98d-116">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="0b98d-116">ResponseObjects</span></span>](responseobjects.md)
  
## <a name="remarks"></a><span data-ttu-id="0b98d-117">Notas</span><span class="sxs-lookup"><span data-stu-id="0b98d-117">Remarks</span></span>

<span data-ttu-id="0b98d-118">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="0b98d-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="0b98d-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0b98d-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0b98d-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0b98d-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b98d-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0b98d-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0b98d-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0b98d-122">Schema Name</span></span>  <br/> |<span data-ttu-id="0b98d-123">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0b98d-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="0b98d-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0b98d-124">Validation File</span></span>  <br/> |<span data-ttu-id="0b98d-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0b98d-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0b98d-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0b98d-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="0b98d-127">Verdadero</span><span class="sxs-lookup"><span data-stu-id="0b98d-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0b98d-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="0b98d-128">See also</span></span>



[<span data-ttu-id="0b98d-129">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="0b98d-129">ResponseObjects</span></span>](responseobjects.md)


- [<span data-ttu-id="0b98d-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0b98d-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

