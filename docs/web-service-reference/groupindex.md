---
title: GroupIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupIndex
api_type:
- schema
ms.assetid: 7a596ff7-6cc3-4626-a52c-538a92202337
description: El elemento GroupIndex representa el valor de la propiedad que se usa para agrupar los elementos para el grupo actual de elementos de una llamada a una operación FindItem.
ms.openlocfilehash: 8b23f5142a15c099c30209ea48cd04f4af4e8c6a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835762"
---
# <a name="groupindex"></a><span data-ttu-id="24449-103">GroupIndex</span><span class="sxs-lookup"><span data-stu-id="24449-103">GroupIndex</span></span>

<span data-ttu-id="24449-104">El elemento **GroupIndex** representa el valor de la propiedad que se usa para agrupar los elementos para el grupo actual de elementos de una llamada a una [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="24449-104">The **GroupIndex** element represents the property value that is used to group items for the current group of items in a [FindItem operation](finditem-operation.md) call.</span></span> 
  
[<span data-ttu-id="24449-105">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="24449-105">FindItemResponse</span></span>](finditemresponse.md)
  
[<span data-ttu-id="24449-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="24449-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="24449-107">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="24449-107">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
  
[<span data-ttu-id="24449-108">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="24449-108">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
  
[<span data-ttu-id="24449-109">Grupos</span><span class="sxs-lookup"><span data-stu-id="24449-109">Groups</span></span>](groups.md)
  
[<span data-ttu-id="24449-110">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="24449-110">GroupedItems</span></span>](groupeditems.md)
  
[<span data-ttu-id="24449-111">GroupIndex</span><span class="sxs-lookup"><span data-stu-id="24449-111">GroupIndex</span></span>](groupindex.md)
  
```xml
<GroupIndex/>
```

 <span data-ttu-id="24449-112">**string**</span><span class="sxs-lookup"><span data-stu-id="24449-112">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="24449-113">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="24449-113">Attributes and elements</span></span>

<span data-ttu-id="24449-114">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="24449-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="24449-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="24449-115">Attributes</span></span>

<span data-ttu-id="24449-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="24449-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="24449-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="24449-117">Child elements</span></span>

<span data-ttu-id="24449-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="24449-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="24449-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="24449-119">Parent elements</span></span>

|<span data-ttu-id="24449-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="24449-120">**Element**</span></span>|<span data-ttu-id="24449-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="24449-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="24449-122">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="24449-122">GroupedItems</span></span>](groupeditems.md) <br/> |<span data-ttu-id="24449-123">Representa una colección de elementos que son el resultado de una [operación FindItem](finditem-operation.md) de agrupada de llamadas.</span><span class="sxs-lookup"><span data-stu-id="24449-123">Represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> <span data-ttu-id="24449-124">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="24449-124">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItemResponse/ResponseMessages/FindItemResponseMessage/RootFolder/Groups/GroupedItems[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="24449-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="24449-125">Text value</span></span>

<span data-ttu-id="24449-126">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="24449-126">A text value is required.</span></span> <span data-ttu-id="24449-127">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="24449-127">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="24449-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="24449-128">Remarks</span></span>

<span data-ttu-id="24449-129">Este elemento sólo se produce en una respuesta de [la operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="24449-129">This element only occurs in a [FindItem operation](finditem-operation.md) response.</span></span> 
  
<span data-ttu-id="24449-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="24449-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="24449-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="24449-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24449-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="24449-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="24449-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="24449-133">Schema name</span></span>  <br/> |<span data-ttu-id="24449-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="24449-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="24449-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="24449-135">Validation file</span></span>  <br/> |<span data-ttu-id="24449-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="24449-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="24449-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="24449-137">Can be empty</span></span>  <br/> |<span data-ttu-id="24449-138">False</span><span class="sxs-lookup"><span data-stu-id="24449-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24449-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="24449-139">See also</span></span>



[<span data-ttu-id="24449-140">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="24449-140">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="24449-141">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="24449-141">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

