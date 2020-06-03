---
title: IsDelegated
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsDelegated
api_type:
- schema
ms.assetid: c12907db-be80-4924-9469-8e58612cf42c
description: El elemento IsDelegated indica si una reunión la controla una cuenta con acceso de delegado.
ms.openlocfilehash: 2c62b59665431d5ea203e972a506aa90afc76601
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456447"
---
# <a name="isdelegated"></a><span data-ttu-id="cc762-103">IsDelegated</span><span class="sxs-lookup"><span data-stu-id="cc762-103">IsDelegated</span></span>

<span data-ttu-id="cc762-104">El elemento **IsDelegated** indica si una reunión la controla una cuenta con acceso de delegado.</span><span class="sxs-lookup"><span data-stu-id="cc762-104">The **IsDelegated** element indicates whether a meeting was handled by an account that has delegate access.</span></span> 
  
```xml
<IsDelegated/>
```

 <span data-ttu-id="cc762-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="cc762-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cc762-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cc762-106">Attributes and elements</span></span>

<span data-ttu-id="cc762-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cc762-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cc762-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cc762-108">Attributes</span></span>

<span data-ttu-id="cc762-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cc762-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cc762-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cc762-110">Child elements</span></span>

<span data-ttu-id="cc762-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cc762-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cc762-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cc762-112">Parent elements</span></span>

|<span data-ttu-id="cc762-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cc762-113">**Element**</span></span>|<span data-ttu-id="cc762-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cc762-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cc762-115">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="cc762-115">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="cc762-116">Representa una cancelación de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cc762-116">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cc762-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="cc762-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="cc762-118">Representa una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cc762-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cc762-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="cc762-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="cc762-120">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cc762-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cc762-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="cc762-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="cc762-122">Representa una respuesta a una reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="cc762-122">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cc762-123">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cc762-123">Text value</span></span>

<span data-ttu-id="cc762-124">Un valor de texto de **true** indica que la reunión se controló mediante una cuenta que tiene acceso de delegado.</span><span class="sxs-lookup"><span data-stu-id="cc762-124">A text value of **true** indicates that the meeting was handled by an account that has delegate access.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cc762-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cc762-125">Remarks</span></span>

<span data-ttu-id="cc762-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="cc762-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cc762-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cc762-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc762-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="cc762-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cc762-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cc762-129">Schema Name</span></span>  <br/> |<span data-ttu-id="cc762-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="cc762-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="cc762-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cc762-131">Validation File</span></span>  <br/> |<span data-ttu-id="cc762-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="cc762-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cc762-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cc762-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="cc762-134">Falso</span><span class="sxs-lookup"><span data-stu-id="cc762-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cc762-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc762-135">See also</span></span>



- [<span data-ttu-id="cc762-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cc762-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

