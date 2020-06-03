---
title: Exists
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Exists
api_type:
- schema
ms.assetid: 55d568bd-8dbc-4d50-b9d7-54b74a54d4b5
description: El elemento EXISTS representa una expresión de búsqueda que devuelve true si la propiedad proporcionada existe en un elemento.
ms.openlocfilehash: b5e7a24c5214574ef385cd6ffca87ed5f861c188
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456951"
---
# <a name="exists"></a><span data-ttu-id="d381f-103">Exists</span><span class="sxs-lookup"><span data-stu-id="d381f-103">Exists</span></span>

<span data-ttu-id="d381f-104">El elemento **EXISTS** representa una expresión de búsqueda que devuelve **true** si la propiedad proporcionada existe en un elemento.</span><span class="sxs-lookup"><span data-stu-id="d381f-104">The **Exists** element represents a search expression that returns **true** if the supplied property exists on an item.</span></span> 
  
```xml
<Exists>
   <Path/>
</Exists>
```

 <span data-ttu-id="d381f-105">**ExistsType**</span><span class="sxs-lookup"><span data-stu-id="d381f-105">**ExistsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d381f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d381f-106">Attributes and elements</span></span>

<span data-ttu-id="d381f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d381f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d381f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d381f-108">Attributes</span></span>

<span data-ttu-id="d381f-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d381f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d381f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d381f-110">Child elements</span></span>

|<span data-ttu-id="d381f-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d381f-111">**Element**</span></span>|<span data-ttu-id="d381f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d381f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d381f-113">FieldURI</span><span class="sxs-lookup"><span data-stu-id="d381f-113">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="d381f-114">Identifica las propiedades a las que se hace referencia con frecuencia mediante el URI.</span><span class="sxs-lookup"><span data-stu-id="d381f-114">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="d381f-115">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="d381f-115">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="d381f-116">Identifica a los miembros individuales de un diccionario.</span><span class="sxs-lookup"><span data-stu-id="d381f-116">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="d381f-117">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="d381f-117">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="d381f-118">Identifica las propiedades MAPI.</span><span class="sxs-lookup"><span data-stu-id="d381f-118">Identifies MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d381f-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d381f-119">Parent elements</span></span>

|<span data-ttu-id="d381f-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d381f-120">**Element**</span></span>|<span data-ttu-id="d381f-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d381f-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d381f-122">Restriction</span><span class="sxs-lookup"><span data-stu-id="d381f-122">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="d381f-123">Representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones de carpeta de búsqueda FindItem/FindFolder.</span><span class="sxs-lookup"><span data-stu-id="d381f-123">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="d381f-124">Not</span><span class="sxs-lookup"><span data-stu-id="d381f-124">Not</span></span>](not.md) <br/> |<span data-ttu-id="d381f-125">Representa una expresión de búsqueda que niega el valor booleano de la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="d381f-125">Represents a search expression that negates the Boolean value of the search expression that it contains.</span></span>  <br/> |
|[<span data-ttu-id="d381f-126">And</span><span class="sxs-lookup"><span data-stu-id="d381f-126">And</span></span>](and.md) <br/> |<span data-ttu-id="d381f-127">Representa una expresión de búsqueda que permite realizar una operación and booleana entre dos o más expresiones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d381f-127">Represents a search expression that enables you to perform a Boolean And operation between two or more search expressions.</span></span> <span data-ttu-id="d381f-128">El resultado de la operación and es **true** si todas las expresiones de búsqueda incluidas en el y son **true**.</span><span class="sxs-lookup"><span data-stu-id="d381f-128">The result of the And operation is **true** if all the search expressions contained within the And are **true**.</span></span>  <br/> |
|[<span data-ttu-id="d381f-129">Or</span><span class="sxs-lookup"><span data-stu-id="d381f-129">Or</span></span>](or.md) <br/> |<span data-ttu-id="d381f-130">Representa una expresión de búsqueda que realiza una operación lógica OR en la expresión de búsqueda que contiene.</span><span class="sxs-lookup"><span data-stu-id="d381f-130">Represents a search expression that performs a logical OR on the search expression that it contains.</span></span> <span data-ttu-id="d381f-131">[O](or.md) devuelve **true** si cualquiera de sus elementos secundarios devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="d381f-131">[Or](or.md) will return **true** if any of its children return **true**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d381f-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d381f-132">Remarks</span></span>

<span data-ttu-id="d381f-133">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="d381f-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d381f-134">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d381f-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d381f-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="d381f-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d381f-136">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d381f-136">Schema Name</span></span>  <br/> |<span data-ttu-id="d381f-137">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d381f-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="d381f-138">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d381f-138">Validation File</span></span>  <br/> |<span data-ttu-id="d381f-139">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d381f-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d381f-140">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d381f-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="d381f-141">Falso</span><span class="sxs-lookup"><span data-stu-id="d381f-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d381f-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="d381f-142">See also</span></span>



- [<span data-ttu-id="d381f-143">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d381f-143">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

