---
title: ParentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bb7aaa46-3a04-4197-aebb-8881ff10603f
description: El elemento ParentId especifica el identificador del elemento primario en una vista previa de búsqueda.
ms.openlocfilehash: e09b5f9e463c7ecdfc595c87a84584f69cab3f2c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529024"
---
# <a name="parentid"></a><span data-ttu-id="a5f50-103">ParentId</span><span class="sxs-lookup"><span data-stu-id="a5f50-103">ParentId</span></span>

<span data-ttu-id="a5f50-104">El elemento **parentId** especifica el identificador del elemento primario en una vista previa de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a5f50-104">The **ParentId** element specifies the identifier of the parent item in a search preview.</span></span> 
  
```XML
<ParentId Id="" ChangeKey=""/>
```

<span data-ttu-id="a5f50-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="a5f50-105">**ItemIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a5f50-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a5f50-106">Attributes and elements</span></span>

<span data-ttu-id="a5f50-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a5f50-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a5f50-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a5f50-108">Attributes</span></span>

|<span data-ttu-id="a5f50-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a5f50-109">**Attribute**</span></span>|<span data-ttu-id="a5f50-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a5f50-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a5f50-111">Id</span><span class="sxs-lookup"><span data-stu-id="a5f50-111">Id</span></span>  <br/> |<span data-ttu-id="a5f50-112">El valor de texto del atributo **ID** es el identificador del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="a5f50-112">The text value of the **Id** attribute is the identifier of the parent item.</span></span>  <br/> |
|<span data-ttu-id="a5f50-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="a5f50-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="a5f50-114">El valor de texto del atributo **changekey** es la clave de cambio del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="a5f50-114">The text value of the **ChangeKey** attribute is the change key of the parent item.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a5f50-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a5f50-115">Child elements</span></span>

<span data-ttu-id="a5f50-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a5f50-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a5f50-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a5f50-117">Parent elements</span></span>

[<span data-ttu-id="a5f50-118">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="a5f50-118">SearchPreviewItem</span></span>](searchpreviewitem.md)
  
## <a name="remarks"></a><span data-ttu-id="a5f50-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5f50-119">Remarks</span></span>

<span data-ttu-id="a5f50-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a5f50-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a5f50-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a5f50-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a5f50-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a5f50-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a5f50-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="a5f50-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a5f50-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a5f50-124">Schema name</span></span>  <br/> |<span data-ttu-id="a5f50-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a5f50-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="a5f50-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a5f50-126">Validation file</span></span>  <br/> |<span data-ttu-id="a5f50-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a5f50-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a5f50-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a5f50-128">Can be empty</span></span>  <br/> |<span data-ttu-id="a5f50-129">true</span><span class="sxs-lookup"><span data-stu-id="a5f50-129">true</span></span>  <br/> |
   

