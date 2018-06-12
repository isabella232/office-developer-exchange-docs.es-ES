---
title: SubmitTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubmitTime
api_type:
- schema
ms.assetid: 97e4b71e-f45c-4bdb-80f9-805934916c0f
description: El elemento SubmitTime representa la hora a la que se envió el mensaje en el servidor.
ms.openlocfilehash: 3f19e2ac14b412ef8d1ab59eb069f0223cf782ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837617"
---
# <a name="submittime"></a><span data-ttu-id="165f6-103">SubmitTime</span><span class="sxs-lookup"><span data-stu-id="165f6-103">SubmitTime</span></span>

<span data-ttu-id="165f6-104">El elemento **SubmitTime** representa la hora a la que se envió el mensaje en el servidor.</span><span class="sxs-lookup"><span data-stu-id="165f6-104">The **SubmitTime** element represents the time at which the message was sent to the server.</span></span> 
  
```XML
<SubmitTime/>
```

 <span data-ttu-id="165f6-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="165f6-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="165f6-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="165f6-106">Attributes and elements</span></span>

<span data-ttu-id="165f6-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="165f6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="165f6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="165f6-108">Attributes</span></span>

<span data-ttu-id="165f6-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="165f6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="165f6-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="165f6-110">Child elements</span></span>

<span data-ttu-id="165f6-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="165f6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="165f6-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="165f6-112">Parent elements</span></span>

|<span data-ttu-id="165f6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="165f6-113">**Element**</span></span>|<span data-ttu-id="165f6-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="165f6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="165f6-115">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="165f6-115">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="165f6-116">Contiene un solo mensaje que se devuelve en una [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="165f6-116">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="165f6-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="165f6-117">Text value</span></span>

<span data-ttu-id="165f6-118">Si se usa este elemento, es necesario un valor de texto que representa un fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="165f6-118">A text value that represents a date/time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="165f6-119">Notas</span><span class="sxs-lookup"><span data-stu-id="165f6-119">Remarks</span></span>

<span data-ttu-id="165f6-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="165f6-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="165f6-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="165f6-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="165f6-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="165f6-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="165f6-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="165f6-123">Schema Name</span></span>  <br/> |<span data-ttu-id="165f6-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="165f6-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="165f6-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="165f6-125">Validation File</span></span>  <br/> |<span data-ttu-id="165f6-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="165f6-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="165f6-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="165f6-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="165f6-128">False</span><span class="sxs-lookup"><span data-stu-id="165f6-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="165f6-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="165f6-129">See also</span></span>



[<span data-ttu-id="165f6-130">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="165f6-130">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="165f6-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="165f6-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

