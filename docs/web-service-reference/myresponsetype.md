---
title: MyResponseType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MyResponseType
api_type:
- schema
ms.assetid: 9741b71d-a310-4520-81d5-3787a1ee630f
description: El elemento MyResponseType contiene el estado o la respuesta a un elemento de calendario.
ms.openlocfilehash: 640b0595ac039cc3c119aa52aa6e791e5b695e87
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466629"
---
# <a name="myresponsetype"></a><span data-ttu-id="8e1bd-103">MyResponseType</span><span class="sxs-lookup"><span data-stu-id="8e1bd-103">MyResponseType</span></span>

<span data-ttu-id="8e1bd-104">El elemento **MyResponseType** contiene el estado o la respuesta a un elemento de calendario.</span><span class="sxs-lookup"><span data-stu-id="8e1bd-104">The **MyResponseType** element contains the status of or response to a calendar item.</span></span> 
  
```xml
<MyResponseType/>
```

 <span data-ttu-id="8e1bd-105">**ResponseTypeType**</span><span class="sxs-lookup"><span data-stu-id="8e1bd-105">**ResponseTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8e1bd-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8e1bd-106">Attributes and elements</span></span>

<span data-ttu-id="8e1bd-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8e1bd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8e1bd-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8e1bd-108">Attributes</span></span>

<span data-ttu-id="8e1bd-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8e1bd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8e1bd-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8e1bd-110">Child elements</span></span>

<span data-ttu-id="8e1bd-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8e1bd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8e1bd-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8e1bd-112">Parent elements</span></span>

|<span data-ttu-id="8e1bd-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8e1bd-113">**Element**</span></span>|<span data-ttu-id="8e1bd-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8e1bd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e1bd-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="8e1bd-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="8e1bd-116">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8e1bd-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="8e1bd-117">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="8e1bd-117">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="8e1bd-118">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8e1bd-118">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8e1bd-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8e1bd-119">Text value</span></span>

<span data-ttu-id="8e1bd-120">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="8e1bd-120">A text value is required.</span></span> <span data-ttu-id="8e1bd-121">A continuación se muestran los valores de texto posibles para este elemento:</span><span class="sxs-lookup"><span data-stu-id="8e1bd-121">The following are the possible text values for this element:</span></span>
  
- <span data-ttu-id="8e1bd-122">Desconocido</span><span class="sxs-lookup"><span data-stu-id="8e1bd-122">Unknown</span></span>
    
- <span data-ttu-id="8e1bd-123">Organizador</span><span class="sxs-lookup"><span data-stu-id="8e1bd-123">Organizer</span></span>
    
- <span data-ttu-id="8e1bd-124">Provisional</span><span class="sxs-lookup"><span data-stu-id="8e1bd-124">Tentative</span></span>
    
- <span data-ttu-id="8e1bd-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8e1bd-125">Accept</span></span>
    
- <span data-ttu-id="8e1bd-126">Opongan</span><span class="sxs-lookup"><span data-stu-id="8e1bd-126">Decline</span></span>
    
- <span data-ttu-id="8e1bd-127">NoResponseReceived</span><span class="sxs-lookup"><span data-stu-id="8e1bd-127">NoResponseReceived</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e1bd-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8e1bd-128">Remarks</span></span>

<span data-ttu-id="8e1bd-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="8e1bd-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8e1bd-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8e1bd-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e1bd-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="8e1bd-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8e1bd-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8e1bd-132">Schema name</span></span>  <br/> |<span data-ttu-id="8e1bd-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8e1bd-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="8e1bd-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8e1bd-134">Validation file</span></span>  <br/> |<span data-ttu-id="8e1bd-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="8e1bd-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8e1bd-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8e1bd-136">Can be empty</span></span>  <br/> |<span data-ttu-id="8e1bd-137">Falso</span><span class="sxs-lookup"><span data-stu-id="8e1bd-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e1bd-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e1bd-138">See also</span></span>



- [<span data-ttu-id="8e1bd-139">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="8e1bd-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

