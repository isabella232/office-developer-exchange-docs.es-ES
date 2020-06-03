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
description: El elemento Delete identifica un solo elemento que se va a eliminar en el almacén del cliente local.
ms.openlocfilehash: 6e30ddc7f7248fe7ff7136e19ba58c7d5d8a800f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44454683"
---
# <a name="delete-itemsync"></a><span data-ttu-id="5f8c0-103">Eliminar (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="5f8c0-103">Delete (ItemSync)</span></span>

<span data-ttu-id="5f8c0-104">El elemento **Delete** identifica un solo elemento que se va a eliminar en el almacén del cliente local.</span><span class="sxs-lookup"><span data-stu-id="5f8c0-104">The **Delete** element identifies a single item to delete in the local client store.</span></span> 
  
- [<span data-ttu-id="5f8c0-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="5f8c0-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)  
- [<span data-ttu-id="5f8c0-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5f8c0-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="5f8c0-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5f8c0-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)  
- [<span data-ttu-id="5f8c0-108">Cambios (elementos)</span><span class="sxs-lookup"><span data-stu-id="5f8c0-108">Changes (Items)</span></span>](changes-items.md)  
- [<span data-ttu-id="5f8c0-109">Eliminar (ItemSync)</span><span class="sxs-lookup"><span data-stu-id="5f8c0-109">Delete (ItemSync)</span></span>](delete-itemsync.md)
  
```xml
<Delete>
   <ItemId/>
</Delete>
```

<span data-ttu-id="5f8c0-110">**SyncFolderItemsDeleteType**</span><span class="sxs-lookup"><span data-stu-id="5f8c0-110">**SyncFolderItemsDeleteType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5f8c0-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5f8c0-111">Attributes and elements</span></span>

<span data-ttu-id="5f8c0-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5f8c0-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f8c0-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="5f8c0-113">Attributes</span></span>

<span data-ttu-id="5f8c0-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5f8c0-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5f8c0-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5f8c0-115">Child elements</span></span>

|<span data-ttu-id="5f8c0-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5f8c0-116">**Element**</span></span>|<span data-ttu-id="5f8c0-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f8c0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f8c0-118">ItemId</span><span class="sxs-lookup"><span data-stu-id="5f8c0-118">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="5f8c0-119">Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5f8c0-119">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5f8c0-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5f8c0-120">Parent elements</span></span>

|<span data-ttu-id="5f8c0-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5f8c0-121">**Element**</span></span>|<span data-ttu-id="5f8c0-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f8c0-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f8c0-123">Cambios (elementos)</span><span class="sxs-lookup"><span data-stu-id="5f8c0-123">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="5f8c0-124">Contiene una matriz de secuencias de tipos de cambios que representan el tipo de diferencias entre los elementos en el cliente y los elementos en el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="5f8c0-124">Contains a sequence array of change types that represent the type of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f8c0-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f8c0-125">Remarks</span></span>

<span data-ttu-id="5f8c0-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="5f8c0-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5f8c0-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5f8c0-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f8c0-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="5f8c0-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5f8c0-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5f8c0-129">Schema name</span></span>  <br/> |<span data-ttu-id="5f8c0-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5f8c0-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="5f8c0-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5f8c0-131">Validation file</span></span>  <br/> |<span data-ttu-id="5f8c0-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="5f8c0-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5f8c0-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5f8c0-133">Can be empty</span></span>  <br/> |<span data-ttu-id="5f8c0-134">Falso</span><span class="sxs-lookup"><span data-stu-id="5f8c0-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5f8c0-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f8c0-135">See also</span></span>

- [<span data-ttu-id="5f8c0-136">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="5f8c0-136">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="5f8c0-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5f8c0-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

