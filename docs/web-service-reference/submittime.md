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
description: El elemento SubmitTime representa la hora en que se envió el mensaje al servidor.
ms.openlocfilehash: e4409d962988ee308e0c0b461f9448ef68067fe8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467056"
---
# <a name="submittime"></a><span data-ttu-id="af0ab-103">SubmitTime</span><span class="sxs-lookup"><span data-stu-id="af0ab-103">SubmitTime</span></span>

<span data-ttu-id="af0ab-104">El elemento **SubmitTime** representa la hora en que se envió el mensaje al servidor.</span><span class="sxs-lookup"><span data-stu-id="af0ab-104">The **SubmitTime** element represents the time at which the message was sent to the server.</span></span> 
  
```XML
<SubmitTime/>
```

 <span data-ttu-id="af0ab-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="af0ab-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="af0ab-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="af0ab-106">Attributes and elements</span></span>

<span data-ttu-id="af0ab-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="af0ab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af0ab-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="af0ab-108">Attributes</span></span>

<span data-ttu-id="af0ab-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="af0ab-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="af0ab-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="af0ab-110">Child elements</span></span>

<span data-ttu-id="af0ab-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="af0ab-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="af0ab-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="af0ab-112">Parent elements</span></span>

|<span data-ttu-id="af0ab-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="af0ab-113">**Element**</span></span>|<span data-ttu-id="af0ab-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="af0ab-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af0ab-115">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="af0ab-115">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="af0ab-116">Contiene un solo mensaje que se devuelve en una [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="af0ab-116">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="af0ab-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="af0ab-117">Text value</span></span>

<span data-ttu-id="af0ab-118">Si se usa este elemento, es necesario un valor de texto que represente una fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="af0ab-118">A text value that represents a date/time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="af0ab-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="af0ab-119">Remarks</span></span>

<span data-ttu-id="af0ab-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="af0ab-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="af0ab-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="af0ab-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af0ab-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="af0ab-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="af0ab-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="af0ab-123">Schema Name</span></span>  <br/> |<span data-ttu-id="af0ab-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="af0ab-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="af0ab-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="af0ab-125">Validation File</span></span>  <br/> |<span data-ttu-id="af0ab-126">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="af0ab-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="af0ab-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="af0ab-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="af0ab-128">Falso</span><span class="sxs-lookup"><span data-stu-id="af0ab-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af0ab-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="af0ab-129">See also</span></span>



[<span data-ttu-id="af0ab-130">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="af0ab-130">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="af0ab-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="af0ab-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

