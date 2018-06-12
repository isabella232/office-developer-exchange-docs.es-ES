---
title: ItemId (NonEmptyArrayOfItemIdsType)
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
description: El elemento ItemId contiene una matriz de identificadores de elemento que identifican los elementos que desee exportar desde un buzón de correo.
ms.openlocfilehash: c6d48832c5435080c7cec8e43093ea60825b604a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836151"
---
# <a name="itemids-nonemptyarrayofitemidstype"></a><span data-ttu-id="a8e92-103">ItemId (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="a8e92-103">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>

<span data-ttu-id="a8e92-104">El elemento **ItemID** contiene una matriz de identificadores de elemento que identifican los elementos que desee exportar desde un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a8e92-104">The **ItemIds** element contains an array of item identifiers that identify the items to export from a mailbox.</span></span> 
  
[<span data-ttu-id="a8e92-105">ExportItems</span><span class="sxs-lookup"><span data-stu-id="a8e92-105">ExportItems</span></span>](exportitems.md)
  
[<span data-ttu-id="a8e92-106">ItemId (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="a8e92-106">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md)
  
```XML
<ItemIds>
   <ItemId/>
</ItemIds>
```

 <span data-ttu-id="a8e92-107">**NonEmptyArrayOfItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="a8e92-107">**NonEmptyArrayOfItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a8e92-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a8e92-108">Attributes and elements</span></span>

<span data-ttu-id="a8e92-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a8e92-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8e92-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="a8e92-110">Attributes</span></span>

<span data-ttu-id="a8e92-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a8e92-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a8e92-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a8e92-112">Child elements</span></span>

|<span data-ttu-id="a8e92-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a8e92-113">**Element**</span></span>|<span data-ttu-id="a8e92-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a8e92-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8e92-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="a8e92-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="a8e92-116">Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a8e92-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a8e92-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a8e92-117">Parent elements</span></span>

|<span data-ttu-id="a8e92-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="a8e92-118">**Element**</span></span>|<span data-ttu-id="a8e92-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a8e92-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8e92-120">ExportItems</span><span class="sxs-lookup"><span data-stu-id="a8e92-120">ExportItems</span></span>](exportitems.md) <br/> |<span data-ttu-id="a8e92-121">Representa una solicitud para exportar elementos de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="a8e92-121">Represents a request to export items from a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a8e92-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a8e92-122">Text value</span></span>

<span data-ttu-id="a8e92-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a8e92-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8e92-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8e92-124">Remarks</span></span>

<span data-ttu-id="a8e92-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a8e92-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a8e92-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a8e92-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8e92-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a8e92-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a8e92-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a8e92-128">Schema Name</span></span>  <br/> |<span data-ttu-id="a8e92-129">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="a8e92-129">Message schema</span></span>  <br/> |
|<span data-ttu-id="a8e92-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a8e92-130">Validation File</span></span>  <br/> |<span data-ttu-id="a8e92-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a8e92-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a8e92-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a8e92-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="a8e92-133">False</span><span class="sxs-lookup"><span data-stu-id="a8e92-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8e92-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="a8e92-134">See also</span></span>



[<span data-ttu-id="a8e92-135">Operación ExportItems</span><span class="sxs-lookup"><span data-stu-id="a8e92-135">ExportItems operation</span></span>](exportitems-operation.md)
  
[<span data-ttu-id="a8e92-136">Operación UploadItems</span><span class="sxs-lookup"><span data-stu-id="a8e92-136">UploadItems operation</span></span>](uploaditems-operation.md)

