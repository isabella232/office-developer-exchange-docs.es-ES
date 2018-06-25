---
title: UploadItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UploadItems
api_type:
- schema
ms.assetid: fd2b9545-7213-4427-95ae-71a155b75971
description: El elemento UploadItems representa una solicitud para cargar los elementos en un buzón de correo.
ms.openlocfilehash: d3cd69cdb744431daeede736c2e156c8ab92a79b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840876"
---
# <a name="uploaditems"></a><span data-ttu-id="e0179-103">UploadItems</span><span class="sxs-lookup"><span data-stu-id="e0179-103">UploadItems</span></span>

<span data-ttu-id="e0179-104">El elemento **UploadItems** representa una solicitud para cargar los elementos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e0179-104">The **UploadItems** element represents a request to upload items into a mailbox.</span></span> 
  
[<span data-ttu-id="e0179-105">UploadItems</span><span class="sxs-lookup"><span data-stu-id="e0179-105">UploadItems</span></span>](uploaditems.md)
  
```XML
<UploadItems>
   <Items/>
</UploadItems>
```

 <span data-ttu-id="e0179-106">**UploadItemsType**</span><span class="sxs-lookup"><span data-stu-id="e0179-106">**UploadItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0179-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e0179-107">Attributes and elements</span></span>

<span data-ttu-id="e0179-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e0179-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0179-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="e0179-109">Attributes</span></span>

<span data-ttu-id="e0179-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e0179-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0179-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e0179-111">Child elements</span></span>

|<span data-ttu-id="e0179-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="e0179-112">**Element**</span></span>|<span data-ttu-id="e0179-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e0179-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0179-114">Elementos (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="e0179-114">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md) <br/> |<span data-ttu-id="e0179-115">Contiene una matriz de elementos que desea cargar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e0179-115">Contains an array of items to upload into a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e0179-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e0179-116">Parent elements</span></span>

<span data-ttu-id="e0179-117">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e0179-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="e0179-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e0179-118">Text value</span></span>

<span data-ttu-id="e0179-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e0179-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e0179-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0179-120">Remarks</span></span>

<span data-ttu-id="e0179-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="e0179-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0179-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e0179-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0179-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e0179-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e0179-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e0179-124">Schema Name</span></span>  <br/> |<span data-ttu-id="e0179-125">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="e0179-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="e0179-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e0179-126">Validation File</span></span>  <br/> |<span data-ttu-id="e0179-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e0179-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e0179-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e0179-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="e0179-129">False</span><span class="sxs-lookup"><span data-stu-id="e0179-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0179-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0179-130">See also</span></span>



[<span data-ttu-id="e0179-131">Operación ExportItems</span><span class="sxs-lookup"><span data-stu-id="e0179-131">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="e0179-132">Operación UploadItems</span><span class="sxs-lookup"><span data-stu-id="e0179-132">UploadItems operation</span></span>](uploaditems-operation.md)

