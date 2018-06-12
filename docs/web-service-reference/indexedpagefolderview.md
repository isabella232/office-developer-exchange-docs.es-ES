---
title: IndexedPageFolderView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndexedPageFolderView
api_type:
- schema
ms.assetid: c6dac232-244b-4db0-9a15-5e01b8aa7a7d
description: El elemento IndexedPageFolderView describe cómo paginada elemento de información se devuelve en una respuesta FindFolder.
ms.openlocfilehash: f32f778daa6fa3fea93ab2bc1951f2407dcf7f80
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835910"
---
# <a name="indexedpagefolderview"></a><span data-ttu-id="72139-103">IndexedPageFolderView</span><span class="sxs-lookup"><span data-stu-id="72139-103">IndexedPageFolderView</span></span>

<span data-ttu-id="72139-104">El elemento **IndexedPageFolderView** describe cómo paginada elemento de información se devuelve en una respuesta [FindFolder](findfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="72139-104">The **IndexedPageFolderView** element describes how paged item information is returned in a [FindFolder](findfolder.md) response.</span></span> 
  
[<span data-ttu-id="72139-105">FindFolder</span><span class="sxs-lookup"><span data-stu-id="72139-105">FindFolder</span></span>](findfolder.md)
  
[<span data-ttu-id="72139-106">IndexedPageFolderView</span><span class="sxs-lookup"><span data-stu-id="72139-106">IndexedPageFolderView</span></span>](indexedpagefolderview.md)
  
```xml
<IndexedPageFolderView MaxEntriesReturned="" Offset="" BasePoint="" />
```

 <span data-ttu-id="72139-107">**IndexedPageViewType**</span><span class="sxs-lookup"><span data-stu-id="72139-107">**IndexedPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="72139-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="72139-108">Attributes and elements</span></span>

<span data-ttu-id="72139-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="72139-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="72139-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="72139-110">Attributes</span></span>

|<span data-ttu-id="72139-111">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="72139-111">**Attribute**</span></span>|<span data-ttu-id="72139-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="72139-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="72139-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="72139-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="72139-114">Describe el número máximo de carpetas para devolver en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="72139-114">Describes the maximum number of folders to return in the response.</span></span> <span data-ttu-id="72139-115">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="72139-115">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="72139-116">**Offset**</span><span class="sxs-lookup"><span data-stu-id="72139-116">**Offset**</span></span> <br/> |<span data-ttu-id="72139-117">Describe el desplazamiento desde el **punto base**.</span><span class="sxs-lookup"><span data-stu-id="72139-117">Describes the offset from the **BasePoint**.</span></span> <span data-ttu-id="72139-118">Desplazamiento debe ser mayor o igual que cero.</span><span class="sxs-lookup"><span data-stu-id="72139-118">Offset must be greater than or equal to zero.</span></span> <span data-ttu-id="72139-119">Si el **punto base** es igual al principio, el desplazamiento es positivo.</span><span class="sxs-lookup"><span data-stu-id="72139-119">If **BasePoint** is equal to Beginning, the offset is positive.</span></span> <span data-ttu-id="72139-120">Si el **punto base** es igual a End, el desplazamiento se administra como si fuese negativo.</span><span class="sxs-lookup"><span data-stu-id="72139-120">If **BasePoint** is equal to End, the offset is handled as if it were negative.</span></span>  <br/> <span data-ttu-id="72139-121">Esto identifica qué carpeta será la primera carpeta de entrega en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="72139-121">This identifies which folder will be the first folder delivered in the response.</span></span> <span data-ttu-id="72139-122">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="72139-122">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="72139-123">**Punto base**</span><span class="sxs-lookup"><span data-stu-id="72139-123">**BasePoint**</span></span> <br/> |<span data-ttu-id="72139-124">Describe si la página de las carpetas se iniciará desde el principio o el final del conjunto de carpetas que se encuentran con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="72139-124">Describes whether the page of folders will start from the start or the end of the set of folders that are found with the search criteria.</span></span> <span data-ttu-id="72139-125">Buscar desde el final siempre busca hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="72139-125">Seeking from the end always searches backward.</span></span> <span data-ttu-id="72139-126">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="72139-126">This attribute is required.</span></span>  <br/> |
   
#### <a name="basepoint-attribute"></a><span data-ttu-id="72139-127">Atributo de punto base</span><span class="sxs-lookup"><span data-stu-id="72139-127">BasePoint Attribute</span></span>

|<span data-ttu-id="72139-128">**Valor**</span><span class="sxs-lookup"><span data-stu-id="72139-128">**Value**</span></span>|<span data-ttu-id="72139-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="72139-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="72139-130">Principio</span><span class="sxs-lookup"><span data-stu-id="72139-130">Beginning</span></span>  <br/> |<span data-ttu-id="72139-131">La vista de página comienza al principio del conjunto de carpetas que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="72139-131">The paged view starts at the beginning of the found folder set.</span></span>  <br/> |
|<span data-ttu-id="72139-132">End</span><span class="sxs-lookup"><span data-stu-id="72139-132">End</span></span>  <br/> |<span data-ttu-id="72139-133">Se inicia la vista de página al final del conjunto de carpetas que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="72139-133">The paged view starts at the end of the found folder set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="72139-134">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="72139-134">Child elements</span></span>

<span data-ttu-id="72139-135">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="72139-135">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="72139-136">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="72139-136">Parent elements</span></span>

|<span data-ttu-id="72139-137">**Element**</span><span class="sxs-lookup"><span data-stu-id="72139-137">**Element**</span></span>|<span data-ttu-id="72139-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="72139-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="72139-139">FindFolder</span><span class="sxs-lookup"><span data-stu-id="72139-139">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="72139-140">Define una solicitud para buscar las carpetas en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="72139-140">Defines a request to find folders in a mailbox.</span></span>  <br/> <span data-ttu-id="72139-141">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="72139-141">The following is the XPath expression to this element:</span></span>  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72139-142">Notas</span><span class="sxs-lookup"><span data-stu-id="72139-142">Remarks</span></span>

<span data-ttu-id="72139-143">Solicitando a end implica mover para el origen identificado por el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="72139-143">Seeking from end involves moving to the origin identified by the offset.</span></span> <span data-ttu-id="72139-144">Además, el puntero se mueve de nuevo el número de registros solicitados.</span><span class="sxs-lookup"><span data-stu-id="72139-144">Additionally, the pointer is moved back by the number of requested records.</span></span> <span data-ttu-id="72139-145">Por ejemplo, si hay 100 registros y el desplazamiento es 25 desde el final, la búsqueda comienza desde 75.</span><span class="sxs-lookup"><span data-stu-id="72139-145">For example, if there are 100 records and the offset is 25 from the end, the search starts from 75.</span></span> <span data-ttu-id="72139-146">Si se devuelven 10 registros, el puntero se mueve hacia atrás un 10 adicionales a 65 de registros y devuelve los registros 65 a través de 75.</span><span class="sxs-lookup"><span data-stu-id="72139-146">If 10 records are returned, the pointer is moved backward an additional 10 records to 65 and returns records 65 through 75.</span></span> <span data-ttu-id="72139-147">El siguiente índice es 64.</span><span class="sxs-lookup"><span data-stu-id="72139-147">The next index is 64.</span></span> <span data-ttu-id="72139-148">El desplazamiento desde el final de una página siguiente es 100 menos 64 que es igual a 36.</span><span class="sxs-lookup"><span data-stu-id="72139-148">The next offset from the end for a page is 100 minus 64 which equals 36.</span></span> <span data-ttu-id="72139-149">El valor para el desvío siguiente desde el final para obtener la siguiente página indizada es 36.</span><span class="sxs-lookup"><span data-stu-id="72139-149">The value for the next offset from the end to get the next indexed page is 36.</span></span>
  
<span data-ttu-id="72139-150">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="72139-150">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="72139-151">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="72139-151">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72139-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="72139-152">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="72139-153">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="72139-153">Schema Name</span></span>  <br/> |<span data-ttu-id="72139-154">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="72139-154">Messages schema</span></span>  <br/> |
|<span data-ttu-id="72139-155">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="72139-155">Validation File</span></span>  <br/> |<span data-ttu-id="72139-156">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="72139-156">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="72139-157">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="72139-157">Can be Empty</span></span>  <br/> |<span data-ttu-id="72139-158">False</span><span class="sxs-lookup"><span data-stu-id="72139-158">False</span></span>  <br/> |
   

