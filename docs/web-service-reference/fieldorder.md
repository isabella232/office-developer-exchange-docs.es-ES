---
title: FieldOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FieldOrder
api_type:
- schema
ms.assetid: b9364842-bbe2-4221-afef-bf5022bc89ec
description: El elemento FieldOrder representa un solo campo por el que se va a ordenar los resultados e indica la dirección para la ordenación.
ms.openlocfilehash: 320a7b821cc593e7dd60a8f8adb23bcd600f71f8
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353304"
---
# <a name="fieldorder"></a><span data-ttu-id="b777a-103">FieldOrder</span><span class="sxs-lookup"><span data-stu-id="b777a-103">FieldOrder</span></span>

<span data-ttu-id="b777a-104">El elemento **FieldOrder** representa un solo campo por el que se va a ordenar los resultados e indica la dirección para la ordenación.</span><span class="sxs-lookup"><span data-stu-id="b777a-104">The **FieldOrder** element represents a single field by which to sort results and indicates the direction for the sort.</span></span> 
  
```xml
<FieldOrder Order="">
   <FieldURI/>
</FieldOrder>
```

```xml
<FieldOrder Order="">
   <ExtendedFieldURI/> 
</FieldOrder>
```

```xml
<FieldOrder Order="">
   <IndexedFieldURI/>
</FieldOrder>
```

<span data-ttu-id="b777a-105">**FieldOrderType**</span><span class="sxs-lookup"><span data-stu-id="b777a-105">**FieldOrderType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b777a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b777a-106">Attributes and elements</span></span>

<span data-ttu-id="b777a-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b777a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b777a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b777a-108">Attributes</span></span>

|<span data-ttu-id="b777a-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="b777a-109">**Attribute**</span></span>|<span data-ttu-id="b777a-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b777a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b777a-111">**Order**</span><span class="sxs-lookup"><span data-stu-id="b777a-111">**Order**</span></span> <br/> | <span data-ttu-id="b777a-112">Describe la dirección del criterio de ordenación.</span><span class="sxs-lookup"><span data-stu-id="b777a-112">Describes the sort order direction.</span></span><br/><br/> <span data-ttu-id="b777a-113">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="b777a-113">The following are the possible values:</span></span> <br/> <br/><span data-ttu-id="b777a-114">-Ascendente</span><span class="sxs-lookup"><span data-stu-id="b777a-114">-  Ascending</span></span>  <br/><span data-ttu-id="b777a-115">-Descendente</span><span class="sxs-lookup"><span data-stu-id="b777a-115">-  Descending</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b777a-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b777a-116">Child elements</span></span>

|<span data-ttu-id="b777a-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="b777a-117">**Element**</span></span>|<span data-ttu-id="b777a-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b777a-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b777a-119">FieldURI</span><span class="sxs-lookup"><span data-stu-id="b777a-119">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="b777a-120">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="b777a-120">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="b777a-121">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="b777a-121">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="b777a-122">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="b777a-122">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="b777a-123">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="b777a-123">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="b777a-124">Identifica las propiedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="b777a-124">Identifies MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b777a-125">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b777a-125">Parent elements</span></span>

|<span data-ttu-id="b777a-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="b777a-126">**Element**</span></span>|<span data-ttu-id="b777a-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b777a-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b777a-128">SortOrder</span><span class="sxs-lookup"><span data-stu-id="b777a-128">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="b777a-129">Define cómo se ordenan los elementos en una solicitud FindItem.</span><span class="sxs-lookup"><span data-stu-id="b777a-129">Defines how items are sorted in a FindItem request.</span></span>  <br/> <span data-ttu-id="b777a-130">La siguiente es la expresión de XPath para este elemento:`/FindItem/SortOrder`</span><span class="sxs-lookup"><span data-stu-id="b777a-130">The following is the XPath expression to this element:  `/FindItem/SortOrder`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b777a-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b777a-131">Remarks</span></span>

<span data-ttu-id="b777a-132">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="b777a-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b777a-133">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b777a-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b777a-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b777a-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b777a-135">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b777a-135">Schema Name</span></span>  <br/> |<span data-ttu-id="b777a-136">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b777a-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="b777a-137">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b777a-137">Validation File</span></span>  <br/> |<span data-ttu-id="b777a-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b777a-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b777a-139">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b777a-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="b777a-140">False</span><span class="sxs-lookup"><span data-stu-id="b777a-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b777a-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="b777a-141">See also</span></span>

- [<span data-ttu-id="b777a-142">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b777a-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

