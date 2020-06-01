---
title: Item (UploadItemType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ab7058f2-615f-4393-a0d4-af76727f37e9
description: El elemento Item representa un solo elemento que se carga en un buzón.
ms.openlocfilehash: 82c0fdf89c06ddfb812c2b2f1899b589eedeb7d8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467553"
---
# <a name="item-uploaditemtype"></a><span data-ttu-id="00bbe-103">Item (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="00bbe-103">Item (UploadItemType)</span></span>

<span data-ttu-id="00bbe-104">El elemento **Item** representa un solo elemento que se carga en un buzón.</span><span class="sxs-lookup"><span data-stu-id="00bbe-104">The **Item** element represents a single item to upload into a mailbox.</span></span> 
  
[<span data-ttu-id="00bbe-105">UploadItems</span><span class="sxs-lookup"><span data-stu-id="00bbe-105">UploadItems</span></span>](uploaditems.md)
  
[<span data-ttu-id="00bbe-106">Elementos (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="00bbe-106">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md)
  
[<span data-ttu-id="00bbe-107">Item (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="00bbe-107">Item (UploadItemType)</span></span>](item-uploaditemtype.md)
  
```XML
<Item CreateAction="" IsAssociated="">
   <ParentFolderId/>
   <ItemId/>
   <Data/>
</Item>
```

 <span data-ttu-id="00bbe-108">**UploadItemType**</span><span class="sxs-lookup"><span data-stu-id="00bbe-108">**UploadItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="00bbe-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="00bbe-109">Attributes and elements</span></span>

<span data-ttu-id="00bbe-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="00bbe-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="00bbe-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="00bbe-111">Attributes</span></span>

|<span data-ttu-id="00bbe-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="00bbe-112">**Attribute**</span></span>|<span data-ttu-id="00bbe-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="00bbe-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00bbe-114">**CreateAction**</span><span class="sxs-lookup"><span data-stu-id="00bbe-114">**CreateAction**</span></span> <br/> |<span data-ttu-id="00bbe-115">Especifica la acción para cargar un elemento en un buzón.</span><span class="sxs-lookup"><span data-stu-id="00bbe-115">Specifies the action for uploading an item into a mailbox.</span></span> <span data-ttu-id="00bbe-116">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="00bbe-116">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="00bbe-117">**IsAssociated**</span><span class="sxs-lookup"><span data-stu-id="00bbe-117">**IsAssociated**</span></span> <br/> |<span data-ttu-id="00bbe-118">Especifica si el elemento cargado es un elemento asociado a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="00bbe-118">Specifies whether the uploaded item is a folder associated item.</span></span> <span data-ttu-id="00bbe-119">Este atributo es un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="00bbe-119">This attribute is a Boolean value.</span></span> <span data-ttu-id="00bbe-120">Un valor de **true** indica que el elemento es un elemento asociado a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="00bbe-120">A value of **true** indicates that the item is a folder associated item.</span></span> <span data-ttu-id="00bbe-121">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="00bbe-121">This attribute is optional.</span></span>  <br/> |
   
#### <a name="createaction-attribute"></a><span data-ttu-id="00bbe-122">Atributo CreateAction</span><span class="sxs-lookup"><span data-stu-id="00bbe-122">CreateAction Attribute</span></span>

|<span data-ttu-id="00bbe-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="00bbe-123">**Value**</span></span>|<span data-ttu-id="00bbe-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="00bbe-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00bbe-125">**CreateNew**</span><span class="sxs-lookup"><span data-stu-id="00bbe-125">**CreateNew**</span></span> <br/> |<span data-ttu-id="00bbe-126">Indica que se ha cargado una nueva copia del elemento original en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="00bbe-126">Indicates that a new copy of the original item is uploaded to the mailbox.</span></span> <span data-ttu-id="00bbe-127">El elemento [Itemid](itemid.md) no debe estar presente si se usa el valor CreateNew.</span><span class="sxs-lookup"><span data-stu-id="00bbe-127">The [ItemId](itemid.md) element must not be present if the CreateNew value is used.</span></span> <span data-ttu-id="00bbe-128">El nuevo identificador de elemento se devuelve en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="00bbe-128">The new item identifier is returned in the response.</span></span>  <br/> |
|<span data-ttu-id="00bbe-129">**Actualización**</span><span class="sxs-lookup"><span data-stu-id="00bbe-129">**Update**</span></span> <br/> |<span data-ttu-id="00bbe-130">Especifica que se actualizará el elemento indicado por el elemento **Itemid** .</span><span class="sxs-lookup"><span data-stu-id="00bbe-130">Specifies that the item indicated by the **ItemId** element will be updated.</span></span> <span data-ttu-id="00bbe-131">Se devuelve un error si el elemento **Itemid** no está presente o si el elemento no existe en la carpeta identificada por el elemento [ParentFolderId](parentfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="00bbe-131">An error is returned if the **ItemId** element is not present or if the item does not exist in the folder identified by the [ParentFolderId](parentfolderid.md) element.</span></span>  <br/> |
|<span data-ttu-id="00bbe-132">**UpdateOrCreate**</span><span class="sxs-lookup"><span data-stu-id="00bbe-132">**UpdateOrCreate**</span></span> <br/> |<span data-ttu-id="00bbe-133">Indica que se ha intentado actualizar el elemento por primera vez.</span><span class="sxs-lookup"><span data-stu-id="00bbe-133">Indicates that an attempt is first made to update the item.</span></span> <span data-ttu-id="00bbe-134">Si el elemento no existe en la carpeta especificada por el elemento **ParentFolderId** , se crea un nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="00bbe-134">If the item does not exist in the folder specified by the **ParentFolderId** element, a new item is created.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="00bbe-135">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="00bbe-135">Child elements</span></span>

|<span data-ttu-id="00bbe-136">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="00bbe-136">**Element**</span></span>|<span data-ttu-id="00bbe-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="00bbe-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="00bbe-138">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="00bbe-138">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="00bbe-139">Representa el identificador de la carpeta principal donde se crea un nuevo elemento o que contiene el elemento que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="00bbe-139">Represents the identifier of the parent folder where a new item is created or that contains the item to update.</span></span>  <br/> |
|[<span data-ttu-id="00bbe-140">ItemId</span><span class="sxs-lookup"><span data-stu-id="00bbe-140">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="00bbe-141">Contiene el identificador único y la clave de cambio de un elemento que se va a crear o actualizar en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="00bbe-141">Contains the unique identifier and change key of an item to create or update in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="00bbe-142">Datos (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="00bbe-142">Data (base64Binary)</span></span>](data-base64binary.md) <br/> |<span data-ttu-id="00bbe-143">Contiene los datos de un elemento único que se va a cargar en un buzón.</span><span class="sxs-lookup"><span data-stu-id="00bbe-143">Contains the data of a single item to upload into a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="00bbe-144">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="00bbe-144">Parent elements</span></span>

|<span data-ttu-id="00bbe-145">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="00bbe-145">**Element**</span></span>|<span data-ttu-id="00bbe-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="00bbe-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="00bbe-147">Elementos (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="00bbe-147">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md) <br/> |<span data-ttu-id="00bbe-148">Contiene una matriz de elementos que se van a cargar en un buzón.</span><span class="sxs-lookup"><span data-stu-id="00bbe-148">Contains an array of item to upload into a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="00bbe-149">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="00bbe-149">Text value</span></span>

<span data-ttu-id="00bbe-150">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="00bbe-150">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00bbe-151">Comentarios</span><span class="sxs-lookup"><span data-stu-id="00bbe-151">Remarks</span></span>

<span data-ttu-id="00bbe-152">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="00bbe-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="00bbe-153">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="00bbe-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00bbe-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="00bbe-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="00bbe-155">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="00bbe-155">Schema Name</span></span>  <br/> |<span data-ttu-id="00bbe-156">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="00bbe-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="00bbe-157">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="00bbe-157">Validation File</span></span>  <br/> |<span data-ttu-id="00bbe-158">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="00bbe-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="00bbe-159">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="00bbe-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="00bbe-160">Falso</span><span class="sxs-lookup"><span data-stu-id="00bbe-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="00bbe-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="00bbe-161">See also</span></span>



[<span data-ttu-id="00bbe-162">Operación ExportItems</span><span class="sxs-lookup"><span data-stu-id="00bbe-162">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="00bbe-163">Operación UploadItems</span><span class="sxs-lookup"><span data-stu-id="00bbe-163">UploadItems operation</span></span>](uploaditems-operation.md)

