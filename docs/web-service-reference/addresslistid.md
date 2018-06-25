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
ms.openlocfilehash: d8a513559b7d127559537b43d7c6c0a4db121702
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763417"
---
# <a name="addresslistid"></a><span data-ttu-id="b0bfc-103">AddressListId</span><span class="sxs-lookup"><span data-stu-id="b0bfc-103">AddressListId</span></span>

<span data-ttu-id="b0bfc-104">El elemento **AddressListId** especifica el identificador de una lista de direcciones.</span><span class="sxs-lookup"><span data-stu-id="b0bfc-104">The **AddressListId** element specifies the identifier of an address list.</span></span> 
  
```XML
<AddressListId Id="">
</AddressListId>
```

 <span data-ttu-id="b0bfc-105">**AddressListIdType**</span><span class="sxs-lookup"><span data-stu-id="b0bfc-105">**AddressListIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b0bfc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b0bfc-106">Attributes and elements</span></span>

<span data-ttu-id="b0bfc-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b0bfc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b0bfc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b0bfc-108">Attributes</span></span>

|<span data-ttu-id="b0bfc-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="b0bfc-109">**Attribute**</span></span>|<span data-ttu-id="b0bfc-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b0bfc-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b0bfc-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="b0bfc-111">**Id**</span></span> <br/> |<span data-ttu-id="b0bfc-112">Un identificador de lista de direcciones de cadena.</span><span class="sxs-lookup"><span data-stu-id="b0bfc-112">A string address list identifier.</span></span> <span data-ttu-id="b0bfc-113">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="b0bfc-113">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b0bfc-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b0bfc-114">Child elements</span></span>

<span data-ttu-id="b0bfc-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b0bfc-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b0bfc-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b0bfc-116">Parent elements</span></span>

|<span data-ttu-id="b0bfc-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="b0bfc-117">**Element**</span></span>|<span data-ttu-id="b0bfc-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b0bfc-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0bfc-119">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="b0bfc-119">ContextFolderId</span></span>](contextfolderid.md) <br/> |<span data-ttu-id="b0bfc-120">Indica la carpeta que está destinada a las acciones que utilizan carpetas.</span><span class="sxs-lookup"><span data-stu-id="b0bfc-120">Indicates the folder that is targeted for actions that use folders.</span></span> <span data-ttu-id="b0bfc-121">Este elemento debe estar presente al copiar, eliminar, mover y establecer el estado de lectura en los elementos de una conversación en una carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="b0bfc-121">This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.</span></span>  <br/> |
|[<span data-ttu-id="b0bfc-122">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="b0bfc-122">CopyToFolder</span></span>](copytofolder.md) <br/> |<span data-ttu-id="b0bfc-123">Especifica el identificador de la carpeta a la que se copian los elementos de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b0bfc-123">Specifies the identifier of the folder to which email items are copied.</span></span>  <br/> |
|[<span data-ttu-id="b0bfc-124">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="b0bfc-124">DestinationFolderId</span></span>](destinationfolderid.md) <br/> |<span data-ttu-id="b0bfc-125">Indica la carpeta de destino para copiar y mover las acciones.</span><span class="sxs-lookup"><span data-stu-id="b0bfc-125">Indicates the destination folder for copy and move actions.</span></span>  <br/> |
|[<span data-ttu-id="b0bfc-126">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="b0bfc-126">MoveToFolder</span></span>](movetofolder.md) <br/> |<span data-ttu-id="b0bfc-127">Especifica el identificador de la carpeta a la que se mueven los elementos de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="b0bfc-127">Specifies the identifier of the folder to which email items are moved</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0bfc-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0bfc-128">Remarks</span></span>

<span data-ttu-id="b0bfc-129">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b0bfc-129">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b0bfc-130">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b0bfc-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b0bfc-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b0bfc-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0bfc-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b0bfc-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b0bfc-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b0bfc-133">Schema Name</span></span>  <br/> |<span data-ttu-id="b0bfc-134">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="b0bfc-134">Type schema</span></span>  <br/> |
|<span data-ttu-id="b0bfc-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b0bfc-135">Validation File</span></span>  <br/> |<span data-ttu-id="b0bfc-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b0bfc-136">types.xsd</span></span>  <br/> |
|<span data-ttu-id="b0bfc-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b0bfc-137">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="b0bfc-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0bfc-138">See also</span></span>

- [<span data-ttu-id="b0bfc-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b0bfc-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

