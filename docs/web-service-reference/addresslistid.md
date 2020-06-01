---
title: AddressListId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a3334bb2-90dc-4fe1-96d9-890b13d9ff30
description: El elemento AddressListId especifica el identificador de una lista de direcciones.
ms.openlocfilehash: c33944bf6e41903a5de596628e1ce7ba9f7421e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463611"
---
# <a name="addresslistid"></a><span data-ttu-id="4c0e4-103">AddressListId</span><span class="sxs-lookup"><span data-stu-id="4c0e4-103">AddressListId</span></span>

<span data-ttu-id="4c0e4-104">El elemento **AddressListId** especifica el identificador de una lista de direcciones.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-104">The **AddressListId** element specifies the identifier of an address list.</span></span> 
  
```XML
<AddressListId Id="">
</AddressListId>
```

 <span data-ttu-id="4c0e4-105">**AddressListIdType**</span><span class="sxs-lookup"><span data-stu-id="4c0e4-105">**AddressListIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4c0e4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4c0e4-106">Attributes and elements</span></span>

<span data-ttu-id="4c0e4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c0e4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4c0e4-108">Attributes</span></span>

|<span data-ttu-id="4c0e4-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="4c0e4-109">**Attribute**</span></span>|<span data-ttu-id="4c0e4-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4c0e4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4c0e4-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="4c0e4-111">**Id**</span></span> <br/> |<span data-ttu-id="4c0e4-112">Identificador de lista de direcciones de cadena.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-112">A string address list identifier.</span></span> <span data-ttu-id="4c0e4-113">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-113">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4c0e4-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4c0e4-114">Child elements</span></span>

<span data-ttu-id="4c0e4-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4c0e4-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4c0e4-116">Parent elements</span></span>

|<span data-ttu-id="4c0e4-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4c0e4-117">**Element**</span></span>|<span data-ttu-id="4c0e4-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4c0e4-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4c0e4-119">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="4c0e4-119">ContextFolderId</span></span>](contextfolderid.md) <br/> |<span data-ttu-id="4c0e4-120">Indica la carpeta que está destinada a las acciones que usan carpetas.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-120">Indicates the folder that is targeted for actions that use folders.</span></span> <span data-ttu-id="4c0e4-121">Este elemento debe estar presente al copiar, eliminar, mover y establecer el estado de lectura en los elementos de la conversación de una carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-121">This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.</span></span>  <br/> |
|[<span data-ttu-id="4c0e4-122">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="4c0e4-122">CopyToFolder</span></span>](copytofolder.md) <br/> |<span data-ttu-id="4c0e4-123">Especifica el identificador de la carpeta en la que se copian los elementos de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-123">Specifies the identifier of the folder to which email items are copied.</span></span>  <br/> |
|[<span data-ttu-id="4c0e4-124">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="4c0e4-124">DestinationFolderId</span></span>](destinationfolderid.md) <br/> |<span data-ttu-id="4c0e4-125">Indica la carpeta de destino para las acciones de copiar y mover.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-125">Indicates the destination folder for copy and move actions.</span></span>  <br/> |
|[<span data-ttu-id="4c0e4-126">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="4c0e4-126">MoveToFolder</span></span>](movetofolder.md) <br/> |<span data-ttu-id="4c0e4-127">Especifica el identificador de la carpeta a la que se mueven los elementos de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="4c0e4-127">Specifies the identifier of the folder to which email items are moved</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c0e4-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4c0e4-128">Remarks</span></span>

<span data-ttu-id="4c0e4-129">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-129">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4c0e4-130">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="4c0e4-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4c0e4-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4c0e4-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c0e4-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="4c0e4-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4c0e4-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4c0e4-133">Schema Name</span></span>  <br/> |<span data-ttu-id="4c0e4-134">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="4c0e4-134">Type schema</span></span>  <br/> |
|<span data-ttu-id="4c0e4-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4c0e4-135">Validation File</span></span>  <br/> |<span data-ttu-id="4c0e4-136">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="4c0e4-136">types.xsd</span></span>  <br/> |
|<span data-ttu-id="4c0e4-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4c0e4-137">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="4c0e4-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c0e4-138">See also</span></span>

- [<span data-ttu-id="4c0e4-139">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4c0e4-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

