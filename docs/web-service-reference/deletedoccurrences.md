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
description: El elemento DeletedOccurrences contiene una matriz de ocurrencias eliminadas de un elemento de calendario periódico.
ms.openlocfilehash: be39ff95b5529481a36b7549e638818a20e01283
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463709"
---
# <a name="deletedoccurrences"></a><span data-ttu-id="55c33-103">DeletedOccurrences</span><span class="sxs-lookup"><span data-stu-id="55c33-103">DeletedOccurrences</span></span>

<span data-ttu-id="55c33-104">El elemento **DeletedOccurrences** contiene una matriz de ocurrencias eliminadas de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="55c33-104">The **DeletedOccurrences** element contains an array of deleted occurrences of a recurring calendar item.</span></span> 
  
```xml
<DeletedOccurrences>
   <DeletedOccurrence/>
</DeletedOccurrences>
```

 <span data-ttu-id="55c33-105">**NonEmptyArrayOfDeletedOccurrencesType**</span><span class="sxs-lookup"><span data-stu-id="55c33-105">**NonEmptyArrayOfDeletedOccurrencesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="55c33-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="55c33-106">Attributes and elements</span></span>

<span data-ttu-id="55c33-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="55c33-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="55c33-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="55c33-108">Attributes</span></span>

<span data-ttu-id="55c33-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="55c33-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="55c33-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="55c33-110">Child elements</span></span>

|<span data-ttu-id="55c33-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="55c33-111">**Element**</span></span>|<span data-ttu-id="55c33-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="55c33-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55c33-113">DeletedOccurrence</span><span class="sxs-lookup"><span data-stu-id="55c33-113">DeletedOccurrence</span></span>](deletedoccurrence.md) <br/> |<span data-ttu-id="55c33-114">Representa una ocurrencia eliminada de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="55c33-114">Represents a deleted occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="55c33-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="55c33-115">Parent elements</span></span>

|<span data-ttu-id="55c33-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="55c33-116">**Element**</span></span>|<span data-ttu-id="55c33-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="55c33-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55c33-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="55c33-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="55c33-119">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="55c33-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="55c33-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="55c33-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="55c33-121">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="55c33-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55c33-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="55c33-122">Remarks</span></span>

<span data-ttu-id="55c33-123">Este elemento es válido si se usa el valor de texto RecurringMaster para el elemento [CalendarItemType](calendaritemtype.md) .</span><span class="sxs-lookup"><span data-stu-id="55c33-123">This element is valid if the RecurringMaster text value is used for the [CalendarItemType](calendaritemtype.md) element.</span></span> 
  
<span data-ttu-id="55c33-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="55c33-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="55c33-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="55c33-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55c33-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="55c33-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="55c33-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="55c33-127">Schema name</span></span>  <br/> |<span data-ttu-id="55c33-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="55c33-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="55c33-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="55c33-129">Validation file</span></span>  <br/> |<span data-ttu-id="55c33-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="55c33-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="55c33-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="55c33-131">Can be empty</span></span>  <br/> |<span data-ttu-id="55c33-132">Falso</span><span class="sxs-lookup"><span data-stu-id="55c33-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55c33-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="55c33-133">See also</span></span>

- [<span data-ttu-id="55c33-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="55c33-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)  
- [<span data-ttu-id="55c33-135">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="55c33-135">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

