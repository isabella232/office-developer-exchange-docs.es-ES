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
description: El elemento ConflictResults contiene el número de conflictos en una respuesta de operación de UpdateItem.
ms.openlocfilehash: 923c7950e21039adf28e232486f4df5fc04889d1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460172"
---
# <a name="conflictresults"></a><span data-ttu-id="9ad73-103">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="9ad73-103">ConflictResults</span></span>

<span data-ttu-id="9ad73-104">El elemento [ConflictResults](conflictresults.md) contiene el número de conflictos en una respuesta de [operación de UpdateItem](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="9ad73-104">The [ConflictResults](conflictresults.md) element contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span> 
  
[<span data-ttu-id="9ad73-105">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="9ad73-105">UpdateItemResponse</span></span>](updateitemresponse.md)
  
[<span data-ttu-id="9ad73-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9ad73-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="9ad73-107">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9ad73-107">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
  
[<span data-ttu-id="9ad73-108">ConflictResults</span><span class="sxs-lookup"><span data-stu-id="9ad73-108">ConflictResults</span></span>](conflictresults.md)
  
```xml
<ConflictResults>
   <Count/>
</ConflictResults>
```

 <span data-ttu-id="9ad73-109">**ConflictResultsType**</span><span class="sxs-lookup"><span data-stu-id="9ad73-109">**ConflictResultsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9ad73-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9ad73-110">Attributes and elements</span></span>

<span data-ttu-id="9ad73-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9ad73-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9ad73-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="9ad73-112">Attributes</span></span>

<span data-ttu-id="9ad73-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9ad73-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9ad73-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9ad73-114">Child elements</span></span>

|<span data-ttu-id="9ad73-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9ad73-115">**Element**</span></span>|<span data-ttu-id="9ad73-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9ad73-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9ad73-117">Count</span><span class="sxs-lookup"><span data-stu-id="9ad73-117">Count</span></span>](count.md) <br/> |<span data-ttu-id="9ad73-118">Contiene el número de conflictos en una respuesta de [operación UpdateItem](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="9ad73-118">Contains the number of conflicts in an [UpdateItem operation](updateitem-operation.md) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9ad73-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9ad73-119">Parent elements</span></span>

|<span data-ttu-id="9ad73-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9ad73-120">**Element**</span></span>|<span data-ttu-id="9ad73-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9ad73-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9ad73-122">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="9ad73-122">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md) <br/> |<span data-ttu-id="9ad73-123">Contiene el estado y el resultado de una sola solicitud de [operación UpdateItem](updateitem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="9ad73-123">Contains the status and result of a single [UpdateItem operation](updateitem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ad73-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9ad73-124">Remarks</span></span>

<span data-ttu-id="9ad73-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con el rol de servidor acceso de clientes instalado.</span><span class="sxs-lookup"><span data-stu-id="9ad73-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9ad73-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9ad73-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ad73-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="9ad73-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9ad73-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9ad73-128">Schema Name</span></span>  <br/> |<span data-ttu-id="9ad73-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9ad73-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="9ad73-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9ad73-130">Validation File</span></span>  <br/> |<span data-ttu-id="9ad73-131">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="9ad73-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9ad73-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9ad73-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="9ad73-133">Falso</span><span class="sxs-lookup"><span data-stu-id="9ad73-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9ad73-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ad73-134">See also</span></span>



[<span data-ttu-id="9ad73-135">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="9ad73-135">UpdateItem operation</span></span>](updateitem-operation.md)
  
 <span data-ttu-id="9ad73-136">**ConflictResultsType**</span><span class="sxs-lookup"><span data-stu-id="9ad73-136">**ConflictResultsType**</span></span>

