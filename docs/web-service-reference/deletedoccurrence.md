---
title: DeletedOccurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeletedOccurrence
api_type:
- schema
ms.assetid: ff24ea15-0cd7-407d-a378-73ec16451870
description: El elemento DeletedOccurrence representa una repetición eliminada de un elemento periódico del calendario.
ms.openlocfilehash: f12a2ba20f87f7803e492d8422b68c8ecdf9d797
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764084"
---
# <a name="deletedoccurrence"></a><span data-ttu-id="d4d05-103">DeletedOccurrence</span><span class="sxs-lookup"><span data-stu-id="d4d05-103">DeletedOccurrence</span></span>

<span data-ttu-id="d4d05-104">El elemento **DeletedOccurrence** representa una repetición eliminada de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="d4d05-104">The **DeletedOccurrence** element represents a deleted occurrence of a recurring calendar item.</span></span> 
  
```xml
<DeletedOccurrence>
   <Start/>
</DeletedOccurrence>
```

 <span data-ttu-id="d4d05-105">**DeletedOccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="d4d05-105">**DeletedOccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d4d05-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d4d05-106">Attributes and elements</span></span>

<span data-ttu-id="d4d05-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d4d05-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d4d05-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d4d05-108">Attributes</span></span>

<span data-ttu-id="d4d05-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d4d05-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d4d05-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d4d05-110">Child elements</span></span>

|<span data-ttu-id="d4d05-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d4d05-111">**Element**</span></span>|<span data-ttu-id="d4d05-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d4d05-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d4d05-113">Start</span><span class="sxs-lookup"><span data-stu-id="d4d05-113">Start</span></span>](start.md) <br/> |<span data-ttu-id="d4d05-114">Representa la hora de inicio de una repetición eliminada de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="d4d05-114">Represents the start time of a deleted occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d4d05-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d4d05-115">Parent elements</span></span>

|<span data-ttu-id="d4d05-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d4d05-116">**Element**</span></span>|<span data-ttu-id="d4d05-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d4d05-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d4d05-118">DeletedOccurrences</span><span class="sxs-lookup"><span data-stu-id="d4d05-118">DeletedOccurrences</span></span>](deletedoccurrences.md) <br/> |<span data-ttu-id="d4d05-119">Contiene una matriz de eliminado apariciones de un elemento periódico del calendario.</span><span class="sxs-lookup"><span data-stu-id="d4d05-119">Contains an array of deleted occurrences of a recurring calendar item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4d05-120">Notas</span><span class="sxs-lookup"><span data-stu-id="d4d05-120">Remarks</span></span>

<span data-ttu-id="d4d05-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d4d05-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d4d05-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d4d05-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d4d05-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d4d05-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d4d05-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d4d05-124">Schema name</span></span>  <br/> |<span data-ttu-id="d4d05-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d4d05-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="d4d05-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d4d05-126">Validation file</span></span>  <br/> |<span data-ttu-id="d4d05-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d4d05-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d4d05-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d4d05-128">Can be empty</span></span>  <br/> |<span data-ttu-id="d4d05-129">False</span><span class="sxs-lookup"><span data-stu-id="d4d05-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d4d05-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="d4d05-130">See also</span></span>

- [<span data-ttu-id="d4d05-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d4d05-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)  
- [<span data-ttu-id="d4d05-132">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="d4d05-132">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

