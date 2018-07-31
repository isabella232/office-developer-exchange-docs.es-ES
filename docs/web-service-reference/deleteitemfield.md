---
title: DeleteItemField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItemField
api_type:
- schema
ms.assetid: 3893be6a-49a7-49f6-bf53-c7f819ec3f87
description: El elemento DeleteItemField representa una operación para eliminar una propiedad determinada de un elemento durante una llamada UpdateItem.
ms.openlocfilehash: 571227eece8f717c1bf5da27cfab8ae50dfe3572
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353885"
---
# <a name="deleteitemfield"></a><span data-ttu-id="f655c-103">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="f655c-103">DeleteItemField</span></span>

<span data-ttu-id="f655c-104">El elemento **DeleteItemField** representa una operación para eliminar una propiedad determinada de un elemento durante una llamada UpdateItem.</span><span class="sxs-lookup"><span data-stu-id="f655c-104">The **DeleteItemField** element represents an operation to delete a given property from an item during an UpdateItem call.</span></span> 
 
- [<span data-ttu-id="f655c-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="f655c-105">UpdateItem</span></span>](updateitem.md)  
- [<span data-ttu-id="f655c-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="f655c-106">ItemChanges</span></span>](itemchanges.md) 
- [<span data-ttu-id="f655c-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="f655c-107">ItemChange</span></span>](itemchange.md) 
- [<span data-ttu-id="f655c-108">Updates (Elemento)</span><span class="sxs-lookup"><span data-stu-id="f655c-108">Updates (Item)</span></span>](updates-item.md) 
- [<span data-ttu-id="f655c-109">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="f655c-109">DeleteItemField</span></span>](deleteitemfield.md)
  
```xml
<DeleteItemField>
   <FieldURI/>
</DeleteItemField>
```

```xml
<DeleteItemField>
   <IndexedFieldURI/> 
</DeleteItemField>
```

```xml
<DeleteItemField>
   <ExtendedFieldURI/>
</DeleteItemField>
```

<span data-ttu-id="f655c-110">**DeleteItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="f655c-110">**DeleteItemFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f655c-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f655c-111">Attributes and elements</span></span>

<span data-ttu-id="f655c-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f655c-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f655c-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="f655c-113">Attributes</span></span>

<span data-ttu-id="f655c-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f655c-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f655c-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f655c-115">Child elements</span></span>

|<span data-ttu-id="f655c-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f655c-116">**Element**</span></span>|<span data-ttu-id="f655c-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f655c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f655c-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="f655c-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="f655c-119">Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="f655c-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="f655c-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="f655c-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="f655c-121">Identifica a los miembros individuales de una propiedad de diccionario.</span><span class="sxs-lookup"><span data-stu-id="f655c-121">Identifies individual members of a dictionary property.</span></span>  <br/> |
|[<span data-ttu-id="f655c-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="f655c-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="f655c-123">Identifica las propiedades extendidas de MAPI.</span><span class="sxs-lookup"><span data-stu-id="f655c-123">Identifies extended MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f655c-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f655c-124">Parent elements</span></span>

|<span data-ttu-id="f655c-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="f655c-125">**Element**</span></span>|<span data-ttu-id="f655c-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f655c-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f655c-127">Updates (Elemento)</span><span class="sxs-lookup"><span data-stu-id="f655c-127">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="f655c-128">Contiene un conjunto de elementos que definen append, establecer y eliminar los cambios realizados en las propiedades de elementos.</span><span class="sxs-lookup"><span data-stu-id="f655c-128">Contains a set of elements that define append, set, and delete changes to item properties.</span></span>  <br/><br/><span data-ttu-id="f655c-129">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="f655c-129">The following is the XPath expression to this element:</span></span><br/>`/UpdateItem/ItemChanges/ItemChange[i]/Updates` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f655c-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f655c-130">Remarks</span></span>

<span data-ttu-id="f655c-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="f655c-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f655c-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f655c-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f655c-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f655c-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f655c-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f655c-134">Schema Name</span></span>  <br/> |<span data-ttu-id="f655c-135">esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f655c-135">types schema</span></span>  <br/> |
|<span data-ttu-id="f655c-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f655c-136">Validation File</span></span>  <br/> |<span data-ttu-id="f655c-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f655c-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f655c-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f655c-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="f655c-139">False</span><span class="sxs-lookup"><span data-stu-id="f655c-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f655c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="f655c-140">See also</span></span>

- [<span data-ttu-id="f655c-141">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="f655c-141">UpdateItem operation</span></span>](updateitem-operation.md)

