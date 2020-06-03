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
description: El elemento Scope especifica el ámbito del informe de seguimiento de mensajes.
ms.openlocfilehash: f86f6198e84e094e61ee569f6d005549316bbb9b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466944"
---
# <a name="scope-nonemptystringtype"></a><span data-ttu-id="fd76f-103">Ámbito (NonEmptyStringType)</span><span class="sxs-lookup"><span data-stu-id="fd76f-103">Scope (NonEmptyStringType)</span></span>

<span data-ttu-id="fd76f-104">El elemento **Scope** especifica el ámbito del informe de seguimiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="fd76f-104">The **Scope** element specifies the scope of the message tracking report.</span></span> 
  
```XML
<Scope>Organization | Forest | Site</Scope>
```

 <span data-ttu-id="fd76f-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="fd76f-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fd76f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fd76f-106">Attributes and elements</span></span>

<span data-ttu-id="fd76f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fd76f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fd76f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fd76f-108">Attributes</span></span>

<span data-ttu-id="fd76f-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fd76f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fd76f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fd76f-110">Child elements</span></span>

<span data-ttu-id="fd76f-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fd76f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fd76f-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fd76f-112">Parent elements</span></span>

<span data-ttu-id="fd76f-113">[FindMessageTrackingReport](findmessagetrackingreport.md)  |  [GetMessageTrackingReport](getmessagetrackingreport.md)</span><span class="sxs-lookup"><span data-stu-id="fd76f-113">[FindMessageTrackingReport](findmessagetrackingreport.md) | [GetMessageTrackingReport](getmessagetrackingreport.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="fd76f-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fd76f-114">Text value</span></span>

<span data-ttu-id="fd76f-115">En la siguiente tabla se enumeran los valores posibles para el elemento **Scope** .</span><span class="sxs-lookup"><span data-stu-id="fd76f-115">The following table lists the possible values for the **Scope** element.</span></span> 
  
|<span data-ttu-id="fd76f-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fd76f-116">**Value**</span></span>|<span data-ttu-id="fd76f-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fd76f-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fd76f-118">Organización</span><span class="sxs-lookup"><span data-stu-id="fd76f-118">Organization</span></span>  <br/> |<span data-ttu-id="fd76f-119">Los ámbitos de seguimiento de mensajes abarcan en toda la organización.</span><span class="sxs-lookup"><span data-stu-id="fd76f-119">The message tracking scopes spans across an organization.</span></span>  <br/> |
|<span data-ttu-id="fd76f-120">Bosque</span><span class="sxs-lookup"><span data-stu-id="fd76f-120">Forest</span></span>  <br/> |<span data-ttu-id="fd76f-121">Los ámbitos de seguimiento de mensajes se extienden por un bosque.</span><span class="sxs-lookup"><span data-stu-id="fd76f-121">The message tracking scopes spans across a forest.</span></span>  <br/> |
|<span data-ttu-id="fd76f-122">Site </span><span class="sxs-lookup"><span data-stu-id="fd76f-122">Site</span></span>  <br/> |<span data-ttu-id="fd76f-123">Los ámbitos de seguimiento de mensajes se extienden en un sitio.</span><span class="sxs-lookup"><span data-stu-id="fd76f-123">The message tracking scopes spans across a site.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd76f-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fd76f-124">Remarks</span></span>

<span data-ttu-id="fd76f-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fd76f-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fd76f-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fd76f-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd76f-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="fd76f-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fd76f-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fd76f-128">Schema Name</span></span>  <br/> |<span data-ttu-id="fd76f-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="fd76f-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fd76f-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fd76f-130">Validation File</span></span>  <br/> |<span data-ttu-id="fd76f-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="fd76f-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fd76f-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fd76f-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="fd76f-133">Falso</span><span class="sxs-lookup"><span data-stu-id="fd76f-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd76f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd76f-134">See also</span></span>



- [<span data-ttu-id="fd76f-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fd76f-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

