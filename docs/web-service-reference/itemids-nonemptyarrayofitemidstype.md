---
title: ItemIds (NonEmptyArrayOfItemIdsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemIds
api_type:
- schema
ms.assetid: e895782a-74fe-4216-8ac2-c3c88c4b232d
description: El elemento ItemIds contiene una matriz de identificadores de elementos que identifican los elementos que se van a exportar desde un buzón.
ms.openlocfilehash: 16c2633528e2ecbc863cfdde645e0f431b4c4297
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468596"
---
# <a name="itemids-nonemptyarrayofitemidstype"></a><span data-ttu-id="239f2-103">ItemIds (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="239f2-103">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>

<span data-ttu-id="239f2-104">El elemento **ItemIds** contiene una matriz de identificadores de elementos que identifican los elementos que se van a exportar desde un buzón.</span><span class="sxs-lookup"><span data-stu-id="239f2-104">The **ItemIds** element contains an array of item identifiers that identify the items to export from a mailbox.</span></span> 
  
[<span data-ttu-id="239f2-105">ExportItems</span><span class="sxs-lookup"><span data-stu-id="239f2-105">ExportItems</span></span>](exportitems.md)
  
[<span data-ttu-id="239f2-106">ItemIds (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="239f2-106">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md)
  
```XML
<ItemIds>
   <ItemId/>
</ItemIds>
```

 <span data-ttu-id="239f2-107">**NonEmptyArrayOfItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="239f2-107">**NonEmptyArrayOfItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="239f2-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="239f2-108">Attributes and elements</span></span>

<span data-ttu-id="239f2-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="239f2-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="239f2-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="239f2-110">Attributes</span></span>

<span data-ttu-id="239f2-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="239f2-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="239f2-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="239f2-112">Child elements</span></span>

|<span data-ttu-id="239f2-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="239f2-113">**Element**</span></span>|<span data-ttu-id="239f2-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="239f2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="239f2-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="239f2-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="239f2-116">Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="239f2-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="239f2-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="239f2-117">Parent elements</span></span>

|<span data-ttu-id="239f2-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="239f2-118">**Element**</span></span>|<span data-ttu-id="239f2-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="239f2-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="239f2-120">ExportItems</span><span class="sxs-lookup"><span data-stu-id="239f2-120">ExportItems</span></span>](exportitems.md) <br/> |<span data-ttu-id="239f2-121">Representa una solicitud para exportar elementos de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="239f2-121">Represents a request to export items from a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="239f2-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="239f2-122">Text value</span></span>

<span data-ttu-id="239f2-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="239f2-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="239f2-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="239f2-124">Remarks</span></span>

<span data-ttu-id="239f2-125">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="239f2-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="239f2-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="239f2-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="239f2-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="239f2-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="239f2-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="239f2-128">Schema Name</span></span>  <br/> |<span data-ttu-id="239f2-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="239f2-129">Message schema</span></span>  <br/> |
|<span data-ttu-id="239f2-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="239f2-130">Validation File</span></span>  <br/> |<span data-ttu-id="239f2-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="239f2-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="239f2-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="239f2-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="239f2-133">Falso</span><span class="sxs-lookup"><span data-stu-id="239f2-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="239f2-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="239f2-134">See also</span></span>



[<span data-ttu-id="239f2-135">Operación ExportItems</span><span class="sxs-lookup"><span data-stu-id="239f2-135">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="239f2-136">Operación UploadItems</span><span class="sxs-lookup"><span data-stu-id="239f2-136">UploadItems operation</span></span>](uploaditems-operation.md)

