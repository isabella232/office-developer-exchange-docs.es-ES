---
title: Ámbito (NonEmptyStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Scope
api_type:
- schema
ms.assetid: 7efb6fd9-1615-469e-96f6-0f7846ad9b44
description: El elemento de ámbito especifica el ámbito del informe de seguimiento de mensajes.
ms.openlocfilehash: 534ed23916a60b246c7cb5be4a59d086980a7c37
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837280"
---
# <a name="scope-nonemptystringtype"></a><span data-ttu-id="cb17a-103">Ámbito (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="cb17a-103">Scope (NonEmptyStringType)</span></span>

<span data-ttu-id="cb17a-104">El elemento de **ámbito** especifica el ámbito del informe de seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="cb17a-104">The **Scope** element specifies the scope of the message tracking report.</span></span> 
  
```XML
<Scope>Organization | Forest | Site</Scope>
```

 <span data-ttu-id="cb17a-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="cb17a-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cb17a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cb17a-106">Attributes and elements</span></span>

<span data-ttu-id="cb17a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cb17a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb17a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cb17a-108">Attributes</span></span>

<span data-ttu-id="cb17a-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cb17a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cb17a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cb17a-110">Child elements</span></span>

<span data-ttu-id="cb17a-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cb17a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cb17a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cb17a-112">Parent elements</span></span>

<span data-ttu-id="cb17a-113">[FindMessageTrackingReport](findmessagetrackingreport.md) | [GetMessageTrackingReport](getmessagetrackingreport.md)</span><span class="sxs-lookup"><span data-stu-id="cb17a-113">[FindMessageTrackingReport](findmessagetrackingreport.md) | [GetMessageTrackingReport](getmessagetrackingreport.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="cb17a-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cb17a-114">Text value</span></span>

<span data-ttu-id="cb17a-115">En la siguiente tabla se enumera los valores posibles para el elemento de **ámbito** .</span><span class="sxs-lookup"><span data-stu-id="cb17a-115">The following table lists the possible values for the **Scope** element.</span></span> 
  
|<span data-ttu-id="cb17a-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cb17a-116">**Value**</span></span>|<span data-ttu-id="cb17a-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cb17a-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cb17a-118">Organización</span><span class="sxs-lookup"><span data-stu-id="cb17a-118">Organization</span></span>  <br/> |<span data-ttu-id="cb17a-119">Los ámbitos de seguimiento de mensajes se extiende en una organización.</span><span class="sxs-lookup"><span data-stu-id="cb17a-119">The message tracking scopes spans across an organization.</span></span>  <br/> |
|<span data-ttu-id="cb17a-120">Bosque</span><span class="sxs-lookup"><span data-stu-id="cb17a-120">Forest</span></span>  <br/> |<span data-ttu-id="cb17a-121">Los ámbitos de seguimiento de mensajes se extiende en un bosque.</span><span class="sxs-lookup"><span data-stu-id="cb17a-121">The message tracking scopes spans across a forest.</span></span>  <br/> |
|<span data-ttu-id="cb17a-122">Sitio</span><span class="sxs-lookup"><span data-stu-id="cb17a-122">Site</span></span>  <br/> |<span data-ttu-id="cb17a-123">Los ámbitos de seguimiento de mensajes se extiende en un sitio.</span><span class="sxs-lookup"><span data-stu-id="cb17a-123">The message tracking scopes spans across a site.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb17a-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb17a-124">Remarks</span></span>

<span data-ttu-id="cb17a-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="cb17a-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb17a-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cb17a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb17a-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cb17a-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cb17a-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cb17a-128">Schema Name</span></span>  <br/> |<span data-ttu-id="cb17a-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="cb17a-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cb17a-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cb17a-130">Validation File</span></span>  <br/> |<span data-ttu-id="cb17a-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cb17a-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cb17a-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cb17a-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="cb17a-133">False</span><span class="sxs-lookup"><span data-stu-id="cb17a-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb17a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb17a-134">See also</span></span>



- [<span data-ttu-id="cb17a-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="cb17a-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

