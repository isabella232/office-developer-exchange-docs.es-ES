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
description: El elemento IndexedPageFolderView describe cómo se devuelve la información del elemento paginado en una respuesta FindFolder.
ms.openlocfilehash: 6e9e2796c0bdcd9a15487f0e1bc7cbdf09d0a492
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457203"
---
# <a name="indexedpagefolderview"></a><span data-ttu-id="85635-103">IndexedPageFolderView</span><span class="sxs-lookup"><span data-stu-id="85635-103">IndexedPageFolderView</span></span>

<span data-ttu-id="85635-104">El elemento **IndexedPageFolderView** describe cómo se devuelve la información del elemento paginado en una respuesta [FindFolder](findfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="85635-104">The **IndexedPageFolderView** element describes how paged item information is returned in a [FindFolder](findfolder.md) response.</span></span> 
  
[<span data-ttu-id="85635-105">FindFolder</span><span class="sxs-lookup"><span data-stu-id="85635-105">FindFolder</span></span>](findfolder.md)
  
[<span data-ttu-id="85635-106">IndexedPageFolderView</span><span class="sxs-lookup"><span data-stu-id="85635-106">IndexedPageFolderView</span></span>](indexedpagefolderview.md)
  
```xml
<IndexedPageFolderView MaxEntriesReturned="" Offset="" BasePoint="" />
```

 <span data-ttu-id="85635-107">**IndexedPageViewType**</span><span class="sxs-lookup"><span data-stu-id="85635-107">**IndexedPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85635-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="85635-108">Attributes and elements</span></span>

<span data-ttu-id="85635-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="85635-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85635-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="85635-110">Attributes</span></span>

|<span data-ttu-id="85635-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="85635-111">**Attribute**</span></span>|<span data-ttu-id="85635-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85635-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85635-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="85635-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="85635-114">Describe el número máximo de carpetas que se devolverá en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="85635-114">Describes the maximum number of folders to return in the response.</span></span> <span data-ttu-id="85635-115">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="85635-115">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="85635-116">**Offset**</span><span class="sxs-lookup"><span data-stu-id="85635-116">**Offset**</span></span> <br/> |<span data-ttu-id="85635-117">Describe el desplazamiento desde **BasePoint**.</span><span class="sxs-lookup"><span data-stu-id="85635-117">Describes the offset from the **BasePoint**.</span></span> <span data-ttu-id="85635-118">El desplazamiento debe ser mayor o igual que cero.</span><span class="sxs-lookup"><span data-stu-id="85635-118">Offset must be greater than or equal to zero.</span></span> <span data-ttu-id="85635-119">Si **BasePoint** es igual al principio, el desplazamiento es positivo.</span><span class="sxs-lookup"><span data-stu-id="85635-119">If **BasePoint** is equal to Beginning, the offset is positive.</span></span> <span data-ttu-id="85635-120">Si **BasePoint** es igual a end, el desplazamiento se trata como si fuera negativo.</span><span class="sxs-lookup"><span data-stu-id="85635-120">If **BasePoint** is equal to End, the offset is handled as if it were negative.</span></span>  <br/> <span data-ttu-id="85635-121">Esto identifica la carpeta que será la primera carpeta entregada en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="85635-121">This identifies which folder will be the first folder delivered in the response.</span></span> <span data-ttu-id="85635-122">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="85635-122">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="85635-123">**BasePoint**</span><span class="sxs-lookup"><span data-stu-id="85635-123">**BasePoint**</span></span> <br/> |<span data-ttu-id="85635-124">Describe si la página de carpetas se iniciará desde el principio o el final del conjunto de carpetas que se encuentren con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="85635-124">Describes whether the page of folders will start from the start or the end of the set of folders that are found with the search criteria.</span></span> <span data-ttu-id="85635-125">Buscar desde el final siempre busca hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="85635-125">Seeking from the end always searches backward.</span></span> <span data-ttu-id="85635-126">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="85635-126">This attribute is required.</span></span>  <br/> |
   
#### <a name="basepoint-attribute"></a><span data-ttu-id="85635-127">Atributo BasePoint</span><span class="sxs-lookup"><span data-stu-id="85635-127">BasePoint Attribute</span></span>

|<span data-ttu-id="85635-128">**Valor**</span><span class="sxs-lookup"><span data-stu-id="85635-128">**Value**</span></span>|<span data-ttu-id="85635-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85635-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85635-130">Empezar</span><span class="sxs-lookup"><span data-stu-id="85635-130">Beginning</span></span>  <br/> |<span data-ttu-id="85635-131">La vista paginada comienza al principio del conjunto de carpetas encontradas.</span><span class="sxs-lookup"><span data-stu-id="85635-131">The paged view starts at the beginning of the found folder set.</span></span>  <br/> |
|<span data-ttu-id="85635-132">End</span><span class="sxs-lookup"><span data-stu-id="85635-132">End</span></span>  <br/> |<span data-ttu-id="85635-133">La vista paginada se inicia al final del conjunto de carpetas encontradas.</span><span class="sxs-lookup"><span data-stu-id="85635-133">The paged view starts at the end of the found folder set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="85635-134">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="85635-134">Child elements</span></span>

<span data-ttu-id="85635-135">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="85635-135">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="85635-136">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="85635-136">Parent elements</span></span>

|<span data-ttu-id="85635-137">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="85635-137">**Element**</span></span>|<span data-ttu-id="85635-138">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="85635-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85635-139">FindFolder</span><span class="sxs-lookup"><span data-stu-id="85635-139">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="85635-140">Define una solicitud para buscar carpetas en un buzón.</span><span class="sxs-lookup"><span data-stu-id="85635-140">Defines a request to find folders in a mailbox.</span></span>  <br/> <span data-ttu-id="85635-141">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="85635-141">The following is the XPath expression to this element:</span></span>  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85635-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="85635-142">Remarks</span></span>

<span data-ttu-id="85635-143">La búsqueda en el final implica moverse al origen identificado por el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="85635-143">Seeking from end involves moving to the origin identified by the offset.</span></span> <span data-ttu-id="85635-144">Además, el puntero se mueve hacia atrás el número de registros solicitados.</span><span class="sxs-lookup"><span data-stu-id="85635-144">Additionally, the pointer is moved back by the number of requested records.</span></span> <span data-ttu-id="85635-145">Por ejemplo, si hay 100 registros y el desplazamiento es 25 desde el final, la búsqueda se inicia desde 75.</span><span class="sxs-lookup"><span data-stu-id="85635-145">For example, if there are 100 records and the offset is 25 from the end, the search starts from 75.</span></span> <span data-ttu-id="85635-146">Si se devuelven 10 registros, el puntero se mueve hacia atrás unos 10 registros adicionales a 65 y devuelve los registros 65 a 75.</span><span class="sxs-lookup"><span data-stu-id="85635-146">If 10 records are returned, the pointer is moved backward an additional 10 records to 65 and returns records 65 through 75.</span></span> <span data-ttu-id="85635-147">El siguiente índice es 64.</span><span class="sxs-lookup"><span data-stu-id="85635-147">The next index is 64.</span></span> <span data-ttu-id="85635-148">El siguiente desplazamiento desde el final de una página es 100 menos 64, que es igual a 36.</span><span class="sxs-lookup"><span data-stu-id="85635-148">The next offset from the end for a page is 100 minus 64 which equals 36.</span></span> <span data-ttu-id="85635-149">El valor del siguiente desplazamiento desde el final para obtener la siguiente página indizada es 36.</span><span class="sxs-lookup"><span data-stu-id="85635-149">The value for the next offset from the end to get the next indexed page is 36.</span></span>
  
<span data-ttu-id="85635-150">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="85635-150">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85635-151">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="85635-151">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85635-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="85635-152">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="85635-153">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="85635-153">Schema Name</span></span>  <br/> |<span data-ttu-id="85635-154">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="85635-154">Messages schema</span></span>  <br/> |
|<span data-ttu-id="85635-155">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="85635-155">Validation File</span></span>  <br/> |<span data-ttu-id="85635-156">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="85635-156">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="85635-157">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="85635-157">Can be Empty</span></span>  <br/> |<span data-ttu-id="85635-158">Falso</span><span class="sxs-lookup"><span data-stu-id="85635-158">False</span></span>  <br/> |
   

