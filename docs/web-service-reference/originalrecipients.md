---
title: OriginalRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OriginalRecipients
api_type:
- schema
ms.assetid: e4af86a5-85af-4239-8055-e29f0acf77c1
description: El elemento OriginalRecipients representa una lista de direcciones de correo electrónico de los destinatarios del primer mensaje.
ms.openlocfilehash: 8f99368409dbfb5ac798b691be65c7fd64f32660
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836665"
---
# <a name="originalrecipients"></a><span data-ttu-id="d2506-103">OriginalRecipients</span><span class="sxs-lookup"><span data-stu-id="d2506-103">OriginalRecipients</span></span>

<span data-ttu-id="d2506-104">El elemento **OriginalRecipients** representa una lista de direcciones de correo electrónico de los destinatarios del primer mensaje.</span><span class="sxs-lookup"><span data-stu-id="d2506-104">The **OriginalRecipients** element represents a list of e-mail addresses of the first message recipients.</span></span> 
  
```XML
<OriginalRecipients>
   <Address/>
</OriginalRecipients>
```

 <span data-ttu-id="d2506-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="d2506-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d2506-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d2506-106">Attributes and elements</span></span>

<span data-ttu-id="d2506-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d2506-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d2506-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d2506-108">Attributes</span></span>

<span data-ttu-id="d2506-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d2506-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d2506-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d2506-110">Child elements</span></span>

|<span data-ttu-id="d2506-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d2506-111">**Element**</span></span>|<span data-ttu-id="d2506-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d2506-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2506-113">Dirección (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="d2506-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="d2506-114">Contiene una dirección de correo electrónico completa resuelta.</span><span class="sxs-lookup"><span data-stu-id="d2506-114">Contains a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d2506-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d2506-115">Parent elements</span></span>

|<span data-ttu-id="d2506-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d2506-116">**Element**</span></span>|<span data-ttu-id="d2506-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d2506-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2506-118">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="d2506-118">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="d2506-119">Contiene un solo mensaje que se devuelve en una [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="d2506-119">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2506-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d2506-120">Remarks</span></span>

<span data-ttu-id="d2506-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d2506-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d2506-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d2506-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2506-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d2506-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d2506-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d2506-124">Schema Name</span></span>  <br/> |<span data-ttu-id="d2506-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d2506-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="d2506-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d2506-126">Validation File</span></span>  <br/> |<span data-ttu-id="d2506-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d2506-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d2506-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d2506-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="d2506-129">False</span><span class="sxs-lookup"><span data-stu-id="d2506-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d2506-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2506-130">See also</span></span>



[<span data-ttu-id="d2506-131">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="d2506-131">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="d2506-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d2506-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

