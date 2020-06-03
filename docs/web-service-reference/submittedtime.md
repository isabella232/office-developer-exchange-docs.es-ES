---
title: SubmittedTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubmittedTime
api_type:
- schema
ms.assetid: 45c8fa36-c539-42ca-99dc-1ac33cc54afc
description: El elemento SubmittedTime representa la hora en que el mensaje entró en el servidor.
ms.openlocfilehash: bf9495aa700d2887d199eccb38289e0ebd2e8636
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465411"
---
# <a name="submittedtime"></a><span data-ttu-id="cc8df-103">SubmittedTime</span><span class="sxs-lookup"><span data-stu-id="cc8df-103">SubmittedTime</span></span>

<span data-ttu-id="cc8df-104">El elemento **SubmittedTime** representa la hora en que el mensaje entró en el servidor.</span><span class="sxs-lookup"><span data-stu-id="cc8df-104">The **SubmittedTime** element represents the time that the message entered the server.</span></span> 
  
```XML
<SubmittedTime/>
```

 <span data-ttu-id="cc8df-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="cc8df-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cc8df-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cc8df-106">Attributes and elements</span></span>

<span data-ttu-id="cc8df-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cc8df-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cc8df-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cc8df-108">Attributes</span></span>

<span data-ttu-id="cc8df-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cc8df-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cc8df-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cc8df-110">Child elements</span></span>

<span data-ttu-id="cc8df-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cc8df-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cc8df-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cc8df-112">Parent elements</span></span>

|<span data-ttu-id="cc8df-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cc8df-113">**Element**</span></span>|<span data-ttu-id="cc8df-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cc8df-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cc8df-115">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="cc8df-115">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="cc8df-116">Contiene un único resultado de mensaje para un elemento [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="cc8df-116">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cc8df-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cc8df-117">Text value</span></span>

 <span data-ttu-id="cc8df-118">Si se usa este elemento, es necesario un valor de texto que represente una fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="cc8df-118">A text value that represents a date/time is required if this element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cc8df-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cc8df-119">Remarks</span></span>

<span data-ttu-id="cc8df-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="cc8df-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cc8df-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cc8df-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc8df-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="cc8df-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cc8df-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cc8df-123">Schema Name</span></span>  <br/> |<span data-ttu-id="cc8df-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="cc8df-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="cc8df-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cc8df-125">Validation File</span></span>  <br/> |<span data-ttu-id="cc8df-126">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="cc8df-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cc8df-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cc8df-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="cc8df-128">Falso</span><span class="sxs-lookup"><span data-stu-id="cc8df-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cc8df-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc8df-129">See also</span></span>



- [<span data-ttu-id="cc8df-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cc8df-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

