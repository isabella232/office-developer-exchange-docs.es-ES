---
title: Elemento (UploadItemType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ab7058f2-615f-4393-a0d4-af76727f37e9
description: El elemento representa un solo elemento va a cargar en un buzón de correo.
ms.openlocfilehash: 8fecef9a2368a44e38633eb9fddaa8197620f6a1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836138"
---
# <a name="item-uploaditemtype"></a><span data-ttu-id="40939-103">Elemento (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="40939-103">Item (UploadItemType)</span></span>

<span data-ttu-id="40939-104">**El elemento** representa un solo elemento va a cargar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="40939-104">The **Item** element represents a single item to upload into a mailbox.</span></span> 
  
[<span data-ttu-id="40939-105">UploadItems</span><span class="sxs-lookup"><span data-stu-id="40939-105">UploadItems</span></span>](uploaditems.md)
  
[<span data-ttu-id="40939-106">Elementos (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="40939-106">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md)
  
[<span data-ttu-id="40939-107">Elemento (UploadItemType)</span><span class="sxs-lookup"><span data-stu-id="40939-107">Item (UploadItemType)</span></span>](item-uploaditemtype.md)
  
```XML
<Item CreateAction="" IsAssociated="">
   <ParentFolderId/>
   <ItemId/>
   <Data/>
</Item>
```

 <span data-ttu-id="40939-108">**UploadItemType**</span><span class="sxs-lookup"><span data-stu-id="40939-108">**UploadItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="40939-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="40939-109">Attributes and elements</span></span>

<span data-ttu-id="40939-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="40939-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="40939-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="40939-111">Attributes</span></span>

|<span data-ttu-id="40939-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="40939-112">**Attribute**</span></span>|<span data-ttu-id="40939-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40939-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="40939-114">**CreateAction**</span><span class="sxs-lookup"><span data-stu-id="40939-114">**CreateAction**</span></span> <br/> |<span data-ttu-id="40939-115">Especifica la acción para cargar un elemento en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="40939-115">Specifies the action for uploading an item into a mailbox.</span></span> <span data-ttu-id="40939-116">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="40939-116">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="40939-117">**IsAssociated**</span><span class="sxs-lookup"><span data-stu-id="40939-117">**IsAssociated**</span></span> <br/> |<span data-ttu-id="40939-118">Especifica si el elemento que se cargan es un elemento de la carpeta asociada.</span><span class="sxs-lookup"><span data-stu-id="40939-118">Specifies whether the uploaded item is a folder associated item.</span></span> <span data-ttu-id="40939-119">Este atributo es un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="40939-119">This attribute is a Boolean value.</span></span> <span data-ttu-id="40939-120">Un valor de **true** indica que el elemento es una carpeta asociada de elemento.</span><span class="sxs-lookup"><span data-stu-id="40939-120">A value of **true** indicates that the item is a folder associated item.</span></span> <span data-ttu-id="40939-121">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="40939-121">This attribute is optional.</span></span>  <br/> |
   
#### <a name="createaction-attribute"></a><span data-ttu-id="40939-122">Atributo CreateAction</span><span class="sxs-lookup"><span data-stu-id="40939-122">CreateAction Attribute</span></span>

|<span data-ttu-id="40939-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="40939-123">**Value**</span></span>|<span data-ttu-id="40939-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40939-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="40939-125">**CreateNew**</span><span class="sxs-lookup"><span data-stu-id="40939-125">**CreateNew**</span></span> <br/> |<span data-ttu-id="40939-126">Indica que se ha cargado una nueva copia del elemento original en el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="40939-126">Indicates that a new copy of the original item is uploaded to the mailbox.</span></span> <span data-ttu-id="40939-127">El elemento de [ItemId](itemid.md) no debe estar presente si se usa el valor CreateNew.</span><span class="sxs-lookup"><span data-stu-id="40939-127">The [ItemId](itemid.md) element must not be present if the CreateNew value is used.</span></span> <span data-ttu-id="40939-128">Se devuelve el identificador del elemento nuevo en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="40939-128">The new item identifier is returned in the response.</span></span>  <br/> |
|<span data-ttu-id="40939-129">**Actualizar**</span><span class="sxs-lookup"><span data-stu-id="40939-129">**Update**</span></span> <br/> |<span data-ttu-id="40939-130">Especifica que se actualizará el elemento indicado por el elemento **ItemId** .</span><span class="sxs-lookup"><span data-stu-id="40939-130">Specifies that the item indicated by the **ItemId** element will be updated.</span></span> <span data-ttu-id="40939-131">Se devuelve un error si el elemento de **ItemId** no está presente o si el elemento no existe en la carpeta identificada por el elemento [ID](parentfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="40939-131">An error is returned if the **ItemId** element is not present or if the item does not exist in the folder identified by the [ParentFolderId](parentfolderid.md) element.</span></span>  <br/> |
|<span data-ttu-id="40939-132">**UpdateOrCreate**</span><span class="sxs-lookup"><span data-stu-id="40939-132">**UpdateOrCreate**</span></span> <br/> |<span data-ttu-id="40939-133">Indica que se realiza en primer lugar un intento para actualizar el elemento.</span><span class="sxs-lookup"><span data-stu-id="40939-133">Indicates that an attempt is first made to update the item.</span></span> <span data-ttu-id="40939-134">Si el elemento no existe en la carpeta especificada por el elemento **ID** , se crea un nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="40939-134">If the item does not exist in the folder specified by the **ParentFolderId** element, a new item is created.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="40939-135">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="40939-135">Child elements</span></span>

|<span data-ttu-id="40939-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="40939-136">**Element**</span></span>|<span data-ttu-id="40939-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40939-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40939-138">Id</span><span class="sxs-lookup"><span data-stu-id="40939-138">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="40939-139">Representa el identificador de la carpeta principal donde se crea un nuevo elemento o que contiene el elemento que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="40939-139">Represents the identifier of the parent folder where a new item is created or that contains the item to update.</span></span>  <br/> |
|[<span data-ttu-id="40939-140">ItemId</span><span class="sxs-lookup"><span data-stu-id="40939-140">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="40939-141">Contiene el único identificador y cambiar la clave de un elemento para crear o actualizar en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="40939-141">Contains the unique identifier and change key of an item to create or update in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="40939-142">Datos (base64Binary)</span><span class="sxs-lookup"><span data-stu-id="40939-142">Data (base64Binary)</span></span>](data-base64binary.md) <br/> |<span data-ttu-id="40939-143">Contiene los datos de un solo elemento va a cargar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="40939-143">Contains the data of a single item to upload into a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="40939-144">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="40939-144">Parent elements</span></span>

|<span data-ttu-id="40939-145">**Element**</span><span class="sxs-lookup"><span data-stu-id="40939-145">**Element**</span></span>|<span data-ttu-id="40939-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="40939-146">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40939-147">Elementos (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="40939-147">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md) <br/> |<span data-ttu-id="40939-148">Contiene una matriz de elemento que se va a cargar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="40939-148">Contains an array of item to upload into a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="40939-149">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="40939-149">Text value</span></span>

<span data-ttu-id="40939-150">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="40939-150">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="40939-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40939-151">Remarks</span></span>

<span data-ttu-id="40939-152">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="40939-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="40939-153">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="40939-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40939-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="40939-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="40939-155">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="40939-155">Schema Name</span></span>  <br/> |<span data-ttu-id="40939-156">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="40939-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="40939-157">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="40939-157">Validation File</span></span>  <br/> |<span data-ttu-id="40939-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="40939-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="40939-159">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="40939-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="40939-160">False</span><span class="sxs-lookup"><span data-stu-id="40939-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40939-161">Ver también</span><span class="sxs-lookup"><span data-stu-id="40939-161">See also</span></span>



[<span data-ttu-id="40939-162">Operación ExportItems</span><span class="sxs-lookup"><span data-stu-id="40939-162">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="40939-163">Operación UploadItems</span><span class="sxs-lookup"><span data-stu-id="40939-163">UploadItems operation</span></span>](uploaditems-operation.md)

