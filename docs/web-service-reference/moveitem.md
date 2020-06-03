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
ms.openlocfilehash: 61dbb91cc20a71f50999241b3daa21bf8ebfbcc8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530404"
---
# <a name="moveitem"></a><span data-ttu-id="f4bb3-103">MoveItem</span><span class="sxs-lookup"><span data-stu-id="f4bb3-103">MoveItem</span></span>

<span data-ttu-id="f4bb3-104">El elemento **MoveItem** define una solicitud para mover un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f4bb3-104">The **MoveItem** element defines a request to move an item in the Exchange store.</span></span> 
  
```XML
<MoveItem>
   <ToFolderId/>
   <ItemIds/>
   <ReturnNewItemIds/>
</MoveItem>
```

 <span data-ttu-id="f4bb3-105">**MoveItemType**</span><span class="sxs-lookup"><span data-stu-id="f4bb3-105">**MoveItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f4bb3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f4bb3-106">Attributes and elements</span></span>

<span data-ttu-id="f4bb3-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f4bb3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4bb3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f4bb3-108">Attributes</span></span>

<span data-ttu-id="f4bb3-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f4bb3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f4bb3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f4bb3-110">Child elements</span></span>

|<span data-ttu-id="f4bb3-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f4bb3-111">**Element**</span></span>|<span data-ttu-id="f4bb3-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f4bb3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f4bb3-113">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="f4bb3-113">ToFolderId</span></span>](tofolderid.md) <br/> |<span data-ttu-id="f4bb3-114">Representa la carpeta de destino de un elemento movido.</span><span class="sxs-lookup"><span data-stu-id="f4bb3-114">Represents the destination folder for a moved item.</span></span>  <br/> |
|[<span data-ttu-id="f4bb3-115">ItemIds</span><span class="sxs-lookup"><span data-stu-id="f4bb3-115">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="f4bb3-116">Contiene una matriz de elementos identificados para mover a la carpeta representada por el elemento [ToFolderId](tofolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="f4bb3-116">Contains an array of identified items to move to the folder represented by the [ToFolderId](tofolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="f4bb3-117">ReturnNewItemIds</span><span class="sxs-lookup"><span data-stu-id="f4bb3-117">ReturnNewItemIds</span></span>](returnnewitemids.md) <br/> |<span data-ttu-id="f4bb3-118">Indica si los identificadores de elemento de los nuevos elementos se devuelven en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f4bb3-118">Indicates whether the item identifiers of new items are returned in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f4bb3-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f4bb3-119">Parent elements</span></span>

<span data-ttu-id="f4bb3-120">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f4bb3-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="f4bb3-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f4bb3-121">Text value</span></span>

<span data-ttu-id="f4bb3-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f4bb3-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f4bb3-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f4bb3-123">Remarks</span></span>

<span data-ttu-id="f4bb3-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f4bb3-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f4bb3-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f4bb3-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4bb3-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="f4bb3-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f4bb3-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f4bb3-127">Schema Name</span></span>  <br/> |<span data-ttu-id="f4bb3-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f4bb3-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f4bb3-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f4bb3-129">Validation File</span></span>  <br/> |<span data-ttu-id="f4bb3-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f4bb3-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f4bb3-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f4bb3-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="f4bb3-132">Falso</span><span class="sxs-lookup"><span data-stu-id="f4bb3-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4bb3-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4bb3-133">See also</span></span>



[<span data-ttu-id="f4bb3-134">Operación MoveItem</span><span class="sxs-lookup"><span data-stu-id="f4bb3-134">MoveItem operation</span></span>](moveitem-operation.md)


- [<span data-ttu-id="f4bb3-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="f4bb3-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

