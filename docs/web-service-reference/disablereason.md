---
title: DisableReason
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f41b5be6-9b79-4e83-8cdb-aa779e13cb3f
description: El elemento DisableReason especifica la razón para deshabilitar una aplicación.
ms.openlocfilehash: f900bd1b98b294900f767c778b9c5f87f74042ca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764185"
---
# <a name="disablereason"></a><span data-ttu-id="70df1-103">DisableReason</span><span class="sxs-lookup"><span data-stu-id="70df1-103">DisableReason</span></span>

<span data-ttu-id="70df1-104">El elemento **DisableReason** especifica la razón para deshabilitar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="70df1-104">The **DisableReason** element specifies the reason for disabling an app.</span></span> 
  
```XML
<DisableReason> NoReason | OutlookClientPerformance | OWAClientPerformance | MobileClientPerformance </DisableReason>
```

 <span data-ttu-id="70df1-105">**DisableReasonType**</span><span class="sxs-lookup"><span data-stu-id="70df1-105">**DisableReasonType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="70df1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="70df1-106">Attributes and elements</span></span>

<span data-ttu-id="70df1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="70df1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70df1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="70df1-108">Attributes</span></span>

<span data-ttu-id="70df1-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="70df1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="70df1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="70df1-110">Child elements</span></span>

<span data-ttu-id="70df1-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="70df1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="70df1-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="70df1-112">Parent elements</span></span>

|<span data-ttu-id="70df1-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="70df1-113">**Element**</span></span>|<span data-ttu-id="70df1-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="70df1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="70df1-115">DisableApp</span><span class="sxs-lookup"><span data-stu-id="70df1-115">DisableApp</span></span>](disableapp.md) <br/> |<span data-ttu-id="70df1-116">Especifica una solicitud para deshabilitar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="70df1-116">Specifies a request to disable an app.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="70df1-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="70df1-117">Text value</span></span>

<span data-ttu-id="70df1-118">**Valor de texto del elemento DisableReason**</span><span class="sxs-lookup"><span data-stu-id="70df1-118">**DisableReason element text value**</span></span>

|<span data-ttu-id="70df1-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="70df1-119">**Value**</span></span>|<span data-ttu-id="70df1-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="70df1-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="70df1-121">NoReason</span><span class="sxs-lookup"><span data-stu-id="70df1-121">NoReason</span></span>  <br/> |<span data-ttu-id="70df1-122">No hay motivo</span><span class="sxs-lookup"><span data-stu-id="70df1-122">No reason given</span></span>  <br/> |
|<span data-ttu-id="70df1-123">OutlookClientPerformance</span><span class="sxs-lookup"><span data-stu-id="70df1-123">OutlookClientPerformance</span></span>  <br/> |<span data-ttu-id="70df1-124">Para mejorar el rendimiento del cliente de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="70df1-124">To improve email client performance.</span></span>  <br/> |
|<span data-ttu-id="70df1-125">OWAClientPerformance</span><span class="sxs-lookup"><span data-stu-id="70df1-125">OWAClientPerformance</span></span>  <br/> |<span data-ttu-id="70df1-126">Para mejorar el rendimiento de las aplicaciones cliente Web.</span><span class="sxs-lookup"><span data-stu-id="70df1-126">To improve Web app client performance.</span></span>  <br/> |
|<span data-ttu-id="70df1-127">MobileClientPerformance</span><span class="sxs-lookup"><span data-stu-id="70df1-127">MobileClientPerformance</span></span>  <br/> |<span data-ttu-id="70df1-128">Para mejorar el rendimiento de cliente móvil.</span><span class="sxs-lookup"><span data-stu-id="70df1-128">To improve mobile client performance.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70df1-129">Notas</span><span class="sxs-lookup"><span data-stu-id="70df1-129">Remarks</span></span>

<span data-ttu-id="70df1-130">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="70df1-130">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="70df1-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="70df1-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="70df1-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="70df1-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70df1-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="70df1-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="70df1-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="70df1-134">Schema Name</span></span>  <br/> |<span data-ttu-id="70df1-135">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="70df1-135">Type schema</span></span>  <br/> |
|<span data-ttu-id="70df1-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="70df1-136">Validation File</span></span>  <br/> |<span data-ttu-id="70df1-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="70df1-137">types.xsd</span></span>  <br/> |
|<span data-ttu-id="70df1-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="70df1-138">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="70df1-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="70df1-139">See also</span></span>

- [<span data-ttu-id="70df1-140">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="70df1-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

