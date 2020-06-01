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
description: El elemento RootFolder contiene los resultados de una búsqueda de una sola carpeta raíz durante una operación FindFolder.
ms.openlocfilehash: b5601d6abec67196c9991908e272a2122a201d69
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457140"
---
# <a name="rootfolder-findfolderresponsemessage"></a><span data-ttu-id="bd70f-103">RootFolder (FindFolderResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="bd70f-103">RootFolder (FindFolderResponseMessage)</span></span>

<span data-ttu-id="bd70f-104">El elemento **RootFolder** contiene los resultados de una búsqueda de una sola carpeta raíz durante una [operación FindFolder](findfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="bd70f-104">The **RootFolder** element contains the results of a search of a single root folder during a [FindFolder operation](findfolder-operation.md).</span></span>
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Folders/>
</RootFolder>
```

 <span data-ttu-id="bd70f-105">**FindFolderParentType**</span><span class="sxs-lookup"><span data-stu-id="bd70f-105">**FindFolderParentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bd70f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bd70f-106">Attributes and elements</span></span>

<span data-ttu-id="bd70f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bd70f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd70f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="bd70f-108">Attributes</span></span>

|<span data-ttu-id="bd70f-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="bd70f-109">**Attribute**</span></span>|<span data-ttu-id="bd70f-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bd70f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bd70f-111">IndexedPagingOffset</span><span class="sxs-lookup"><span data-stu-id="bd70f-111">IndexedPagingOffset</span></span>  <br/> |<span data-ttu-id="bd70f-112">Representa el siguiente índice que se debe usar para la siguiente solicitud al usar una vista de paginación indizada.</span><span class="sxs-lookup"><span data-stu-id="bd70f-112">Represents the next index that should be used for the next request when using an indexed paging view.</span></span>  <br/> |
|<span data-ttu-id="bd70f-113">NumeratorOffset</span><span class="sxs-lookup"><span data-stu-id="bd70f-113">NumeratorOffset</span></span>  <br/> |<span data-ttu-id="bd70f-114">Representa el nuevo valor del numerador que se va a usar para la siguiente solicitud cuando se usan vistas de página fraccionarias.</span><span class="sxs-lookup"><span data-stu-id="bd70f-114">Represents the new numerator value to use for the next request when using fractional page views.</span></span>  <br/> |
|<span data-ttu-id="bd70f-115">AbsoluteDenominator</span><span class="sxs-lookup"><span data-stu-id="bd70f-115">AbsoluteDenominator</span></span>  <br/> |<span data-ttu-id="bd70f-116">Representa el siguiente denominador que se va a usar para la siguiente solicitud cuando se realiza una paginación fraccionada.</span><span class="sxs-lookup"><span data-stu-id="bd70f-116">Represents the next denominator to use for the next request when doing fractional paging.</span></span>  <br/> |
|<span data-ttu-id="bd70f-117">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="bd70f-117">IncludesLastItemInRange</span></span>  <br/> |<span data-ttu-id="bd70f-118">Indica si los resultados actuales contienen la última carpeta de la consulta, de modo que no es necesario realizar más paginación.</span><span class="sxs-lookup"><span data-stu-id="bd70f-118">Indicates whether the current results contain the last folder in the query, such that further paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="bd70f-119">TotalItemsInView</span><span class="sxs-lookup"><span data-stu-id="bd70f-119">TotalItemsInView</span></span>  <br/> |<span data-ttu-id="bd70f-120">Representa el número total de carpetas que superan la restricción.</span><span class="sxs-lookup"><span data-stu-id="bd70f-120">Represents the total number of folders that pass the restriction.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bd70f-121">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bd70f-121">Child elements</span></span>

|<span data-ttu-id="bd70f-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bd70f-122">**Element**</span></span>|<span data-ttu-id="bd70f-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bd70f-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd70f-124">Folders</span><span class="sxs-lookup"><span data-stu-id="bd70f-124">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="bd70f-125">Contiene una matriz de carpetas que se han encontrado mediante la [operación FindFolder](findfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="bd70f-125">Contains an array of folders found by using the [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bd70f-126">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bd70f-126">Parent elements</span></span>

|<span data-ttu-id="bd70f-127">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bd70f-127">**Element**</span></span>|<span data-ttu-id="bd70f-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bd70f-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd70f-129">FindFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="bd70f-129">FindFolderResponseMessage</span></span>](findfolderresponsemessage.md) <br/> |<span data-ttu-id="bd70f-130">Contiene el estado y el resultado de una solicitud de [operación FindFolder](findfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="bd70f-130">Contains the status and result of a [FindFolder operation](findfolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd70f-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bd70f-131">Remarks</span></span>

<span data-ttu-id="bd70f-132">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="bd70f-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bd70f-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bd70f-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd70f-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="bd70f-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bd70f-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bd70f-135">Schema name</span></span>  <br/> |<span data-ttu-id="bd70f-136">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="bd70f-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bd70f-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bd70f-137">Validation file</span></span>  <br/> |<span data-ttu-id="bd70f-138">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="bd70f-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bd70f-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bd70f-139">Can be empty</span></span>  <br/> |<span data-ttu-id="bd70f-140">Falso</span><span class="sxs-lookup"><span data-stu-id="bd70f-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bd70f-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd70f-141">See also</span></span>



[<span data-ttu-id="bd70f-142">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="bd70f-142">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="bd70f-143">Buscar carpetas</span><span class="sxs-lookup"><span data-stu-id="bd70f-143">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

