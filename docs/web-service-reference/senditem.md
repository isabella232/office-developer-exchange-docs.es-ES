---
title: SendItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendItem
api_type:
- schema
ms.assetid: a966da19-b05a-4504-ac98-91acc1667b9a
description: El elemento de SendItem es el elemento raíz en una solicitud para enviar un elemento en el almacén de Exchange.
ms.openlocfilehash: c5ce52ee4643219aa31ae59e8b7d40d7a904c8ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837340"
---
# <a name="senditem"></a><span data-ttu-id="864ed-103">SendItem</span><span class="sxs-lookup"><span data-stu-id="864ed-103">SendItem</span></span>

<span data-ttu-id="864ed-104">El elemento de **SendItem** es el elemento raíz en una solicitud para enviar un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="864ed-104">The **SendItem** element is the root element in a request to send an item in the Exchange store.</span></span> 
  
```xml
<SendItem SaveItemToFolder="">
   <ItemIds/>
   <SavedItemFolderId/>
</SendItem>
```

 <span data-ttu-id="864ed-105">**SendItemType**</span><span class="sxs-lookup"><span data-stu-id="864ed-105">**SendItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="864ed-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="864ed-106">Attributes and elements</span></span>

<span data-ttu-id="864ed-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="864ed-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="864ed-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="864ed-108">Attributes</span></span>

|<span data-ttu-id="864ed-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="864ed-109">**Attribute**</span></span>|<span data-ttu-id="864ed-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="864ed-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="864ed-111">**SaveItemToFolder**</span><span class="sxs-lookup"><span data-stu-id="864ed-111">**SaveItemToFolder**</span></span> <br/> |<span data-ttu-id="864ed-112">Identifica si se guarda una copia del elemento enviado.</span><span class="sxs-lookup"><span data-stu-id="864ed-112">Identifies whether a copy of the sent item is saved.</span></span> <span data-ttu-id="864ed-113">La operación de guardar acción depende del valor de **SaveItemToFolder** y si está presente en la solicitud de un elemento [SavedItemFolderId](saveditemfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="864ed-113">The save action depends on the value of **SaveItemToFolder** and whether a [SavedItemFolderId](saveditemfolderid.md) element is present in the request.</span></span> <span data-ttu-id="864ed-114">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="864ed-114">This element is required.</span></span>  <br/> |
   
#### <a name="saveitemtofolder-attribute"></a><span data-ttu-id="864ed-115">Atributo SaveItemToFolder</span><span class="sxs-lookup"><span data-stu-id="864ed-115">SaveItemToFolder Attribute</span></span>

|<span data-ttu-id="864ed-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="864ed-116">**Value**</span></span>|<span data-ttu-id="864ed-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="864ed-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="864ed-118">**True**</span><span class="sxs-lookup"><span data-stu-id="864ed-118">**true**</span></span> <br/> |<span data-ttu-id="864ed-119">Si el elemento [SavedItemFolderId](saveditemfolderid.md) no está presente, el elemento se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="864ed-119">If the [SavedItemFolderId](saveditemfolderid.md) element is not present, the item is saved in the Sent Items folder.</span></span> <span data-ttu-id="864ed-120">Si el elemento [SavedItemFolderId](saveditemfolderid.md) está presente, el elemento se guarda en la carpeta que se especifica mediante el elemento [SavedItemFolderId](saveditemfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="864ed-120">If the [SavedItemFolderId](saveditemfolderid.md) element is present, the item is saved in the folder that is specified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
|<span data-ttu-id="864ed-121">**False**</span><span class="sxs-lookup"><span data-stu-id="864ed-121">**false**</span></span> <br/> |<span data-ttu-id="864ed-122">Si el elemento [SavedItemFolderId](saveditemfolderid.md) no está presente, no se guarda el elemento.</span><span class="sxs-lookup"><span data-stu-id="864ed-122">If the [SavedItemFolderId](saveditemfolderid.md) element is not present, the item is not saved.</span></span> <span data-ttu-id="864ed-123">Si el elemento [SavedItemFolderId](saveditemfolderid.md) está presente, se devolverá una respuesta de error con un elemento [ResponseCode](responsecode.md) que contiene el valor de **ErrorInvalidSendItemSaveSettings** .</span><span class="sxs-lookup"><span data-stu-id="864ed-123">If the [SavedItemFolderId](saveditemfolderid.md) element is present, an error response will be returned with a [ResponseCode](responsecode.md) element that contains the **ErrorInvalidSendItemSaveSettings** value.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="864ed-124">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="864ed-124">Child elements</span></span>

|<span data-ttu-id="864ed-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="864ed-125">**Element**</span></span>|<span data-ttu-id="864ed-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="864ed-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="864ed-127">ItemId</span><span class="sxs-lookup"><span data-stu-id="864ed-127">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="864ed-128">Contiene las identidades únicas de los elementos, elementos de aparición y elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="864ed-128">Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="864ed-129">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="864ed-129">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> |<span data-ttu-id="864ed-130">Identifica la carpeta de destino para las operaciones que actualizar, enviar y crear elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="864ed-130">Identifies the target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="864ed-131">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="864ed-131">Parent elements</span></span>

<span data-ttu-id="864ed-132">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="864ed-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="864ed-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="864ed-133">Remarks</span></span>

<span data-ttu-id="864ed-134">Si se envía un elemento en la carpeta Elementos enviados, se elimina el elemento enviado y se coloca una copia de él en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="864ed-134">If an item in the Sent Items folder is sent, the sent item is deleted and a copy of it is put in the Sent Items folder.</span></span>
  
<span data-ttu-id="864ed-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="864ed-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="864ed-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="864ed-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="864ed-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="864ed-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="864ed-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="864ed-138">Schema Name</span></span>  <br/> |<span data-ttu-id="864ed-139">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="864ed-139">Messages schema</span></span>  <br/> |
|<span data-ttu-id="864ed-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="864ed-140">Validation File</span></span>  <br/> |<span data-ttu-id="864ed-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="864ed-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="864ed-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="864ed-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="864ed-143">False</span><span class="sxs-lookup"><span data-stu-id="864ed-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="864ed-144">Ver también</span><span class="sxs-lookup"><span data-stu-id="864ed-144">See also</span></span>



[<span data-ttu-id="864ed-145">Operación SendItem</span><span class="sxs-lookup"><span data-stu-id="864ed-145">SendItem operation</span></span>](senditem-operation.md)

