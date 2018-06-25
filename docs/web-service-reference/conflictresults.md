---
title: ConflictResults
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConflictResults
api_type:
- schema
ms.assetid: 08cdd547-4de7-4c7a-b60f-e618dc217d20
description: El elemento ConflictResults contiene el número de conflictos en una respuesta de operación UpdateItem.
ms.openlocfilehash: faa6dc6c5fbbe874438a89c810a12fa675e8a1c9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763773"
---
# <a name="conflictresults"></a><span data-ttu-id="69170-103">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="69170-103">ConflictResults</span></span>

<span data-ttu-id="69170-104">El elemento [ConflictResults](conflictresults.md) contiene el número de conflictos en una respuesta de [la operación UpdateItem](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="69170-104">The [ConflictResults](conflictresults.md) element contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span> 
  
[<span data-ttu-id="69170-105">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="69170-105">UpdateItemResponse</span></span>](updateitemresponse.md)
  
[<span data-ttu-id="69170-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="69170-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="69170-107">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="69170-107">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
  
[<span data-ttu-id="69170-108">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="69170-108">ConflictResults</span></span>](conflictresults.md)
  
```xml
<ConflictResults>
   <Count/>
</ConflictResults>
```

 <span data-ttu-id="69170-109">**ConflictResultsType**</span><span class="sxs-lookup"><span data-stu-id="69170-109">**ConflictResultsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="69170-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="69170-110">Attributes and elements</span></span>

<span data-ttu-id="69170-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="69170-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69170-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="69170-112">Attributes</span></span>

<span data-ttu-id="69170-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="69170-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="69170-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="69170-114">Child elements</span></span>

|<span data-ttu-id="69170-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="69170-115">**Element**</span></span>|<span data-ttu-id="69170-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69170-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69170-117">Count</span><span class="sxs-lookup"><span data-stu-id="69170-117">Count</span></span>](count.md) <br/> |<span data-ttu-id="69170-118">Contiene el número de conflictos en una respuesta de [la operación UpdateItem](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="69170-118">Contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="69170-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="69170-119">Parent elements</span></span>

|<span data-ttu-id="69170-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="69170-120">**Element**</span></span>|<span data-ttu-id="69170-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69170-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69170-122">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="69170-122">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md) <br/> |<span data-ttu-id="69170-123">Contiene el estado y el resultado de una única solicitud de [operación UpdateItem](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="69170-123">Contains the status and result of a single [UpdateItem operation](updateitem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69170-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="69170-124">Remarks</span></span>

<span data-ttu-id="69170-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con la función de servidor de acceso de cliente instalada.</span><span class="sxs-lookup"><span data-stu-id="69170-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69170-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="69170-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69170-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="69170-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="69170-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="69170-128">Schema Name</span></span>  <br/> |<span data-ttu-id="69170-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="69170-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="69170-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="69170-130">Validation File</span></span>  <br/> |<span data-ttu-id="69170-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="69170-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="69170-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="69170-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="69170-133">False</span><span class="sxs-lookup"><span data-stu-id="69170-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69170-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="69170-134">See also</span></span>



[<span data-ttu-id="69170-135">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="69170-135">UpdateItem operation</span></span>](updateitem-operation.md)
  
 <span data-ttu-id="69170-136">**ConflictResultsType**</span><span class="sxs-lookup"><span data-stu-id="69170-136">**ConflictResultsType**</span></span>

