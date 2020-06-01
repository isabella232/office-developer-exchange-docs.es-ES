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
description: El elemento UploadItems representa una solicitud para cargar elementos en un buzón.
ms.openlocfilehash: 8fdb7253926e030085374b650e792349e598ee4a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468827"
---
# <a name="uploaditems"></a><span data-ttu-id="9dba0-103">UploadItems</span><span class="sxs-lookup"><span data-stu-id="9dba0-103">UploadItems</span></span>

<span data-ttu-id="9dba0-104">El elemento **UploadItems** representa una solicitud para cargar elementos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="9dba0-104">The **UploadItems** element represents a request to upload items into a mailbox.</span></span> 
  
[<span data-ttu-id="9dba0-105">UploadItems</span><span class="sxs-lookup"><span data-stu-id="9dba0-105">UploadItems</span></span>](uploaditems.md)
  
```XML
<UploadItems>
   <Items/>
</UploadItems>
```

 <span data-ttu-id="9dba0-106">**UploadItemsType**</span><span class="sxs-lookup"><span data-stu-id="9dba0-106">**UploadItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9dba0-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9dba0-107">Attributes and elements</span></span>

<span data-ttu-id="9dba0-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9dba0-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9dba0-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="9dba0-109">Attributes</span></span>

<span data-ttu-id="9dba0-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9dba0-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9dba0-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9dba0-111">Child elements</span></span>

|<span data-ttu-id="9dba0-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9dba0-112">**Element**</span></span>|<span data-ttu-id="9dba0-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9dba0-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9dba0-114">Elementos (NonEmptyArrayOfUploadItemsType)</span><span class="sxs-lookup"><span data-stu-id="9dba0-114">Items (NonEmptyArrayOfUploadItemsType)</span></span>](items-nonemptyarrayofuploaditemstype.md) <br/> |<span data-ttu-id="9dba0-115">Contiene una matriz de elementos que se van a cargar en un buzón.</span><span class="sxs-lookup"><span data-stu-id="9dba0-115">Contains an array of items to upload into a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9dba0-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9dba0-116">Parent elements</span></span>

<span data-ttu-id="9dba0-117">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9dba0-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="9dba0-118">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9dba0-118">Text value</span></span>

<span data-ttu-id="9dba0-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9dba0-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9dba0-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9dba0-120">Remarks</span></span>

<span data-ttu-id="9dba0-121">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="9dba0-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9dba0-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9dba0-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9dba0-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="9dba0-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9dba0-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9dba0-124">Schema Name</span></span>  <br/> |<span data-ttu-id="9dba0-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="9dba0-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="9dba0-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9dba0-126">Validation File</span></span>  <br/> |<span data-ttu-id="9dba0-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9dba0-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9dba0-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9dba0-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="9dba0-129">Falso</span><span class="sxs-lookup"><span data-stu-id="9dba0-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9dba0-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="9dba0-130">See also</span></span>



[<span data-ttu-id="9dba0-131">Operación ExportItems</span><span class="sxs-lookup"><span data-stu-id="9dba0-131">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="9dba0-132">Operación UploadItems</span><span class="sxs-lookup"><span data-stu-id="9dba0-132">UploadItems operation</span></span>](uploaditems-operation.md)

