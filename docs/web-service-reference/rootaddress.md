---
title: RootAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RootAddress
api_type:
- schema
ms.assetid: 1dbb130a-e4eb-4baf-ae07-2568a8375bff
description: El elemento RootAddress representa la primera dirección que inicia el evento para un evento RecipientTrackingEvent.
ms.openlocfilehash: e020ff07f271bdde6c2a4172141097dcba66f64e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465096"
---
# <a name="rootaddress"></a><span data-ttu-id="1257e-103">RootAddress</span><span class="sxs-lookup"><span data-stu-id="1257e-103">RootAddress</span></span>

<span data-ttu-id="1257e-104">El elemento **RootAddress** representa la primera dirección que inicia el evento para un evento [RecipientTrackingEvent](recipienttrackingevent.md) .</span><span class="sxs-lookup"><span data-stu-id="1257e-104">The **RootAddress** element represents the first address that starts the event for a [RecipientTrackingEvent](recipienttrackingevent.md) event.</span></span> 
  
```xml
<RootAddress/>
```

 <span data-ttu-id="1257e-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="1257e-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1257e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1257e-106">Attributes and elements</span></span>

<span data-ttu-id="1257e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1257e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1257e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1257e-108">Attributes</span></span>

<span data-ttu-id="1257e-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1257e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1257e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1257e-110">Child elements</span></span>

<span data-ttu-id="1257e-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1257e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1257e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1257e-112">Parent elements</span></span>

|<span data-ttu-id="1257e-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1257e-113">**Element**</span></span>|<span data-ttu-id="1257e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1257e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1257e-115">RecipientTrackingEvent</span><span class="sxs-lookup"><span data-stu-id="1257e-115">RecipientTrackingEvent</span></span>](recipienttrackingevent.md) <br/> |<span data-ttu-id="1257e-116">Contiene información de un evento único para un destinatario.</span><span class="sxs-lookup"><span data-stu-id="1257e-116">Contains information for a single event for a recipient.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1257e-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1257e-117">Text value</span></span>

<span data-ttu-id="1257e-118">El valor de texto es la dirección que inicia el evento Tracking.</span><span class="sxs-lookup"><span data-stu-id="1257e-118">The text value is the address that starts the tracking event.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1257e-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1257e-119">Remarks</span></span>

<span data-ttu-id="1257e-120">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="1257e-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1257e-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1257e-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1257e-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="1257e-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1257e-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1257e-123">Schema Name</span></span>  <br/> |<span data-ttu-id="1257e-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1257e-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="1257e-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1257e-125">Validation File</span></span>  <br/> |<span data-ttu-id="1257e-126">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1257e-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1257e-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1257e-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="1257e-128">Falso</span><span class="sxs-lookup"><span data-stu-id="1257e-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1257e-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1257e-129">See also</span></span>



[<span data-ttu-id="1257e-130">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="1257e-130">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="1257e-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1257e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

