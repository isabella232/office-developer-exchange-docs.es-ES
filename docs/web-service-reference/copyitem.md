---
title: CopyItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyItem
api_type:
- schema
ms.assetid: ffb4c13e-e7ea-4e6b-87a0-509ce5371100
description: El elemento CopyItem define una solicitud para copiar un elemento en un buzón en el almacén de Exchange.
ms.openlocfilehash: 08cc1b67f7c7d369263acfc4b3d13e8aa70d2d5f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763900"
---
# <a name="copyitem"></a><span data-ttu-id="a3d01-103">CopyItem</span><span class="sxs-lookup"><span data-stu-id="a3d01-103">CopyItem</span></span>

<span data-ttu-id="a3d01-104">El elemento **CopyItem** define una solicitud para copiar un elemento en un buzón en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a3d01-104">The **CopyItem** element defines a request to copy an item in a mailbox in the Exchange store.</span></span> 
  
```XML
<CopyItem>
   <ToFolderId/>
   <ItemIds/>
   <ReturnNewItemIds/>
</CopyItem>
```

 <span data-ttu-id="a3d01-105">**CopyItemType**</span><span class="sxs-lookup"><span data-stu-id="a3d01-105">**CopyItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a3d01-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a3d01-106">Attributes and elements</span></span>

<span data-ttu-id="a3d01-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a3d01-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3d01-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a3d01-108">Attributes</span></span>

<span data-ttu-id="a3d01-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a3d01-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a3d01-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a3d01-110">Child elements</span></span>

|<span data-ttu-id="a3d01-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a3d01-111">**Element**</span></span>|<span data-ttu-id="a3d01-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a3d01-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3d01-113">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="a3d01-113">ToFolderId</span></span>](tofolderid.md) <br/> |<span data-ttu-id="a3d01-114">Representa la carpeta de destino para el elemento copiado.</span><span class="sxs-lookup"><span data-stu-id="a3d01-114">Represents the destination folder for a copied item.</span></span>  <br/> |
|[<span data-ttu-id="a3d01-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="a3d01-115">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="a3d01-116">Contiene una matriz de elementos identificados a copiar en la carpeta representada por el elemento [ToFolderId](tofolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="a3d01-116">Contains an array of identified items to copy to the folder represented by the [ToFolderId](tofolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="a3d01-117">ReturnNewItemIds</span><span class="sxs-lookup"><span data-stu-id="a3d01-117">ReturnNewItemIds</span></span>](returnnewitemids.md) <br/> |<span data-ttu-id="a3d01-118">Indica si se devuelven los identificadores de elemento de los elementos nuevos en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a3d01-118">Indicates whether the item identifiers of new items are returned in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a3d01-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a3d01-119">Parent elements</span></span>

<span data-ttu-id="a3d01-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a3d01-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a3d01-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3d01-121">Remarks</span></span>

<span data-ttu-id="a3d01-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a3d01-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a3d01-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a3d01-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3d01-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a3d01-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a3d01-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a3d01-125">Schema Name</span></span>  <br/> |<span data-ttu-id="a3d01-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a3d01-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a3d01-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a3d01-127">Validation File</span></span>  <br/> |<span data-ttu-id="a3d01-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a3d01-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a3d01-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a3d01-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="a3d01-130">False</span><span class="sxs-lookup"><span data-stu-id="a3d01-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a3d01-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="a3d01-131">See also</span></span>



[<span data-ttu-id="a3d01-132">Operación CopyItem</span><span class="sxs-lookup"><span data-stu-id="a3d01-132">CopyItem operation</span></span>](copyitem-operation.md)


- [<span data-ttu-id="a3d01-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="a3d01-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

