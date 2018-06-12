---
title: ReturnNewItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aeef79e4-31e1-4213-b627-9bac676be018
description: El elemento ReturnNewItemIds indica si se devuelven los identificadores de elemento de los elementos nuevos en la respuesta.
ms.openlocfilehash: 6d3bc83c05a82d6e448041167676f41c2620dcd4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837232"
---
# <a name="returnnewitemids"></a><span data-ttu-id="d0b37-103">ReturnNewItemIds</span><span class="sxs-lookup"><span data-stu-id="d0b37-103">ReturnNewItemIds</span></span>

<span data-ttu-id="d0b37-104">El elemento **ReturnNewItemIds** indica si se devuelven los identificadores de elemento de los elementos nuevos en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0b37-104">The **ReturnNewItemIds** element indicates whether the item identifiers of new items are returned in the response.</span></span> 
  
```XML
<ReturnNewItemIds/>
```

 <span data-ttu-id="d0b37-105">**xs: Boolean**</span><span class="sxs-lookup"><span data-stu-id="d0b37-105">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0b37-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d0b37-106">Attributes and elements</span></span>

<span data-ttu-id="d0b37-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d0b37-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0b37-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d0b37-108">Attributes</span></span>

<span data-ttu-id="d0b37-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d0b37-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0b37-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d0b37-110">Child elements</span></span>

<span data-ttu-id="d0b37-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d0b37-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d0b37-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d0b37-112">Parent elements</span></span>

|<span data-ttu-id="d0b37-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d0b37-113">**Element**</span></span>|<span data-ttu-id="d0b37-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d0b37-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0b37-115">CopyItem</span><span class="sxs-lookup"><span data-stu-id="d0b37-115">CopyItem</span></span>](copyitem.md) <br/> |<span data-ttu-id="d0b37-116">Define una solicitud para copiar un elemento en un buzón en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d0b37-116">Defines a request to copy an item in a mailbox in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="d0b37-117">MoveItem</span><span class="sxs-lookup"><span data-stu-id="d0b37-117">MoveItem</span></span>](moveitem.md) <br/> |<span data-ttu-id="d0b37-118">Define una solicitud para mover un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d0b37-118">Defines a request to move an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d0b37-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d0b37-119">Text value</span></span>

<span data-ttu-id="d0b37-120">Un valor de texto de **true** para el elemento **ReturnNewItemIds** indica que se devuelven los identificadores de elemento nuevo en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0b37-120">A text value of **true** for the **ReturnNewItemIds** element indicates that the new item identifiers are returned in the response.</span></span> <span data-ttu-id="d0b37-121">Un valor de **false** indica que no se devuelven los identificadores de elemento nuevo en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0b37-121">A value of **false** indicates that the new item identifiers are not returned in the response.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d0b37-122">Notas</span><span class="sxs-lookup"><span data-stu-id="d0b37-122">Remarks</span></span>

<span data-ttu-id="d0b37-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d0b37-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0b37-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d0b37-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0b37-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d0b37-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d0b37-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d0b37-126">Schema Name</span></span>  <br/> |<span data-ttu-id="d0b37-127">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="d0b37-127">Message schema</span></span>  <br/> |
|<span data-ttu-id="d0b37-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d0b37-128">Validation File</span></span>  <br/> |<span data-ttu-id="d0b37-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d0b37-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d0b37-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d0b37-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="d0b37-131">False</span><span class="sxs-lookup"><span data-stu-id="d0b37-131">False</span></span>  <br/> |
   

