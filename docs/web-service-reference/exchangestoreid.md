---
title: ExchangeStoreId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5acceb42-a757-4c74-ab1c-b1abf7bf1e0a
description: El elemento ExchangeStoreId especifica el identificador de grupo (IM) de mensajería instantánea.
ms.openlocfilehash: 815e9c2f368558ea38efce3671dbdc33d4d97168
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764477"
---
# <a name="exchangestoreid"></a><span data-ttu-id="222c8-103">ExchangeStoreId</span><span class="sxs-lookup"><span data-stu-id="222c8-103">ExchangeStoreId</span></span>

<span data-ttu-id="222c8-104">El elemento **ExchangeStoreId** especifica el identificador de grupo (IM) de mensajería instantánea.</span><span class="sxs-lookup"><span data-stu-id="222c8-104">The **ExchangeStoreId** element specifies the instant messaging (IM) group identifier.</span></span> 
  
```XML
<ExchangeStoreId Id="" ChangeKey=""/>
```

 <span data-ttu-id="222c8-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="222c8-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="222c8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="222c8-106">Attributes and elements</span></span>

<span data-ttu-id="222c8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="222c8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="222c8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="222c8-108">Attributes</span></span>

|<span data-ttu-id="222c8-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="222c8-109">**Attribute**</span></span>|<span data-ttu-id="222c8-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="222c8-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="222c8-111">Id</span><span class="sxs-lookup"><span data-stu-id="222c8-111">Id</span></span>  <br/> |<span data-ttu-id="222c8-112">El valor de texto del atributo **Id** es el identificador del grupo.</span><span class="sxs-lookup"><span data-stu-id="222c8-112">The text value of the **Id** attribute is the identifier of the group.</span></span>  <br/> |
|<span data-ttu-id="222c8-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="222c8-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="222c8-114">El valor de texto del atributo **ChangeKey** es la clave de cambio del grupo.</span><span class="sxs-lookup"><span data-stu-id="222c8-114">The text value of the **ChangeKey** attribute is the change key of the group.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="222c8-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="222c8-115">Child elements</span></span>

<span data-ttu-id="222c8-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="222c8-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="222c8-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="222c8-117">Parent elements</span></span>

|<span data-ttu-id="222c8-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="222c8-118">**Element**</span></span>|<span data-ttu-id="222c8-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="222c8-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="222c8-120">ImGroup</span><span class="sxs-lookup"><span data-stu-id="222c8-120">ImGroup</span></span>](imgroup.md) <br/> |<span data-ttu-id="222c8-121">Representa un grupo de mensajería instantáneo.</span><span class="sxs-lookup"><span data-stu-id="222c8-121">Represents an instant messaging group.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="222c8-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="222c8-122">Remarks</span></span>

<span data-ttu-id="222c8-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="222c8-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="222c8-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="222c8-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="222c8-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="222c8-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="222c8-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="222c8-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="222c8-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="222c8-127">Schema Name</span></span>  <br/> |<span data-ttu-id="222c8-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="222c8-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="222c8-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="222c8-129">Validation File</span></span>  <br/> |<span data-ttu-id="222c8-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="222c8-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="222c8-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="222c8-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="222c8-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="222c8-132">See also</span></span>



- [<span data-ttu-id="222c8-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="222c8-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

