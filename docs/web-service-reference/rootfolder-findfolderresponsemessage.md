---
title: RootFolder (FindFolderResponseMessage)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RootFolder
api_type:
- schema
ms.assetid: 5089c815-663f-46be-bc59-aed9ee20f94a
description: El elemento RootFolder contiene los resultados de una búsqueda de una sola carpeta raíz durante una operación de FindFolder.
ms.openlocfilehash: 1cd79d5fa34318e7fe29606df84cbf0ef0520b93
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837253"
---
# <a name="rootfolder-findfolderresponsemessage"></a><span data-ttu-id="05855-103">RootFolder (FindFolderResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="05855-103">RootFolder (FindFolderResponseMessage)</span></span>

<span data-ttu-id="05855-104">El elemento **RootFolder** contiene los resultados de una búsqueda de una sola carpeta raíz durante una [operación de FindFolder](findfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="05855-104">The **RootFolder** element contains the results of a search of a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Folders/>
</RootFolder>
```

 <span data-ttu-id="05855-105">**FindFolderParentType**</span><span class="sxs-lookup"><span data-stu-id="05855-105">**FindFolderParentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="05855-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="05855-106">Attributes and elements</span></span>

<span data-ttu-id="05855-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="05855-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="05855-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="05855-108">Attributes</span></span>

|<span data-ttu-id="05855-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="05855-109">**Attribute**</span></span>|<span data-ttu-id="05855-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="05855-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="05855-111">IndexedPagingOffset</span><span class="sxs-lookup"><span data-stu-id="05855-111">IndexedPagingOffset</span></span>  <br/> |<span data-ttu-id="05855-112">Representa el siguiente índice que se debe usar para la solicitud siguiente cuando se usa una vista indizada de paginación.</span><span class="sxs-lookup"><span data-stu-id="05855-112">Represents the next index that should be used for the next request when using an indexed paging view.</span></span>  <br/> |
|<span data-ttu-id="05855-113">NumeratorOffset</span><span class="sxs-lookup"><span data-stu-id="05855-113">NumeratorOffset</span></span>  <br/> |<span data-ttu-id="05855-114">Representa el nuevo valor numerador debe usar para la solicitud siguiente con vistas de página fraccionaria.</span><span class="sxs-lookup"><span data-stu-id="05855-114">Represents the new numerator value to use for the next request when using fractional page views.</span></span>  <br/> |
|<span data-ttu-id="05855-115">AbsoluteDenominator</span><span class="sxs-lookup"><span data-stu-id="05855-115">AbsoluteDenominator</span></span>  <br/> |<span data-ttu-id="05855-116">Representa el denominador siguiente para usar para la solicitud siguiente al realizar la paginación fraccionaria.</span><span class="sxs-lookup"><span data-stu-id="05855-116">Represents the next denominator to use for the next request when doing fractional paging.</span></span>  <br/> |
|<span data-ttu-id="05855-117">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="05855-117">IncludesLastItemInRange</span></span>  <br/> |<span data-ttu-id="05855-118">Indica si los resultados actuales contienen la última carpeta en la consulta, por ejemplo, que no es necesaria la paginación aún más.</span><span class="sxs-lookup"><span data-stu-id="05855-118">Indicates whether the current results contain the last folder in the query, such that further paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="05855-119">TotalItemsInView</span><span class="sxs-lookup"><span data-stu-id="05855-119">TotalItemsInView</span></span>  <br/> |<span data-ttu-id="05855-120">Representa el número total de carpetas que pase la restricción.</span><span class="sxs-lookup"><span data-stu-id="05855-120">Represents the total number of folders that pass the restriction.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="05855-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="05855-121">Child elements</span></span>

|<span data-ttu-id="05855-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="05855-122">**Element**</span></span>|<span data-ttu-id="05855-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="05855-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05855-124">Carpetas</span><span class="sxs-lookup"><span data-stu-id="05855-124">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="05855-125">Contiene una matriz de carpetas que se encuentran mediante la [operación FindFolder](findfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="05855-125">Contains an array of folders found by using the [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="05855-126">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="05855-126">Parent elements</span></span>

|<span data-ttu-id="05855-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="05855-127">**Element**</span></span>|<span data-ttu-id="05855-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="05855-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05855-129">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="05855-129">FindFolderResponseMessage</span></span>](findfolderresponsemessage.md) <br/> |<span data-ttu-id="05855-130">Contiene el estado y el resultado de una solicitud de [operación FindFolder](findfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="05855-130">Contains the status and result of a [FindFolder operation](findfolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05855-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="05855-131">Remarks</span></span>

<span data-ttu-id="05855-132">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="05855-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05855-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="05855-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05855-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="05855-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="05855-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="05855-135">Schema name</span></span>  <br/> |<span data-ttu-id="05855-136">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="05855-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="05855-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="05855-137">Validation file</span></span>  <br/> |<span data-ttu-id="05855-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="05855-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="05855-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="05855-139">Can be empty</span></span>  <br/> |<span data-ttu-id="05855-140">False</span><span class="sxs-lookup"><span data-stu-id="05855-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05855-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="05855-141">See also</span></span>



[<span data-ttu-id="05855-142">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="05855-142">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="05855-143">Buscar carpetas</span><span class="sxs-lookup"><span data-stu-id="05855-143">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

