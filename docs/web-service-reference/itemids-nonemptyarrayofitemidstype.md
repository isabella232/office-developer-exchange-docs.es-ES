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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468596"
---
# <a name="itemids-nonemptyarrayofitemidstype"></a><span data-ttu-id="80172-103">ItemIds (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="80172-103">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>

<span data-ttu-id="80172-104">El elemento **ItemIds** contiene una matriz de identificadores de elementos que identifican los elementos que se van a exportar desde un buzón.</span><span class="sxs-lookup"><span data-stu-id="80172-104">The **ItemIds** element contains an array of item identifiers that identify the items to export from a mailbox.</span></span> 
  
[<span data-ttu-id="80172-105">ExportItems</span><span class="sxs-lookup"><span data-stu-id="80172-105">ExportItems</span></span>](exportitems.md)
  
[<span data-ttu-id="80172-106">ItemIds (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="80172-106">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md)
  
```XML
<ItemIds>
   <ItemId/>
</ItemIds>
```

 <span data-ttu-id="80172-107">**NonEmptyArrayOfItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="80172-107">**NonEmptyArrayOfItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="80172-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="80172-108">Attributes and elements</span></span>

<span data-ttu-id="80172-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="80172-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80172-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="80172-110">Attributes</span></span>

<span data-ttu-id="80172-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="80172-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="80172-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="80172-112">Child elements</span></span>

|<span data-ttu-id="80172-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="80172-113">**Element**</span></span>|<span data-ttu-id="80172-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="80172-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="80172-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="80172-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="80172-116">Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="80172-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="80172-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="80172-117">Parent elements</span></span>

|<span data-ttu-id="80172-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="80172-118">**Element**</span></span>|<span data-ttu-id="80172-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="80172-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="80172-120">ExportItems</span><span class="sxs-lookup"><span data-stu-id="80172-120">ExportItems</span></span>](exportitems.md) <br/> |<span data-ttu-id="80172-121">Representa una solicitud para exportar elementos de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="80172-121">Represents a request to export items from a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="80172-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="80172-122">Text value</span></span>

<span data-ttu-id="80172-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="80172-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="80172-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="80172-124">Remarks</span></span>

<span data-ttu-id="80172-125">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="80172-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="80172-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="80172-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80172-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="80172-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="80172-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="80172-128">Schema Name</span></span>  <br/> |<span data-ttu-id="80172-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="80172-129">Message schema</span></span>  <br/> |
|<span data-ttu-id="80172-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="80172-130">Validation File</span></span>  <br/> |<span data-ttu-id="80172-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="80172-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="80172-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="80172-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="80172-133">Falso</span><span class="sxs-lookup"><span data-stu-id="80172-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80172-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="80172-134">See also</span></span>



[<span data-ttu-id="80172-135">Operación ExportItems</span><span class="sxs-lookup"><span data-stu-id="80172-135">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="80172-136">Operación UploadItems</span><span class="sxs-lookup"><span data-stu-id="80172-136">UploadItems operation</span></span>](uploaditems-operation.md)

