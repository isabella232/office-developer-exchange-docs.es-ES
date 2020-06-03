---
title: HasBlockedImages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ddeb11db-797d-4939-91d5-3e44be5f0778
description: El elemento HasBlockedImages especifica un valor booleano que indica si el elemento tiene imágenes bloqueadas.
ms.openlocfilehash: 370ab4b12ae841815faa344b2fd3a6d3ddc16bcb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462797"
---
# <a name="hasblockedimages"></a><span data-ttu-id="c3a08-103">HasBlockedImages</span><span class="sxs-lookup"><span data-stu-id="c3a08-103">HasBlockedImages</span></span>

<span data-ttu-id="c3a08-104">El elemento **HasBlockedImages** especifica un valor booleano que indica si el elemento tiene imágenes bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="c3a08-104">The **HasBlockedImages** element specifies a Boolean value that indicates whether the item has blocked images.</span></span> 
  
```XML
<HasBlockedImages> true | false </HasBlockedImages>
```

 <span data-ttu-id="c3a08-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c3a08-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c3a08-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c3a08-106">Attributes and elements</span></span>

<span data-ttu-id="c3a08-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c3a08-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c3a08-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c3a08-108">Attributes</span></span>

<span data-ttu-id="c3a08-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c3a08-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c3a08-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c3a08-110">Child elements</span></span>

<span data-ttu-id="c3a08-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c3a08-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c3a08-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c3a08-112">Parent elements</span></span>

|<span data-ttu-id="c3a08-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c3a08-113">**Element**</span></span>|<span data-ttu-id="c3a08-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c3a08-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c3a08-115">Item</span><span class="sxs-lookup"><span data-stu-id="c3a08-115">Item</span></span>](item.md) <br/> |<span data-ttu-id="c3a08-116">Representa un elemento genérico del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c3a08-116">Represents a generic item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c3a08-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c3a08-117">Text value</span></span>

<span data-ttu-id="c3a08-118">Un valor de texto de **true** para el elemento **HasBlockedImages** indica que el elemento tiene imágenes bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="c3a08-118">A text value of **true** for the **HasBlockedImages** element indicates that the item has blocked images.</span></span> <span data-ttu-id="c3a08-119">Un valor de **false** indica que el elemento no tiene ninguna imagen bloqueada.</span><span class="sxs-lookup"><span data-stu-id="c3a08-119">A value of **false** indicates that the item does not have any blocked images.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c3a08-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c3a08-120">Remarks</span></span>

<span data-ttu-id="c3a08-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c3a08-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c3a08-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c3a08-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c3a08-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c3a08-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3a08-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="c3a08-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c3a08-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c3a08-125">Schema Name</span></span>  <br/> |<span data-ttu-id="c3a08-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="c3a08-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="c3a08-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c3a08-127">Validation File</span></span>  <br/> |<span data-ttu-id="c3a08-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c3a08-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c3a08-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c3a08-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c3a08-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3a08-130">See also</span></span>



- [<span data-ttu-id="c3a08-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c3a08-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

