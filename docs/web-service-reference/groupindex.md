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
description: El elemento GroupIndex representa el valor de propiedad que se usa para agrupar elementos para el grupo actual de elementos en una llamada de operación FindItem.
ms.openlocfilehash: 05f303be92885a15dddf85c85251af04910d835c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530271"
---
# <a name="groupindex"></a><span data-ttu-id="31094-103">GroupIndex</span><span class="sxs-lookup"><span data-stu-id="31094-103">GroupIndex</span></span>

<span data-ttu-id="31094-104">El elemento **GroupIndex** representa el valor de propiedad que se usa para agrupar elementos para el grupo actual de elementos en una llamada de [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="31094-104">The **GroupIndex** element represents the property value that is used to group items for the current group of items in a [FindItem operation](finditem-operation.md) call.</span></span> 
  
[<span data-ttu-id="31094-105">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="31094-105">FindItemResponse</span></span>](finditemresponse.md)
  
[<span data-ttu-id="31094-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="31094-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="31094-107">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="31094-107">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
  
[<span data-ttu-id="31094-108">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="31094-108">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
  
[<span data-ttu-id="31094-109">Grupos</span><span class="sxs-lookup"><span data-stu-id="31094-109">Groups</span></span>](groups.md)
  
[<span data-ttu-id="31094-110">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="31094-110">GroupedItems</span></span>](groupeditems.md)
  
[<span data-ttu-id="31094-111">GroupIndex</span><span class="sxs-lookup"><span data-stu-id="31094-111">GroupIndex</span></span>](groupindex.md)
  
```xml
<GroupIndex/>
```

 <span data-ttu-id="31094-112">**string**</span><span class="sxs-lookup"><span data-stu-id="31094-112">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="31094-113">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="31094-113">Attributes and elements</span></span>

<span data-ttu-id="31094-114">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="31094-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31094-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="31094-115">Attributes</span></span>

<span data-ttu-id="31094-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="31094-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="31094-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="31094-117">Child elements</span></span>

<span data-ttu-id="31094-118">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="31094-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="31094-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="31094-119">Parent elements</span></span>

|<span data-ttu-id="31094-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="31094-120">**Element**</span></span>|<span data-ttu-id="31094-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="31094-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31094-122">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="31094-122">GroupedItems</span></span>](groupeditems.md) <br/> |<span data-ttu-id="31094-123">Representa una colección de elementos que son el resultado de una llamada de [operación FindItem](finditem-operation.md) agrupada.</span><span class="sxs-lookup"><span data-stu-id="31094-123">Represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> <span data-ttu-id="31094-124">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="31094-124">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItemResponse/ResponseMessages/FindItemResponseMessage/RootFolder/Groups/GroupedItems[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="31094-125">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="31094-125">Text value</span></span>

<span data-ttu-id="31094-126">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="31094-126">A text value is required.</span></span> <span data-ttu-id="31094-127">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="31094-127">This property is read-only.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31094-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31094-128">Remarks</span></span>

<span data-ttu-id="31094-129">Este elemento solo se produce en una respuesta de la [operación FindItem](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="31094-129">This element only occurs in a [FindItem operation](finditem-operation.md) response.</span></span> 
  
<span data-ttu-id="31094-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="31094-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31094-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="31094-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31094-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="31094-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="31094-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="31094-133">Schema name</span></span>  <br/> |<span data-ttu-id="31094-134">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="31094-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="31094-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="31094-135">Validation file</span></span>  <br/> |<span data-ttu-id="31094-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="31094-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="31094-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="31094-137">Can be empty</span></span>  <br/> |<span data-ttu-id="31094-138">Falso</span><span class="sxs-lookup"><span data-stu-id="31094-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31094-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="31094-139">See also</span></span>



[<span data-ttu-id="31094-140">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="31094-140">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="31094-141">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="31094-141">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

