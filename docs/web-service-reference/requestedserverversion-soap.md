---
title: RequestedServerVersion (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: cf3f9d7a-2add-4457-b009-2929220f90b5
description: El elemento RequestedServerVersion especifica la versión del servidor destino de una llamada al método de detección automática.
ms.openlocfilehash: ff63c82943bdd3476a4284f5aa2075fc9c0194b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467910"
---
# <a name="requestedserverversion-soap"></a><span data-ttu-id="04852-103">RequestedServerVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="04852-103">RequestedServerVersion (SOAP)</span></span>

<span data-ttu-id="04852-104">El elemento **RequestedServerVersion** especifica la versión del servidor destino de una llamada al método de **detección automática** .</span><span class="sxs-lookup"><span data-stu-id="04852-104">The **RequestedServerVersion** element specifies the server version that an **Autodiscover** method call targets.</span></span> 
  
```XML
<RequestedServerVersion/>
```

 <span data-ttu-id="04852-105">**ExchangeVersion**</span><span class="sxs-lookup"><span data-stu-id="04852-105">**ExchangeVersion**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="04852-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="04852-106">Attributes and elements</span></span>

<span data-ttu-id="04852-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="04852-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04852-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="04852-108">Attributes</span></span>

<span data-ttu-id="04852-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="04852-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="04852-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="04852-110">Child elements</span></span>

<span data-ttu-id="04852-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="04852-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="04852-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="04852-112">Parent elements</span></span>

<span data-ttu-id="04852-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="04852-113">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="04852-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="04852-114">Text value</span></span>

<span data-ttu-id="04852-115">El valor de texto del elemento **RequestedServerVersion** especifica la versión del servidor a la que se dirige una llamada al método de **detección automática** .</span><span class="sxs-lookup"><span data-stu-id="04852-115">The text value of the **RequestedServerVersion** element specifies the server version that an **Autodiscover** method call targets.</span></span> <span data-ttu-id="04852-116">En la siguiente tabla se enumeran las versiones de servidor válidas.</span><span class="sxs-lookup"><span data-stu-id="04852-116">The following table lists the valid server versions.</span></span> 
  
|<span data-ttu-id="04852-117">**Valor de texto**</span><span class="sxs-lookup"><span data-stu-id="04852-117">**Text value**</span></span>|<span data-ttu-id="04852-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="04852-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="04852-119">Exchange2007_SP1</span><span class="sxs-lookup"><span data-stu-id="04852-119">Exchange2007_SP1</span></span>  <br/> |<span data-ttu-id="04852-120">Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="04852-120">Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|<span data-ttu-id="04852-121">Exchange2010</span><span class="sxs-lookup"><span data-stu-id="04852-121">Exchange2010</span></span>  <br/> |<span data-ttu-id="04852-122">Exchange Server 2010.</span><span class="sxs-lookup"><span data-stu-id="04852-122">Exchange Server 2010.</span></span>  <br/> |
|<span data-ttu-id="04852-123">Exchange2010_SP1</span><span class="sxs-lookup"><span data-stu-id="04852-123">Exchange2010_SP1</span></span>  <br/> |<span data-ttu-id="04852-124">Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="04852-124">Exchange Server 2010 Service Pack 1 (SP1).</span></span>  <br/> |
|<span data-ttu-id="04852-125">Exchange2010_SP2</span><span class="sxs-lookup"><span data-stu-id="04852-125">Exchange2010_SP2</span></span>  <br/> |<span data-ttu-id="04852-126">Exchange Server 2010 Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="04852-126">Exchange Server 2010 Service Pack 2 (SP2).</span></span>  <br/> |
|<span data-ttu-id="04852-127">Exchange2013</span><span class="sxs-lookup"><span data-stu-id="04852-127">Exchange2013</span></span>  <br/> |<span data-ttu-id="04852-128">Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04852-128">Exchange Server 2013.</span></span> <span data-ttu-id="04852-129">El campo Exchange2013 se aplica a los clientes de Exchange Online y versiones de Exchange que comienzan con Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04852-129">The Exchange2013 field is applicable for clients that target Exchange Online and versions of Exchange starting with Exchange Server 2013.</span></span>  <br/> |
|<span data-ttu-id="04852-130">Exchange2013_SP1</span><span class="sxs-lookup"><span data-stu-id="04852-130">Exchange2013_SP1</span></span>  <br/> |<span data-ttu-id="04852-131">Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="04852-131">Exchange Server 2013 Service Pack 1 (SP1).</span></span> <span data-ttu-id="04852-132">El campo Exchange2013_SP1 se aplica a los clientes de Exchange Online y versiones de Exchange que comienzan con Exchange Server 2013 SP1.</span><span class="sxs-lookup"><span data-stu-id="04852-132">The Exchange2013_SP1 field is applicable for clients that target Exchange Online and versions of Exchange starting with Exchange Server 2013 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="04852-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04852-133">Remarks</span></span>

<span data-ttu-id="04852-134">El elemento **RequestedServerVersion** se establece en el encabezado SOAP.</span><span class="sxs-lookup"><span data-stu-id="04852-134">The **RequestedServerVersion** element is set in the SOAP header.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="04852-135">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="04852-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04852-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="04852-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="04852-137">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="04852-137">Schema Name</span></span>  <br/> |<span data-ttu-id="04852-138">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="04852-138">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="04852-139">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="04852-139">Validation File</span></span>  <br/> |<span data-ttu-id="04852-140">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="04852-140">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="04852-141">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="04852-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="04852-142">Verdadero</span><span class="sxs-lookup"><span data-stu-id="04852-142">True</span></span>  <br/> |
   

