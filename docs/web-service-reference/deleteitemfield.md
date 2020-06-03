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
description: El elemento DeleteItemField representa una operación para eliminar una propiedad determinada de un elemento durante una llamada a UpdateItem.
ms.openlocfilehash: e6f5ee8a1130d7c040f3ddd94021eff6d4a758b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455677"
---
# <a name="deleteitemfield"></a><span data-ttu-id="00564-103">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="00564-103">DeleteItemField</span></span>

<span data-ttu-id="00564-104">El elemento **DeleteItemField** representa una operación para eliminar una propiedad determinada de un elemento durante una llamada a UpdateItem.</span><span class="sxs-lookup"><span data-stu-id="00564-104">The **DeleteItemField** element represents an operation to delete a given property from an item during an UpdateItem call.</span></span> 
 
- [<span data-ttu-id="00564-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="00564-105">UpdateItem</span></span>](updateitem.md)  
- [<span data-ttu-id="00564-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="00564-106">ItemChanges</span></span>](itemchanges.md) 
- [<span data-ttu-id="00564-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="00564-107">ItemChange</span></span>](itemchange.md) 
- [<span data-ttu-id="00564-108">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="00564-108">Updates (Item)</span></span>](updates-item.md) 
- [<span data-ttu-id="00564-109">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="00564-109">DeleteItemField</span></span>](deleteitemfield.md)
  
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

<span data-ttu-id="00564-110">**DeleteItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="00564-110">**DeleteItemFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="00564-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="00564-111">Attributes and elements</span></span>

<span data-ttu-id="00564-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="00564-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="00564-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="00564-113">Attributes</span></span>

<span data-ttu-id="00564-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="00564-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="00564-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="00564-115">Child elements</span></span>

|<span data-ttu-id="00564-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="00564-116">**Element**</span></span>|<span data-ttu-id="00564-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="00564-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="00564-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="00564-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="00564-119">Identifica las propiedades a las que se hace referencia con frecuencia mediante el URI.</span><span class="sxs-lookup"><span data-stu-id="00564-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="00564-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="00564-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="00564-121">Identifica los miembros individuales de una propiedad Dictionary.</span><span class="sxs-lookup"><span data-stu-id="00564-121">Identifies individual members of a dictionary property.</span></span>  <br/> |
|[<span data-ttu-id="00564-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="00564-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="00564-123">Identifica las propiedades de MAPI extendida.</span><span class="sxs-lookup"><span data-stu-id="00564-123">Identifies extended MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="00564-124">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="00564-124">Parent elements</span></span>

|<span data-ttu-id="00564-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="00564-125">**Element**</span></span>|<span data-ttu-id="00564-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="00564-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="00564-127">Actualizaciones (elemento)</span><span class="sxs-lookup"><span data-stu-id="00564-127">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="00564-128">Contiene un conjunto de elementos que definen los cambios de anexar, establecer y eliminar en las propiedades del elemento.</span><span class="sxs-lookup"><span data-stu-id="00564-128">Contains a set of elements that define append, set, and delete changes to item properties.</span></span>  <br/><br/><span data-ttu-id="00564-129">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="00564-129">The following is the XPath expression to this element:</span></span><br/>`/UpdateItem/ItemChanges/ItemChange[i]/Updates` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00564-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="00564-130">Remarks</span></span>

<span data-ttu-id="00564-131">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="00564-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="00564-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="00564-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00564-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="00564-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="00564-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="00564-134">Schema Name</span></span>  <br/> |<span data-ttu-id="00564-135">esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="00564-135">types schema</span></span>  <br/> |
|<span data-ttu-id="00564-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="00564-136">Validation File</span></span>  <br/> |<span data-ttu-id="00564-137">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="00564-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="00564-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="00564-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="00564-139">Falso</span><span class="sxs-lookup"><span data-stu-id="00564-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="00564-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="00564-140">See also</span></span>

- [<span data-ttu-id="00564-141">Operación UpdateItem</span><span class="sxs-lookup"><span data-stu-id="00564-141">UpdateItem operation</span></span>](updateitem-operation.md)

