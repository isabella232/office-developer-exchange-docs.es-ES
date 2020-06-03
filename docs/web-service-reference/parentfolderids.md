---
title: ParentFolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentFolderIds
api_type:
- schema
ms.assetid: e7998023-e5e0-465c-91fa-2aa6d1559f64
description: El elemento ParentFolderIds identifica las carpetas para las operaciones FindItem y FindFolder que se van a buscar.
ms.openlocfilehash: 6bc4b9cfe96c6c83cbeb623ec176e33177356bbc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465432"
---
# <a name="parentfolderids"></a><span data-ttu-id="c8702-103">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="c8702-103">ParentFolderIds</span></span>

<span data-ttu-id="c8702-104">El elemento **ParentFolderIds** identifica las carpetas para las operaciones FindItem y FindFolder que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="c8702-104">The **ParentFolderIds** element identifies folders for the FindItem and FindFolder operations to search.</span></span> 
  
```xml
<ParentFolderIds>
   <DistinguishedFolderId/>
<ParentFolderIds>
```

```xml
<ParentFolderIds>
   <FolderId/> 
<ParentFolderIds>
```

<span data-ttu-id="c8702-105">**NonEmptyArrayOfBaseFolderIdsType**</span><span class="sxs-lookup"><span data-stu-id="c8702-105">**NonEmptyArrayOfBaseFolderIdsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c8702-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c8702-106">Attributes and elements</span></span>

<span data-ttu-id="c8702-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c8702-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c8702-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c8702-108">Attributes</span></span>

<span data-ttu-id="c8702-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c8702-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c8702-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c8702-110">Child elements</span></span>

|<span data-ttu-id="c8702-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c8702-111">**Element**</span></span>|<span data-ttu-id="c8702-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8702-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8702-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="c8702-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="c8702-114">Contiene el identificador y la clave de cambio de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c8702-114">Contains the identifier and change key of a folder.</span></span> <span data-ttu-id="c8702-115">El elemento **ParentFolderIds** debe usar este elemento o el elemento [DistinguishedFolderId](distinguishedfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="c8702-115">The **ParentFolderIds** element must use either this element or the [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span>  <br/> |
|[<span data-ttu-id="c8702-116">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="c8702-116">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="c8702-117">Identifica las carpetas de Microsoft Exchange Server 2007 a las que se puede hacer referencia por su nombre.</span><span class="sxs-lookup"><span data-stu-id="c8702-117">Identifies Microsoft Exchange Server 2007 folders that can be referenced by name.</span></span> <span data-ttu-id="c8702-118">El elemento **ParentFolderIds** debe usar este elemento o el elemento [FolderId](folderid.md) .</span><span class="sxs-lookup"><span data-stu-id="c8702-118">The **ParentFolderIds** element must use either this element or the [FolderId](folderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c8702-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c8702-119">Parent elements</span></span>

|<span data-ttu-id="c8702-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c8702-120">**Element**</span></span>|<span data-ttu-id="c8702-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c8702-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8702-122">FindFolder</span><span class="sxs-lookup"><span data-stu-id="c8702-122">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="c8702-123">Define una solicitud para identificar las carpetas en un buzón.</span><span class="sxs-lookup"><span data-stu-id="c8702-123">Defines a request to identify folders in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c8702-124">FindItem</span><span class="sxs-lookup"><span data-stu-id="c8702-124">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="c8702-125">Define una solicitud para buscar elementos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="c8702-125">Defines a request to find items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="c8702-126">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="c8702-126">ResolveNames</span></span>](resolvenames.md) <br/> |<span data-ttu-id="c8702-127">Define una solicitud para resolver nombres ambiguos.</span><span class="sxs-lookup"><span data-stu-id="c8702-127">Defines a request to resolve ambiguous names.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8702-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c8702-128">Remarks</span></span>

<span data-ttu-id="c8702-129">El elemento **ParentFolderIds** debe usar el elemento [FolderId](folderid.md) o [DistinguishedFolderId](distinguishedfolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="c8702-129">The **ParentFolderIds** element must use either the [FolderId](folderid.md) or the [DistinguishedFolderId](distinguishedfolderid.md) element.</span></span> <span data-ttu-id="c8702-130">Se puede definir un número ilimitado de carpetas para la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c8702-130">An unlimited number of folders can be defined for the search.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c8702-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c8702-131">Example</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="c8702-132">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c8702-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8702-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="c8702-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c8702-134">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c8702-134">Schema Name</span></span>  <br/> |<span data-ttu-id="c8702-135">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c8702-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c8702-136">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c8702-136">Validation File</span></span>  <br/> |<span data-ttu-id="c8702-137">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c8702-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c8702-138">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c8702-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="c8702-139">Falso</span><span class="sxs-lookup"><span data-stu-id="c8702-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8702-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8702-140">See also</span></span>

- [<span data-ttu-id="c8702-141">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="c8702-141">FindFolder operation</span></span>](findfolder-operation.md)  
- [<span data-ttu-id="c8702-142">Operación FindItem</span><span class="sxs-lookup"><span data-stu-id="c8702-142">FindItem operation</span></span>](finditem-operation.md) 
- [<span data-ttu-id="c8702-143">Operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="c8702-143">ResolveNames operation</span></span>](resolvenames-operation.md)

