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
description: El elemento FindItem define una solicitud para buscar elementos en un buzón de correo.
ms.openlocfilehash: 6664cd91007f1d39db7e8d446e0135f47d5ab932
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353927"
---
# <a name="finditem"></a><span data-ttu-id="6a94a-103">FindItem</span><span class="sxs-lookup"><span data-stu-id="6a94a-103">FindItem</span></span>

<span data-ttu-id="6a94a-104">El elemento **FindItem** define una solicitud para buscar elementos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="6a94a-104">The **FindItem** element defines a request to find items in a mailbox.</span></span> 
  
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


<span data-ttu-id="6a94a-105">**FindItemType**</span><span class="sxs-lookup"><span data-stu-id="6a94a-105">**FindItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6a94a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6a94a-106">Attributes and elements</span></span>

<span data-ttu-id="6a94a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6a94a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6a94a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6a94a-108">Attributes</span></span>

|<span data-ttu-id="6a94a-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="6a94a-109">**Attribute**</span></span>|<span data-ttu-id="6a94a-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6a94a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6a94a-111">**Cruce seguro del**</span><span class="sxs-lookup"><span data-stu-id="6a94a-111">**Traversal**</span></span> <br/> |<span data-ttu-id="6a94a-112">Define si la búsqueda busca elementos en las carpetas o dumpsters de las carpetas.</span><span class="sxs-lookup"><span data-stu-id="6a94a-112">Defines whether the search finds items in folders or the folders' dumpsters.</span></span> <span data-ttu-id="6a94a-113">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="6a94a-113">This attribute is required.</span></span>  <br/> |
   
#### <a name="traversal-attribute-values"></a><span data-ttu-id="6a94a-114">Valores de atributo recorrido</span><span class="sxs-lookup"><span data-stu-id="6a94a-114">Traversal attribute values</span></span>

|<span data-ttu-id="6a94a-115">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6a94a-115">**Value**</span></span>|<span data-ttu-id="6a94a-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6a94a-116">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6a94a-117">Superficial</span><span class="sxs-lookup"><span data-stu-id="6a94a-117">Shallow</span></span>  <br/> |<span data-ttu-id="6a94a-118">Devuelve sólo las identidades de los elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="6a94a-118">Returns only the identities of items in the folder.</span></span>  <br/> |
|<span data-ttu-id="6a94a-119">SoftDeleted</span><span class="sxs-lookup"><span data-stu-id="6a94a-119">SoftDeleted</span></span>  <br/> |<span data-ttu-id="6a94a-120">Devuelve sólo las identidades de los elementos que se encuentran en una carpeta volcado de archivos.</span><span class="sxs-lookup"><span data-stu-id="6a94a-120">Returns only the identities of items that are in a folder's dumpster.</span></span> <span data-ttu-id="6a94a-121">Tenga en cuenta que dará como resultado un recorrido eliminado temporalmente combinado con una restricción de la búsqueda en cero los elementos devueltos incluso si hay elementos que coincidan con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6a94a-121">Note that a soft-deleted traversal combined with a search restriction will result in zero items returned even if there are items that match the search criteria.</span></span>  <br/> |
|<span data-ttu-id="6a94a-122">Asociado</span><span class="sxs-lookup"><span data-stu-id="6a94a-122">Associated</span></span>  <br/> |<span data-ttu-id="6a94a-123">Devuelve sólo las identidades de elementos asociados en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="6a94a-123">Returns only the identities of associated items in the folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6a94a-124">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6a94a-124">Child elements</span></span>

|<span data-ttu-id="6a94a-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="6a94a-125">**Element**</span></span>|<span data-ttu-id="6a94a-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6a94a-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6a94a-127">ItemShape</span><span class="sxs-lookup"><span data-stu-id="6a94a-127">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="6a94a-128">Identifica las propiedades de elemento y el contenido que desea incluir en una respuesta de [la operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="6a94a-128">Identifies the item properties and content to include in a [FindItem operation](finditem-operation.md) response.</span></span>  <br/> |
|[<span data-ttu-id="6a94a-129">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="6a94a-129">IndexedPageItemView</span></span>](indexedpageitemview.md) <br/> |<span data-ttu-id="6a94a-130">Describe cómo paginada elemento de información se devuelve para una solicitud de **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="6a94a-130">Describes how paged item information is returned for a **FindItem** request.</span></span> <span data-ttu-id="6a94a-131">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="6a94a-131">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="6a94a-132">FractionalPageItemView</span><span class="sxs-lookup"><span data-stu-id="6a94a-132">FractionalPageItemView</span></span>](fractionalpageitemview.md) <br/> |<span data-ttu-id="6a94a-133">Describe donde se inicia la vista de página y el número máximo de elementos devueltos en una solicitud de **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="6a94a-133">Describes where the paged view starts and the maximum number of items returned in a **FindItem** request.</span></span> <span data-ttu-id="6a94a-134">Se describe el desplazamiento de la vista de página desde el principio del conjunto de elementos encontrados por una fracción.</span><span class="sxs-lookup"><span data-stu-id="6a94a-134">The paged view offset from the beginning of the set of found items is described by a fraction.</span></span> <span data-ttu-id="6a94a-135">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="6a94a-135">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="6a94a-136">CalendarView</span><span class="sxs-lookup"><span data-stu-id="6a94a-136">CalendarView</span></span>](calendarview.md) <br/> |<span data-ttu-id="6a94a-137">Proporciona tiempo abarcar límites para definir una búsqueda de elementos de calendario.</span><span class="sxs-lookup"><span data-stu-id="6a94a-137">Provides time span limits to define a search for calendar items.</span></span> <span data-ttu-id="6a94a-138">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="6a94a-138">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="6a94a-139">ContactsView</span><span class="sxs-lookup"><span data-stu-id="6a94a-139">ContactsView</span></span>](contactsview.md) <br/> |<span data-ttu-id="6a94a-140">Define una búsqueda de elementos de contacto basándose en los nombres para mostrar alfabético.</span><span class="sxs-lookup"><span data-stu-id="6a94a-140">Defines a search for contact items based on alphabetical display names.</span></span> <span data-ttu-id="6a94a-141">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="6a94a-141">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="6a94a-142">GroupBy</span><span class="sxs-lookup"><span data-stu-id="6a94a-142">GroupBy</span></span>](groupby.md) <br/> |<span data-ttu-id="6a94a-143">Especifica los grupos arbitrarios para las consultas de **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="6a94a-143">Specifies arbitrary groupings for **FindItem** queries.</span></span> <span data-ttu-id="6a94a-144">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="6a94a-144">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="6a94a-145">DistinguishedGroupBy</span><span class="sxs-lookup"><span data-stu-id="6a94a-145">DistinguishedGroupBy</span></span>](distinguishedgroupby.md) <br/> |<span data-ttu-id="6a94a-146">Proporciona agrupaciones estándares para las consultas de **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="6a94a-146">Provides standard groupings for **FindItem** queries.</span></span> <span data-ttu-id="6a94a-147">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="6a94a-147">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="6a94a-148">Restriction</span><span class="sxs-lookup"><span data-stu-id="6a94a-148">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="6a94a-149">Define la restricción o la consulta que se usa para filtrar los elementos o carpetas en **FindItem**/ operaciones de carpeta**FindFolder** y búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6a94a-149">Defines the restriction or query that is used to filter items or folders in **FindItem**/ **FindFolder** and search folder operations.</span></span> <span data-ttu-id="6a94a-150">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="6a94a-150">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="6a94a-151">SortOrder</span><span class="sxs-lookup"><span data-stu-id="6a94a-151">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="6a94a-152">Define cómo se ordenan los elementos en una solicitud FindItem.</span><span class="sxs-lookup"><span data-stu-id="6a94a-152">Defines how items are sorted in a FindItem request.</span></span> <span data-ttu-id="6a94a-153">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="6a94a-153">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="6a94a-154">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="6a94a-154">ParentFolderIds</span></span>](parentfolderids.md) <br/> |<span data-ttu-id="6a94a-155">Identifica las carpetas para buscar las operaciones FindItem y FindFolder.</span><span class="sxs-lookup"><span data-stu-id="6a94a-155">Identifies folders to search for the FindItem and FindFolder operations.</span></span>  <br/> |
|[<span data-ttu-id="6a94a-156">QueryString (QueryStringType)</span><span class="sxs-lookup"><span data-stu-id="6a94a-156">QueryString (QueryStringType)</span></span>](querystring-querystringtype.md) <br/> |<span data-ttu-id="6a94a-157">Contiene una cadena de consulta de buzón de correo basada en la sintaxis de consulta avanzada (AQS).</span><span class="sxs-lookup"><span data-stu-id="6a94a-157">Contains a mailbox query string based on Advanced Query Syntax (AQS).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6a94a-158">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6a94a-158">Parent elements</span></span>

<span data-ttu-id="6a94a-159">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6a94a-159">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6a94a-160">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6a94a-160">Remarks</span></span>

<span data-ttu-id="6a94a-161">Solo uno de los [IndexedPageItemView](indexedpageitemview.md), [FractionalPageItemView](fractionalpageitemview.md), [CalendarView](calendarview.md)o elementos de [contactos](contactsview.md) puede incluir en una solicitud **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="6a94a-161">Only one of the [IndexedPageItemView](indexedpageitemview.md), [FractionalPageItemView](fractionalpageitemview.md), [CalendarView](calendarview.md), or [ContactsView](contactsview.md) elements can be included in a **FindItem** request.</span></span> <span data-ttu-id="6a94a-162">Solo uno de los elementos [GroupBy](groupby.md) o [DistinguishedGroupBy](distinguishedgroupby.md) puede incluirse en una solicitud **FindItem** .</span><span class="sxs-lookup"><span data-stu-id="6a94a-162">Only one of the [GroupBy](groupby.md) or [DistinguishedGroupBy](distinguishedgroupby.md) elements can be included in a **FindItem** request.</span></span> 
  
<span data-ttu-id="6a94a-163">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6a94a-163">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6a94a-164">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6a94a-164">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6a94a-165">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6a94a-165">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6a94a-166">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6a94a-166">Schema Name</span></span>  <br/> |<span data-ttu-id="6a94a-167">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="6a94a-167">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6a94a-168">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6a94a-168">Validation File</span></span>  <br/> |<span data-ttu-id="6a94a-169">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6a94a-169">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6a94a-170">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6a94a-170">Can be Empty</span></span>  <br/> |<span data-ttu-id="6a94a-171">False</span><span class="sxs-lookup"><span data-stu-id="6a94a-171">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6a94a-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a94a-172">See also</span></span>

- [<span data-ttu-id="6a94a-173">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="6a94a-173">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="6a94a-174">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="6a94a-174">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

