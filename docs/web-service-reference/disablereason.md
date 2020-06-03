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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463674"
---
# <a name="disablereason"></a><span data-ttu-id="beb20-103">DisableReason</span><span class="sxs-lookup"><span data-stu-id="beb20-103">DisableReason</span></span>

<span data-ttu-id="beb20-104">El elemento **DisableReason** especifica el motivo por el que se deshabilita una aplicación.</span><span class="sxs-lookup"><span data-stu-id="beb20-104">The **DisableReason** element specifies the reason for disabling an app.</span></span> 
  
```XML
<DisableReason> NoReason | OutlookClientPerformance | OWAClientPerformance | MobileClientPerformance </DisableReason>
```

 <span data-ttu-id="beb20-105">**DisableReasonType**</span><span class="sxs-lookup"><span data-stu-id="beb20-105">**DisableReasonType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="beb20-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="beb20-106">Attributes and elements</span></span>

<span data-ttu-id="beb20-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="beb20-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="beb20-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="beb20-108">Attributes</span></span>

<span data-ttu-id="beb20-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="beb20-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="beb20-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="beb20-110">Child elements</span></span>

<span data-ttu-id="beb20-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="beb20-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="beb20-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="beb20-112">Parent elements</span></span>

|<span data-ttu-id="beb20-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="beb20-113">**Element**</span></span>|<span data-ttu-id="beb20-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="beb20-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="beb20-115">DisableApp</span><span class="sxs-lookup"><span data-stu-id="beb20-115">DisableApp</span></span>](disableapp.md) <br/> |<span data-ttu-id="beb20-116">Especifica una solicitud para deshabilitar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="beb20-116">Specifies a request to disable an app.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="beb20-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="beb20-117">Text value</span></span>

<span data-ttu-id="beb20-118">**Valor de texto del elemento DisableReason**</span><span class="sxs-lookup"><span data-stu-id="beb20-118">**DisableReason element text value**</span></span>

|<span data-ttu-id="beb20-119">**Valor**</span><span class="sxs-lookup"><span data-stu-id="beb20-119">**Value**</span></span>|<span data-ttu-id="beb20-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="beb20-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="beb20-121">Noreason</span><span class="sxs-lookup"><span data-stu-id="beb20-121">NoReason</span></span>  <br/> |<span data-ttu-id="beb20-122">Sin motivo dado</span><span class="sxs-lookup"><span data-stu-id="beb20-122">No reason given</span></span>  <br/> |
|<span data-ttu-id="beb20-123">OutlookClientPerformance</span><span class="sxs-lookup"><span data-stu-id="beb20-123">OutlookClientPerformance</span></span>  <br/> |<span data-ttu-id="beb20-124">Mejorar el rendimiento del cliente de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="beb20-124">To improve email client performance.</span></span>  <br/> |
|<span data-ttu-id="beb20-125">OWAClientPerformance</span><span class="sxs-lookup"><span data-stu-id="beb20-125">OWAClientPerformance</span></span>  <br/> |<span data-ttu-id="beb20-126">Para mejorar el rendimiento del cliente de la aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="beb20-126">To improve Web app client performance.</span></span>  <br/> |
|<span data-ttu-id="beb20-127">MobileClientPerformance</span><span class="sxs-lookup"><span data-stu-id="beb20-127">MobileClientPerformance</span></span>  <br/> |<span data-ttu-id="beb20-128">Mejorar el rendimiento del cliente móvil.</span><span class="sxs-lookup"><span data-stu-id="beb20-128">To improve mobile client performance.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="beb20-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="beb20-129">Remarks</span></span>

<span data-ttu-id="beb20-130">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="beb20-130">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="beb20-131">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="beb20-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="beb20-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="beb20-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="beb20-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="beb20-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="beb20-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="beb20-134">Schema Name</span></span>  <br/> |<span data-ttu-id="beb20-135">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="beb20-135">Type schema</span></span>  <br/> |
|<span data-ttu-id="beb20-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="beb20-136">Validation File</span></span>  <br/> |<span data-ttu-id="beb20-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="beb20-137">types.xsd</span></span>  <br/> |
|<span data-ttu-id="beb20-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="beb20-138">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="beb20-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="beb20-139">See also</span></span>

- [<span data-ttu-id="beb20-140">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="beb20-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

