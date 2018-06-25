---
title: MoveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveItem
api_type:
- schema
ms.assetid: a4593377-22dd-415f-b01d-387389ef650f
description: El elemento MoveItem define una solicitud para mover un elemento en el almacén de Exchange.
ms.openlocfilehash: cd7f35bdabe8a596f4c186df1c8cd54e0ea1c540
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836486"
---
# <a name="moveitem"></a><span data-ttu-id="b1491-103">MoveItem</span><span class="sxs-lookup"><span data-stu-id="b1491-103">MoveItem</span></span>

<span data-ttu-id="b1491-104">El elemento **MoveItem** define una solicitud para mover un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b1491-104">The **MoveItem** element defines a request to move an item in the Exchange store.</span></span> 
  
```XML
<MoveItem>
   <ToFolderId/>
   <ItemIds/>
   <ReturnNewItemIds/>
</MoveItem>
```

 <span data-ttu-id="b1491-105">**MoveItemType**</span><span class="sxs-lookup"><span data-stu-id="b1491-105">**MoveItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b1491-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b1491-106">Attributes and elements</span></span>

<span data-ttu-id="b1491-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b1491-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1491-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b1491-108">Attributes</span></span>

<span data-ttu-id="b1491-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b1491-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b1491-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b1491-110">Child elements</span></span>

|<span data-ttu-id="b1491-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b1491-111">**Element**</span></span>|<span data-ttu-id="b1491-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b1491-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1491-113">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="b1491-113">ToFolderId</span></span>](tofolderid.md) <br/> |<span data-ttu-id="b1491-114">Representa la carpeta de destino para un elemento que se ha movido.</span><span class="sxs-lookup"><span data-stu-id="b1491-114">Represents the destination folder for a moved item.</span></span>  <br/> |
|[<span data-ttu-id="b1491-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="b1491-115">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="b1491-116">Contiene una matriz de elementos identificados para mover a la carpeta representada por el elemento [ToFolderId](tofolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="b1491-116">Contains an array of identified items to move to the folder represented by the [ToFolderId](tofolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="b1491-117">ReturnNewItemIds</span><span class="sxs-lookup"><span data-stu-id="b1491-117">ReturnNewItemIds</span></span>](returnnewitemids.md) <br/> |<span data-ttu-id="b1491-118">Indica si se devuelven los identificadores de elemento de los elementos nuevos en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b1491-118">Indicates whether the item identifiers of new items are returned in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b1491-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b1491-119">Parent elements</span></span>

<span data-ttu-id="b1491-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b1491-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="b1491-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b1491-121">Text value</span></span>

<span data-ttu-id="b1491-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b1491-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b1491-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b1491-123">Remarks</span></span>

<span data-ttu-id="b1491-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b1491-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b1491-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b1491-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1491-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b1491-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b1491-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b1491-127">Schema Name</span></span>  <br/> |<span data-ttu-id="b1491-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b1491-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b1491-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b1491-129">Validation File</span></span>  <br/> |<span data-ttu-id="b1491-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b1491-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b1491-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b1491-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="b1491-132">False</span><span class="sxs-lookup"><span data-stu-id="b1491-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b1491-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1491-133">See also</span></span>



[<span data-ttu-id="b1491-134">Operación MoveItem</span><span class="sxs-lookup"><span data-stu-id="b1491-134">MoveItem operation</span></span>](moveitem-operation.md)


- [<span data-ttu-id="b1491-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b1491-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

