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
description: El elemento SendItem es el elemento raíz de una solicitud para enviar un elemento en el almacén de Exchange.
ms.openlocfilehash: 28f0d484dd079146c998cb7317bd2d80c6739e19
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530568"
---
# <a name="senditem"></a><span data-ttu-id="6961b-103">SendItem</span><span class="sxs-lookup"><span data-stu-id="6961b-103">SendItem</span></span>

<span data-ttu-id="6961b-104">El elemento **SendItem** es el elemento raíz de una solicitud para enviar un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6961b-104">The **SendItem** element is the root element in a request to send an item in the Exchange store.</span></span> 
  
```xml
<SendItem SaveItemToFolder="">
   <ItemIds/>
   <SavedItemFolderId/>
</SendItem>
```

 <span data-ttu-id="6961b-105">**SendItemType**</span><span class="sxs-lookup"><span data-stu-id="6961b-105">**SendItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6961b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6961b-106">Attributes and elements</span></span>

<span data-ttu-id="6961b-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6961b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6961b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6961b-108">Attributes</span></span>

|<span data-ttu-id="6961b-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="6961b-109">**Attribute**</span></span>|<span data-ttu-id="6961b-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6961b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6961b-111">**SaveItemToFolder**</span><span class="sxs-lookup"><span data-stu-id="6961b-111">**SaveItemToFolder**</span></span> <br/> |<span data-ttu-id="6961b-112">Identifica si se guarda una copia del elemento enviado.</span><span class="sxs-lookup"><span data-stu-id="6961b-112">Identifies whether a copy of the sent item is saved.</span></span> <span data-ttu-id="6961b-113">La acción guardar depende del valor de **SaveItemToFolder** y de si un elemento [SavedItemFolderId](saveditemfolderid.md) está presente en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6961b-113">The save action depends on the value of **SaveItemToFolder** and whether a [SavedItemFolderId](saveditemfolderid.md) element is present in the request.</span></span> <span data-ttu-id="6961b-114">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="6961b-114">This element is required.</span></span>  <br/> |
   
#### <a name="saveitemtofolder-attribute"></a><span data-ttu-id="6961b-115">Atributo SaveItemToFolder</span><span class="sxs-lookup"><span data-stu-id="6961b-115">SaveItemToFolder Attribute</span></span>

|<span data-ttu-id="6961b-116">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6961b-116">**Value**</span></span>|<span data-ttu-id="6961b-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6961b-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6961b-118">**true**</span><span class="sxs-lookup"><span data-stu-id="6961b-118">**true**</span></span> <br/> |<span data-ttu-id="6961b-119">Si el elemento [SavedItemFolderId](saveditemfolderid.md) no está presente, el elemento se guarda en la carpeta elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="6961b-119">If the [SavedItemFolderId](saveditemfolderid.md) element is not present, the item is saved in the Sent Items folder.</span></span> <span data-ttu-id="6961b-120">Si el elemento [SavedItemFolderId](saveditemfolderid.md) está presente, el elemento se guarda en la carpeta especificada por el elemento [SavedItemFolderId](saveditemfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="6961b-120">If the [SavedItemFolderId](saveditemfolderid.md) element is present, the item is saved in the folder that is specified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
|<span data-ttu-id="6961b-121">**false**</span><span class="sxs-lookup"><span data-stu-id="6961b-121">**false**</span></span> <br/> |<span data-ttu-id="6961b-122">Si el elemento [SavedItemFolderId](saveditemfolderid.md) no está presente, no se guarda el elemento.</span><span class="sxs-lookup"><span data-stu-id="6961b-122">If the [SavedItemFolderId](saveditemfolderid.md) element is not present, the item is not saved.</span></span> <span data-ttu-id="6961b-123">Si el elemento [SavedItemFolderId](saveditemfolderid.md) está presente, se devolverá una respuesta de error con un elemento [ResponseCode](responsecode.md) que contiene el valor **ErrorInvalidSendItemSaveSettings** .</span><span class="sxs-lookup"><span data-stu-id="6961b-123">If the [SavedItemFolderId](saveditemfolderid.md) element is present, an error response will be returned with a [ResponseCode](responsecode.md) element that contains the **ErrorInvalidSendItemSaveSettings** value.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6961b-124">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6961b-124">Child elements</span></span>

|<span data-ttu-id="6961b-125">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6961b-125">**Element**</span></span>|<span data-ttu-id="6961b-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6961b-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6961b-127">ItemIds</span><span class="sxs-lookup"><span data-stu-id="6961b-127">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="6961b-128">Contiene las identidades únicas de los elementos, los elementos de ocurrencia y los elementos maestros periódicos que se usan para eliminar, enviar, obtener, mover o copiar elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6961b-128">Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6961b-129">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="6961b-129">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> |<span data-ttu-id="6961b-130">Identifica la carpeta de destino para las operaciones que actualizan, envían y crean elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6961b-130">Identifies the target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6961b-131">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6961b-131">Parent elements</span></span>

<span data-ttu-id="6961b-132">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6961b-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6961b-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6961b-133">Remarks</span></span>

<span data-ttu-id="6961b-134">Si se envía un elemento de la carpeta elementos enviados, se elimina el elemento enviado y se coloca una copia en la carpeta elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="6961b-134">If an item in the Sent Items folder is sent, the sent item is deleted and a copy of it is put in the Sent Items folder.</span></span>
  
<span data-ttu-id="6961b-135">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="6961b-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6961b-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6961b-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6961b-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="6961b-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6961b-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6961b-138">Schema Name</span></span>  <br/> |<span data-ttu-id="6961b-139">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="6961b-139">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6961b-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6961b-140">Validation File</span></span>  <br/> |<span data-ttu-id="6961b-141">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6961b-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6961b-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6961b-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="6961b-143">Falso</span><span class="sxs-lookup"><span data-stu-id="6961b-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6961b-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="6961b-144">See also</span></span>



[<span data-ttu-id="6961b-145">Operación SendItem</span><span class="sxs-lookup"><span data-stu-id="6961b-145">SendItem operation</span></span>](senditem-operation.md)

