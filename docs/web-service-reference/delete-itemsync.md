---
title: Eliminar (ItemSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Delete
api_type:
- schema
ms.assetid: 4f372d57-2e39-46af-9d83-6c8c55108587
description: El elemento Eliminar identifica un solo elemento para eliminar en el almacén de cliente local.
ms.openlocfilehash: 18b7ae2f97db2de64896680c3aa76f2590c03177
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764081"
---
# <a name="delete-itemsync"></a><span data-ttu-id="7357d-103">Eliminar (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="7357d-103">Delete (ItemSync)</span></span>

<span data-ttu-id="7357d-104">El elemento **Eliminar** identifica un solo elemento para eliminar en el almacén de cliente local.</span><span class="sxs-lookup"><span data-stu-id="7357d-104">The **Delete** element identifies a single item to delete in the local client store.</span></span> 
  
- [<span data-ttu-id="7357d-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="7357d-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)  
- [<span data-ttu-id="7357d-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7357d-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="7357d-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7357d-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)  
- [<span data-ttu-id="7357d-108">Cambios (elementos)</span><span class="sxs-lookup"><span data-stu-id="7357d-108">Changes (Items)</span></span>](changes-items.md)  
- [<span data-ttu-id="7357d-109">Eliminar (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="7357d-109">Delete (ItemSync)</span></span>](delete-itemsync.md)
  
```xml
<Delete>
   <ItemId/>
</Delete>
```

<span data-ttu-id="7357d-110">**SyncFolderItemsDeleteType**</span><span class="sxs-lookup"><span data-stu-id="7357d-110">**SyncFolderItemsDeleteType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="7357d-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7357d-111">Attributes and elements</span></span>

<span data-ttu-id="7357d-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7357d-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7357d-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="7357d-113">Attributes</span></span>

<span data-ttu-id="7357d-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7357d-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7357d-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7357d-115">Child elements</span></span>

|<span data-ttu-id="7357d-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="7357d-116">**Element**</span></span>|<span data-ttu-id="7357d-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7357d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7357d-118">ItemId</span><span class="sxs-lookup"><span data-stu-id="7357d-118">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="7357d-119">Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7357d-119">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7357d-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7357d-120">Parent elements</span></span>

|<span data-ttu-id="7357d-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="7357d-121">**Element**</span></span>|<span data-ttu-id="7357d-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7357d-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7357d-123">Cambios (elementos)</span><span class="sxs-lookup"><span data-stu-id="7357d-123">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="7357d-124">Contiene una matriz de secuencia de tipos de cambio que representan el tipo de las diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7357d-124">Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7357d-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7357d-125">Remarks</span></span>

<span data-ttu-id="7357d-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="7357d-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7357d-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7357d-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7357d-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7357d-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7357d-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7357d-129">Schema name</span></span>  <br/> |<span data-ttu-id="7357d-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7357d-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="7357d-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7357d-131">Validation file</span></span>  <br/> |<span data-ttu-id="7357d-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7357d-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7357d-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7357d-133">Can be empty</span></span>  <br/> |<span data-ttu-id="7357d-134">False</span><span class="sxs-lookup"><span data-stu-id="7357d-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7357d-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="7357d-135">See also</span></span>

- [<span data-ttu-id="7357d-136">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="7357d-136">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="7357d-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7357d-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

