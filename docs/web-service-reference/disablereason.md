---
title: DisableReason
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f41b5be6-9b79-4e83-8cdb-aa779e13cb3f
description: El elemento DisableReason especifica el motivo por el que se deshabilita una aplicación.
ms.openlocfilehash: 1406d69647bde5389dc9bb61adf7537a57d5adfc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463674"
---
# <a name="disablereason"></a><span data-ttu-id="e5c92-103">DisableReason</span><span class="sxs-lookup"><span data-stu-id="e5c92-103">DisableReason</span></span>

<span data-ttu-id="e5c92-104">El elemento **DisableReason** especifica el motivo por el que se deshabilita una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e5c92-104">The **DisableReason** element specifies the reason for disabling an app.</span></span> 
  
```XML
<DisableReason> NoReason | OutlookClientPerformance | OWAClientPerformance | MobileClientPerformance </DisableReason>
```

 <span data-ttu-id="e5c92-105">**DisableReasonType**</span><span class="sxs-lookup"><span data-stu-id="e5c92-105">**DisableReasonType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e5c92-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e5c92-106">Attributes and elements</span></span>

<span data-ttu-id="e5c92-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e5c92-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e5c92-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e5c92-108">Attributes</span></span>

<span data-ttu-id="e5c92-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e5c92-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e5c92-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e5c92-110">Child elements</span></span>

<span data-ttu-id="e5c92-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e5c92-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e5c92-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e5c92-112">Parent elements</span></span>

|<span data-ttu-id="e5c92-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e5c92-113">**Element**</span></span>|<span data-ttu-id="e5c92-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e5c92-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e5c92-115">DisableApp</span><span class="sxs-lookup"><span data-stu-id="e5c92-115">DisableApp</span></span>](disableapp.md) <br/> |<span data-ttu-id="e5c92-116">Especifica una solicitud para deshabilitar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e5c92-116">Specifies a request to disable an app.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e5c92-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e5c92-117">Text value</span></span>

<span data-ttu-id="e5c92-118">**Valor de texto del elemento DisableReason**</span><span class="sxs-lookup"><span data-stu-id="e5c92-118">**DisableReason element text value**</span></span>

|<span data-ttu-id="e5c92-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e5c92-119">**Value**</span></span>|<span data-ttu-id="e5c92-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e5c92-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e5c92-121">Noreason</span><span class="sxs-lookup"><span data-stu-id="e5c92-121">NoReason</span></span>  <br/> |<span data-ttu-id="e5c92-122">Sin motivo dado</span><span class="sxs-lookup"><span data-stu-id="e5c92-122">No reason given</span></span>  <br/> |
|<span data-ttu-id="e5c92-123">OutlookClientPerformance</span><span class="sxs-lookup"><span data-stu-id="e5c92-123">OutlookClientPerformance</span></span>  <br/> |<span data-ttu-id="e5c92-124">Mejorar el rendimiento del cliente de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e5c92-124">To improve email client performance.</span></span>  <br/> |
|<span data-ttu-id="e5c92-125">OWAClientPerformance</span><span class="sxs-lookup"><span data-stu-id="e5c92-125">OWAClientPerformance</span></span>  <br/> |<span data-ttu-id="e5c92-126">Para mejorar el rendimiento del cliente de la aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="e5c92-126">To improve Web app client performance.</span></span>  <br/> |
|<span data-ttu-id="e5c92-127">MobileClientPerformance</span><span class="sxs-lookup"><span data-stu-id="e5c92-127">MobileClientPerformance</span></span>  <br/> |<span data-ttu-id="e5c92-128">Mejorar el rendimiento del cliente móvil.</span><span class="sxs-lookup"><span data-stu-id="e5c92-128">To improve mobile client performance.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5c92-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e5c92-129">Remarks</span></span>

<span data-ttu-id="e5c92-130">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e5c92-130">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e5c92-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e5c92-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e5c92-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e5c92-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5c92-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5c92-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e5c92-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e5c92-134">Schema Name</span></span>  <br/> |<span data-ttu-id="e5c92-135">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="e5c92-135">Type schema</span></span>  <br/> |
|<span data-ttu-id="e5c92-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e5c92-136">Validation File</span></span>  <br/> |<span data-ttu-id="e5c92-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e5c92-137">types.xsd</span></span>  <br/> |
|<span data-ttu-id="e5c92-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e5c92-138">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e5c92-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5c92-139">See also</span></span>

- [<span data-ttu-id="e5c92-140">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e5c92-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

