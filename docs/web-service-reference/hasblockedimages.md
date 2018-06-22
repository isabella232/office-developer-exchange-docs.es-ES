---
title: HasBlockedImages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ddeb11db-797d-4939-91d5-3e44be5f0778
description: El elemento HasBlockedImages especifica un valor booleano que indica si el elemento ha bloqueado las imágenes.
ms.openlocfilehash: fbe9967c898016aeef27e3c86e8a1cf603bd87fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835795"
---
# <a name="hasblockedimages"></a><span data-ttu-id="fa563-103">HasBlockedImages</span><span class="sxs-lookup"><span data-stu-id="fa563-103">HasBlockedImages</span></span>

<span data-ttu-id="fa563-104">El elemento **HasBlockedImages** especifica un valor booleano que indica si el elemento ha bloqueado las imágenes.</span><span class="sxs-lookup"><span data-stu-id="fa563-104">The **HasBlockedImages** element specifies a Boolean value that indicates whether the item has blocked images.</span></span> 
  
```XML
<HasBlockedImages> true | false </HasBlockedImages>
```

 <span data-ttu-id="fa563-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fa563-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa563-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fa563-106">Attributes and elements</span></span>

<span data-ttu-id="fa563-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fa563-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa563-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fa563-108">Attributes</span></span>

<span data-ttu-id="fa563-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fa563-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa563-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fa563-110">Child elements</span></span>

<span data-ttu-id="fa563-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="fa563-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fa563-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fa563-112">Parent elements</span></span>

|<span data-ttu-id="fa563-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="fa563-113">**Element**</span></span>|<span data-ttu-id="fa563-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa563-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa563-115">Item</span><span class="sxs-lookup"><span data-stu-id="fa563-115">Item</span></span>](item.md) <br/> |<span data-ttu-id="fa563-116">Representa un elemento genérico en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="fa563-116">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fa563-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fa563-117">Text value</span></span>

<span data-ttu-id="fa563-118">Un valor de texto de **true** para el elemento **HasBlockedImages** indica que el elemento ha bloqueado las imágenes.</span><span class="sxs-lookup"><span data-stu-id="fa563-118">A text value of **true** for the **HasBlockedImages** element indicates that the item has blocked images.</span></span> <span data-ttu-id="fa563-119">Un valor de **false** indica que el elemento no tiene ningún imágenes bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="fa563-119">A value of **false** indicates that the item does not have any blocked images.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fa563-120">Notas</span><span class="sxs-lookup"><span data-stu-id="fa563-120">Remarks</span></span>

<span data-ttu-id="fa563-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fa563-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fa563-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fa563-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa563-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fa563-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa563-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fa563-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa563-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fa563-125">Schema Name</span></span>  <br/> |<span data-ttu-id="fa563-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="fa563-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="fa563-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fa563-127">Validation File</span></span>  <br/> |<span data-ttu-id="fa563-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fa563-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa563-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fa563-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="fa563-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="fa563-130">See also</span></span>



- [<span data-ttu-id="fa563-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="fa563-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

