---
title: FindItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindItem
api_type:
- schema
ms.assetid: f7624f5c-c390-4563-ab9a-08f1024fb914
description: El elemento FindItem define una solicitud para buscar elementos en un buzón.
ms.openlocfilehash: 3aeda1cffc03292734a91bc3fff3289d51c9b445
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460998"
---
# <a name="finditem"></a><span data-ttu-id="af011-103">FindItem</span><span class="sxs-lookup"><span data-stu-id="af011-103">FindItem</span></span>

<span data-ttu-id="af011-104">El elemento **FindItem** define una solicitud para buscar elementos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="af011-104">The **FindItem** element defines a request to find items in a mailbox.</span></span> 
  
```xml
<FindItem Traversal="">
   <ItemShape/>
   <IndexedPageItemView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <IndexedPageItemView/>
   <DistinguishedGroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <ContactsView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <ContactsView/> 
   <DistinguishedGroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <CalendarView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <FractionalPageItemView/>
   <GroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```

```xml
<FindItem Traversal="">
   <ItemShape/>
   <FractionalPageItemView/>
   <DistinguishedGroupBy/>
   <Restriction/>
   <SortOrder/>
   <ParentFolderIds/>
   <QueryString/>
</FindItem>
```


<span data-ttu-id="af011-105">**FindItemType**</span><span class="sxs-lookup"><span data-stu-id="af011-105">**FindItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="af011-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="af011-106">Attributes and elements</span></span>

<span data-ttu-id="af011-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="af011-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af011-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="af011-108">Attributes</span></span>

|<span data-ttu-id="af011-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="af011-109">**Attribute**</span></span>|<span data-ttu-id="af011-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="af011-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="af011-111">**Transversal**</span><span class="sxs-lookup"><span data-stu-id="af011-111">**Traversal**</span></span> <br/> |<span data-ttu-id="af011-112">Define si la búsqueda encuentra elementos en las carpetas o en los supercontenedores de las carpetas.</span><span class="sxs-lookup"><span data-stu-id="af011-112">Defines whether the search finds items in folders or the folders' dumpsters.</span></span> <span data-ttu-id="af011-113">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="af011-113">This attribute is required.</span></span>  <br/> |
   
#### <a name="traversal-attribute-values"></a><span data-ttu-id="af011-114">Valores de atributo de recorrido</span><span class="sxs-lookup"><span data-stu-id="af011-114">Traversal attribute values</span></span>

|<span data-ttu-id="af011-115">**Valor**</span><span class="sxs-lookup"><span data-stu-id="af011-115">**Value**</span></span>|<span data-ttu-id="af011-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="af011-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="af011-117">Profunda</span><span class="sxs-lookup"><span data-stu-id="af011-117">Shallow</span></span>  <br/> |<span data-ttu-id="af011-118">Devuelve solo las identidades de los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="af011-118">Returns only the identities of items in the folder.</span></span>  <br/> |
|<span data-ttu-id="af011-119">SoftDeleted</span><span class="sxs-lookup"><span data-stu-id="af011-119">SoftDeleted</span></span>  <br/> |<span data-ttu-id="af011-120">Devuelve solo las identidades de los elementos que están en el contenedor de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="af011-120">Returns only the identities of items that are in a folder's dumpster.</span></span> <span data-ttu-id="af011-121">Tenga en cuenta que un recorrido de eliminación temporal combinado con una restricción de búsqueda dará como resultado la devolución de elementos cero, incluso si hay elementos que coinciden con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="af011-121">Note that a soft-deleted traversal combined with a search restriction will result in zero items returned even if there are items that match the search criteria.</span></span>  <br/> |
|<span data-ttu-id="af011-122">Están</span><span class="sxs-lookup"><span data-stu-id="af011-122">Associated</span></span>  <br/> |<span data-ttu-id="af011-123">Devuelve solo las identidades de los elementos asociados de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="af011-123">Returns only the identities of associated items in the folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="af011-124">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="af011-124">Child elements</span></span>

|<span data-ttu-id="af011-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="af011-125">**Element**</span></span>|<span data-ttu-id="af011-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="af011-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af011-127">ItemShape</span><span class="sxs-lookup"><span data-stu-id="af011-127">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="af011-128">Identifica las propiedades del elemento y el contenido que se deben incluir en una respuesta de la [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="af011-128">Identifies the item properties and content to include in a [FindItem operation](finditem-operation.md) response.</span></span>  <br/> |
|[<span data-ttu-id="af011-129">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="af011-129">IndexedPageItemView</span></span>](indexedpageitemview.md) <br/> |<span data-ttu-id="af011-130">Describe cómo se devuelve la información de elementos paginados para una solicitud **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="af011-130">Describes how paged item information is returned for a **FindItem** request.</span></span> <span data-ttu-id="af011-131">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="af011-131">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="af011-132">FractionalPageItemView</span><span class="sxs-lookup"><span data-stu-id="af011-132">FractionalPageItemView</span></span>](fractionalpageitemview.md) <br/> |<span data-ttu-id="af011-133">Describe dónde se inicia la vista paginada y el número máximo de elementos devueltos en una solicitud **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="af011-133">Describes where the paged view starts and the maximum number of items returned in a **FindItem** request.</span></span> <span data-ttu-id="af011-134">El desplazamiento de la vista paginada desde el principio del conjunto de elementos encontrados se describe mediante una fracción.</span><span class="sxs-lookup"><span data-stu-id="af011-134">The paged view offset from the beginning of the set of found items is described by a fraction.</span></span> <span data-ttu-id="af011-135">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="af011-135">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="af011-136">CalendarView</span><span class="sxs-lookup"><span data-stu-id="af011-136">CalendarView</span></span>](calendarview.md) <br/> |<span data-ttu-id="af011-137">Proporciona límites de tiempo para definir una búsqueda para los elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="af011-137">Provides time span limits to define a search for calendar items.</span></span> <span data-ttu-id="af011-138">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="af011-138">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="af011-139">ContactsView</span><span class="sxs-lookup"><span data-stu-id="af011-139">ContactsView</span></span>](contactsview.md) <br/> |<span data-ttu-id="af011-140">Define una búsqueda para los elementos de contacto basándose en los nombres para mostrar alfabéticos.</span><span class="sxs-lookup"><span data-stu-id="af011-140">Defines a search for contact items based on alphabetical display names.</span></span> <span data-ttu-id="af011-141">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="af011-141">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="af011-142">GroupBy</span><span class="sxs-lookup"><span data-stu-id="af011-142">GroupBy</span></span>](groupby.md) <br/> |<span data-ttu-id="af011-143">Especifica agrupaciones arbitrarias para consultas **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="af011-143">Specifies arbitrary groupings for **FindItem** queries.</span></span> <span data-ttu-id="af011-144">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="af011-144">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="af011-145">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="af011-145">DistinguishedGroupBy</span></span>](distinguishedgroupby.md) <br/> |<span data-ttu-id="af011-146">Proporciona agrupaciones estándar para las consultas **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="af011-146">Provides standard groupings for **FindItem** queries.</span></span> <span data-ttu-id="af011-147">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="af011-147">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="af011-148">Restriction</span><span class="sxs-lookup"><span data-stu-id="af011-148">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="af011-149">Define la restricción o consulta que se usa para filtrar elementos o carpetas **FindItem**en /  las operaciones de carpeta de**FindFolder** y de búsqueda de la FindItem.</span><span class="sxs-lookup"><span data-stu-id="af011-149">Defines the restriction or query that is used to filter items or folders in **FindItem**/ **FindFolder** and search folder operations.</span></span> <span data-ttu-id="af011-150">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="af011-150">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="af011-151">SortOrder</span><span class="sxs-lookup"><span data-stu-id="af011-151">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="af011-152">Define cómo se ordenan los elementos en una solicitud FindItem.</span><span class="sxs-lookup"><span data-stu-id="af011-152">Defines how items are sorted in a FindItem request.</span></span> <span data-ttu-id="af011-153">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="af011-153">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="af011-154">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="af011-154">ParentFolderIds</span></span>](parentfolderids.md) <br/> |<span data-ttu-id="af011-155">Identifica las carpetas para buscar las operaciones FindItem y FindFolder.</span><span class="sxs-lookup"><span data-stu-id="af011-155">Identifies folders to search for the FindItem and FindFolder operations.</span></span>  <br/> |
|[<span data-ttu-id="af011-156">QueryString (QueryStringType)</span><span class="sxs-lookup"><span data-stu-id="af011-156">QueryString (QueryStringType)</span></span>](querystring-querystringtype.md) <br/> |<span data-ttu-id="af011-157">Contiene una cadena de consulta de buzón basada en la sintaxis de consulta avanzada (AQS).</span><span class="sxs-lookup"><span data-stu-id="af011-157">Contains a mailbox query string based on Advanced Query Syntax (AQS).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="af011-158">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="af011-158">Parent elements</span></span>

<span data-ttu-id="af011-159">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="af011-159">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="af011-160">Comentarios</span><span class="sxs-lookup"><span data-stu-id="af011-160">Remarks</span></span>

<span data-ttu-id="af011-161">Solo se puede incluir uno de los elementos [IndexedPageItemView](indexedpageitemview.md), [FractionalPageItemView](fractionalpageitemview.md), [CalendarView](calendarview.md)o [ContactsView](contactsview.md) en una solicitud **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="af011-161">Only one of the [IndexedPageItemView](indexedpageitemview.md), [FractionalPageItemView](fractionalpageitemview.md), [CalendarView](calendarview.md), or [ContactsView](contactsview.md) elements can be included in a **FindItem** request.</span></span> <span data-ttu-id="af011-162">Solo se puede incluir uno de los elementos [GroupBy](groupby.md) o [DistinguishedGroupBy](distinguishedgroupby.md) en una solicitud **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="af011-162">Only one of the [GroupBy](groupby.md) or [DistinguishedGroupBy](distinguishedgroupby.md) elements can be included in a **FindItem** request.</span></span> 
  
<span data-ttu-id="af011-163">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="af011-163">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="af011-164">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="af011-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af011-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="af011-165">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="af011-166">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="af011-166">Schema Name</span></span>  <br/> |<span data-ttu-id="af011-167">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="af011-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="af011-168">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="af011-168">Validation File</span></span>  <br/> |<span data-ttu-id="af011-169">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="af011-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="af011-170">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="af011-170">Can be Empty</span></span>  <br/> |<span data-ttu-id="af011-171">Falso</span><span class="sxs-lookup"><span data-stu-id="af011-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af011-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="af011-172">See also</span></span>

- [<span data-ttu-id="af011-173">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="af011-173">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="af011-174">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="af011-174">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

