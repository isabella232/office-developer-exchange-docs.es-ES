---
title: BccRecipient
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BccRecipient
api_type:
- schema
ms.assetid: 4ef0cff5-8a5a-4d76-9d2b-938774d8fc1b
description: El elemento BccRecipient representa un destinatario para recibir una copia oculta (CCO) del mensaje de correo electrónico.
ms.openlocfilehash: bed58536263196a61651493e92a4dcd1df3f5ec9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763608"
---
# <a name="bccrecipient"></a><span data-ttu-id="21d0b-103">BccRecipient</span><span class="sxs-lookup"><span data-stu-id="21d0b-103">BccRecipient</span></span>

<span data-ttu-id="21d0b-104">El elemento **BccRecipient** representa un destinatario para recibir una copia oculta (CCO) del mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="21d0b-104">The **BccRecipient** element represents a recipient to receive a blind carbon copy (Bcc) of an e-mail message.</span></span> 
  
```XML
<BccRecipient>true | false</BccRecipient>
```

 <span data-ttu-id="21d0b-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="21d0b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="21d0b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="21d0b-106">Attributes and elements</span></span>

<span data-ttu-id="21d0b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="21d0b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21d0b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="21d0b-108">Attributes</span></span>

<span data-ttu-id="21d0b-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="21d0b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="21d0b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="21d0b-110">Child elements</span></span>

<span data-ttu-id="21d0b-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="21d0b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="21d0b-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="21d0b-112">Parent elements</span></span>

|<span data-ttu-id="21d0b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="21d0b-113">**Element**</span></span>|<span data-ttu-id="21d0b-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="21d0b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21d0b-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="21d0b-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="21d0b-116">Contiene información de un solo evento de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="21d0b-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="21d0b-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="21d0b-117">Text value</span></span>

<span data-ttu-id="21d0b-118">Este elemento puede ser **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="21d0b-118">This element can be either **true** or **false**.</span></span> <span data-ttu-id="21d0b-119">Un valor de **true** indica que el destinatario es carbón oculta copiado; un valor de **false** indica que el destinatario no es carbón oculta copiado.</span><span class="sxs-lookup"><span data-stu-id="21d0b-119">A value of **true** indicates that the recipient is blind carbon copied; a value of **false** indicates that the recipient is not blind carbon copied.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="21d0b-120">Notas</span><span class="sxs-lookup"><span data-stu-id="21d0b-120">Remarks</span></span>

<span data-ttu-id="21d0b-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="21d0b-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21d0b-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="21d0b-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21d0b-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="21d0b-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="21d0b-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="21d0b-124">Schema Name</span></span>  <br/> |<span data-ttu-id="21d0b-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="21d0b-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="21d0b-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="21d0b-126">Validation File</span></span>  <br/> |<span data-ttu-id="21d0b-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="21d0b-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="21d0b-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="21d0b-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="21d0b-129">False</span><span class="sxs-lookup"><span data-stu-id="21d0b-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21d0b-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="21d0b-130">See also</span></span>



- [<span data-ttu-id="21d0b-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="21d0b-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

