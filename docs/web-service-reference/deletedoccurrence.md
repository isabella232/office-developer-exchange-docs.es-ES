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
description: El elemento DeletedOccurrence representa una ocurrencia eliminada de un elemento de calendario periódico.
ms.openlocfilehash: 814a81934786963ae5e7ea3a40406834c27b64ce
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457840"
---
# <a name="deletedoccurrence"></a><span data-ttu-id="ffa0a-103">DeletedOccurrence</span><span class="sxs-lookup"><span data-stu-id="ffa0a-103">DeletedOccurrence</span></span>

<span data-ttu-id="ffa0a-104">El elemento **DeletedOccurrence** representa una ocurrencia eliminada de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-104">The **DeletedOccurrence** element represents a deleted occurrence of a recurring calendar item.</span></span> 
  
```xml
<DeletedOccurrence>
   <Start/>
</DeletedOccurrence>
```

 <span data-ttu-id="ffa0a-105">**DeletedOccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="ffa0a-105">**DeletedOccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ffa0a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ffa0a-106">Attributes and elements</span></span>

<span data-ttu-id="ffa0a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ffa0a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ffa0a-108">Attributes</span></span>

<span data-ttu-id="ffa0a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ffa0a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ffa0a-110">Child elements</span></span>

|<span data-ttu-id="ffa0a-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ffa0a-111">**Element**</span></span>|<span data-ttu-id="ffa0a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ffa0a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ffa0a-113">Start</span><span class="sxs-lookup"><span data-stu-id="ffa0a-113">Start</span></span>](start.md) <br/> |<span data-ttu-id="ffa0a-114">Representa la hora de inicio de una ocurrencia eliminada de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-114">Represents the start time of a deleted occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ffa0a-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ffa0a-115">Parent elements</span></span>

|<span data-ttu-id="ffa0a-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ffa0a-116">**Element**</span></span>|<span data-ttu-id="ffa0a-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ffa0a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ffa0a-118">DeletedOccurrences</span><span class="sxs-lookup"><span data-stu-id="ffa0a-118">DeletedOccurrences</span></span>](deletedoccurrences.md) <br/> |<span data-ttu-id="ffa0a-119">Contiene una matriz de ocurrencias eliminadas de un elemento de calendario periódico.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-119">Contains an array of deleted occurrences of a recurring calendar item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffa0a-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ffa0a-120">Remarks</span></span>

<span data-ttu-id="ffa0a-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="ffa0a-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ffa0a-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ffa0a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ffa0a-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="ffa0a-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ffa0a-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ffa0a-124">Schema name</span></span>  <br/> |<span data-ttu-id="ffa0a-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ffa0a-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="ffa0a-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ffa0a-126">Validation file</span></span>  <br/> |<span data-ttu-id="ffa0a-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="ffa0a-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ffa0a-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ffa0a-128">Can be empty</span></span>  <br/> |<span data-ttu-id="ffa0a-129">Falso</span><span class="sxs-lookup"><span data-stu-id="ffa0a-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ffa0a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffa0a-130">See also</span></span>

- [<span data-ttu-id="ffa0a-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ffa0a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)  
- [<span data-ttu-id="ffa0a-132">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="ffa0a-132">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

