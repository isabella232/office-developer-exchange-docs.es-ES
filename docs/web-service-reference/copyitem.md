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
description: El elemento CopyItem define una solicitud para copiar un elemento en un buzón de correo en el almacén de Exchange.
ms.openlocfilehash: b9af1670fd580107de08ad3b950191399436388d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458505"
---
# <a name="copyitem"></a><span data-ttu-id="333d9-103">CopyItem</span><span class="sxs-lookup"><span data-stu-id="333d9-103">CopyItem</span></span>

<span data-ttu-id="333d9-104">El elemento **CopyItem** define una solicitud para copiar un elemento en un buzón de correo en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="333d9-104">The **CopyItem** element defines a request to copy an item in a mailbox in the Exchange store.</span></span> 
  
```XML
<CopyItem>
   <ToFolderId/>
   <ItemIds/>
   <ReturnNewItemIds/>
</CopyItem>
```

 <span data-ttu-id="333d9-105">**CopyItemType**</span><span class="sxs-lookup"><span data-stu-id="333d9-105">**CopyItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="333d9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="333d9-106">Attributes and elements</span></span>

<span data-ttu-id="333d9-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="333d9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="333d9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="333d9-108">Attributes</span></span>

<span data-ttu-id="333d9-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="333d9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="333d9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="333d9-110">Child elements</span></span>

|<span data-ttu-id="333d9-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="333d9-111">**Element**</span></span>|<span data-ttu-id="333d9-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="333d9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="333d9-113">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="333d9-113">ToFolderId</span></span>](tofolderid.md) <br/> |<span data-ttu-id="333d9-114">Representa la carpeta de destino de un elemento copiado.</span><span class="sxs-lookup"><span data-stu-id="333d9-114">Represents the destination folder for a copied item.</span></span>  <br/> |
|[<span data-ttu-id="333d9-115">ItemIds</span><span class="sxs-lookup"><span data-stu-id="333d9-115">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="333d9-116">Contiene una matriz de elementos identificados que se van a copiar en la carpeta representada por el elemento [ToFolderId](tofolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="333d9-116">Contains an array of identified items to copy to the folder represented by the [ToFolderId](tofolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="333d9-117">ReturnNewItemIds</span><span class="sxs-lookup"><span data-stu-id="333d9-117">ReturnNewItemIds</span></span>](returnnewitemids.md) <br/> |<span data-ttu-id="333d9-118">Indica si los identificadores de elemento de los nuevos elementos se devuelven en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="333d9-118">Indicates whether the item identifiers of new items are returned in the response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="333d9-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="333d9-119">Parent elements</span></span>

<span data-ttu-id="333d9-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="333d9-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="333d9-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="333d9-121">Remarks</span></span>

<span data-ttu-id="333d9-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="333d9-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="333d9-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="333d9-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="333d9-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="333d9-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="333d9-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="333d9-125">Schema Name</span></span>  <br/> |<span data-ttu-id="333d9-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="333d9-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="333d9-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="333d9-127">Validation File</span></span>  <br/> |<span data-ttu-id="333d9-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="333d9-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="333d9-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="333d9-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="333d9-130">Falso</span><span class="sxs-lookup"><span data-stu-id="333d9-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="333d9-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="333d9-131">See also</span></span>



[<span data-ttu-id="333d9-132">Operación CopyItem</span><span class="sxs-lookup"><span data-stu-id="333d9-132">CopyItem operation</span></span>](copyitem-operation.md)


- [<span data-ttu-id="333d9-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="333d9-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

