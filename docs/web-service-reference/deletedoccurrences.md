---
title: DeletedOccurrences
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeletedOccurrences
api_type:
- schema
ms.assetid: 736fb305-9528-4be8-ad37-65d7556edbf2
description: El elemento DeletedOccurrences contiene una matriz de eliminado apariciones de un elemento periódico del calendario.
ms.openlocfilehash: 269c1176913cd642f93987462286dd1fee3a7339
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764088"
---
# <a name="deletedoccurrences"></a><span data-ttu-id="2512c-103">DeletedOccurrences</span><span class="sxs-lookup"><span data-stu-id="2512c-103">DeletedOccurrences</span></span>

<span data-ttu-id="2512c-104">El elemento **DeletedOccurrences** contiene una matriz de eliminado apariciones de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="2512c-104">The **DeletedOccurrences** element contains an array of deleted occurrences of a recurring calendar item.</span></span> 
  
```xml
<DeletedOccurrences>
   <DeletedOccurrence/>
</DeletedOccurrences>
```

 <span data-ttu-id="2512c-105">**NonEmptyArrayOfDeletedOccurrencesType**</span><span class="sxs-lookup"><span data-stu-id="2512c-105">**NonEmptyArrayOfDeletedOccurrencesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2512c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2512c-106">Attributes and elements</span></span>

<span data-ttu-id="2512c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2512c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2512c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2512c-108">Attributes</span></span>

<span data-ttu-id="2512c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2512c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2512c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2512c-110">Child elements</span></span>

|<span data-ttu-id="2512c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2512c-111">**Element**</span></span>|<span data-ttu-id="2512c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2512c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2512c-113">DeletedOccurrence</span><span class="sxs-lookup"><span data-stu-id="2512c-113">DeletedOccurrence</span></span>](deletedoccurrence.md) <br/> |<span data-ttu-id="2512c-114">Representa una repetición eliminada de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="2512c-114">Represents a deleted occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2512c-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2512c-115">Parent elements</span></span>

|<span data-ttu-id="2512c-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="2512c-116">**Element**</span></span>|<span data-ttu-id="2512c-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2512c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2512c-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="2512c-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="2512c-119">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2512c-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="2512c-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="2512c-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="2512c-121">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2512c-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2512c-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2512c-122">Remarks</span></span>

<span data-ttu-id="2512c-123">Este elemento es válida si el valor de texto RecurringMaster se usa para el elemento [CalendarItemType](calendaritemtype.md) .</span><span class="sxs-lookup"><span data-stu-id="2512c-123">This element is valid if the RecurringMaster text value is used for the [CalendarItemType](calendaritemtype.md) element.</span></span> 
  
<span data-ttu-id="2512c-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="2512c-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2512c-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2512c-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2512c-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2512c-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2512c-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2512c-127">Schema name</span></span>  <br/> |<span data-ttu-id="2512c-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2512c-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="2512c-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2512c-129">Validation file</span></span>  <br/> |<span data-ttu-id="2512c-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2512c-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2512c-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2512c-131">Can be empty</span></span>  <br/> |<span data-ttu-id="2512c-132">False</span><span class="sxs-lookup"><span data-stu-id="2512c-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2512c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2512c-133">See also</span></span>

- [<span data-ttu-id="2512c-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2512c-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)  
- [<span data-ttu-id="2512c-135">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="2512c-135">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

