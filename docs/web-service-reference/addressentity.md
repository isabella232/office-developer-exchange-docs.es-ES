---
title: AddressEntity
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ead22eab-f1e7-48b4-a165-db0e49fe86a8
description: El elemento AddressEntity especifica una entidad única dirección.
ms.openlocfilehash: 6a46a64c9824efdd8df6a08fe1a159e7e42b3731
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763424"
---
# <a name="addressentity"></a><span data-ttu-id="2a0f3-103">AddressEntity</span><span class="sxs-lookup"><span data-stu-id="2a0f3-103">AddressEntity</span></span>

<span data-ttu-id="2a0f3-104">El elemento **AddressEntity** especifica una entidad única dirección.</span><span class="sxs-lookup"><span data-stu-id="2a0f3-104">The **AddressEntity** element specifies a single address entity.</span></span> 
  
```XML
<AddressEntity>
    <Address></Address>
    <Position></Position>
</AddressEntity>
```

 <span data-ttu-id="2a0f3-105">**AddressEntityType**</span><span class="sxs-lookup"><span data-stu-id="2a0f3-105">**AddressEntityType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2a0f3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2a0f3-106">Attributes and elements</span></span>

<span data-ttu-id="2a0f3-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2a0f3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a0f3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2a0f3-108">Attributes</span></span>

<span data-ttu-id="2a0f3-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2a0f3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2a0f3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2a0f3-110">Child elements</span></span>

|<span data-ttu-id="2a0f3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="2a0f3-111">**Element**</span></span>|<span data-ttu-id="2a0f3-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a0f3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a0f3-113">Dirección (cadena)</span><span class="sxs-lookup"><span data-stu-id="2a0f3-113">Address (string)</span></span>](address-string.md) <br/> |<span data-ttu-id="2a0f3-114">Especifica una dirección.</span><span class="sxs-lookup"><span data-stu-id="2a0f3-114">Specifies an address.</span></span>  <br/> |
|[<span data-ttu-id="2a0f3-115">Position</span><span class="sxs-lookup"><span data-stu-id="2a0f3-115">Position</span></span>](position.md) <br/> |<span data-ttu-id="2a0f3-116">Especifica la posición en un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="2a0f3-116">Specifies the position in an email message.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2a0f3-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2a0f3-117">Parent elements</span></span>

|<span data-ttu-id="2a0f3-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="2a0f3-118">**Element**</span></span>|<span data-ttu-id="2a0f3-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a0f3-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a0f3-120">Direcciones (ArrayOfAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="2a0f3-120">Addresses (ArrayOfAddressEntitiesType)</span></span>](addresses-arrayofaddressentitiestype.md) <br/> |<span data-ttu-id="2a0f3-121">Especifica una matriz de elementos de **AddressEntity** .</span><span class="sxs-lookup"><span data-stu-id="2a0f3-121">Specifies an array of **AddressEntity** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2a0f3-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2a0f3-122">Text value</span></span>

<span data-ttu-id="2a0f3-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2a0f3-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2a0f3-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2a0f3-124">Remarks</span></span>

<span data-ttu-id="2a0f3-125">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2a0f3-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2a0f3-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2a0f3-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a0f3-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2a0f3-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a0f3-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2a0f3-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2a0f3-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2a0f3-129">Schema Name</span></span>  <br/> |<span data-ttu-id="2a0f3-130">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="2a0f3-130">Type schema</span></span>  <br/> |
|<span data-ttu-id="2a0f3-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2a0f3-131">Validation File</span></span>  <br/> |<span data-ttu-id="2a0f3-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2a0f3-132">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2a0f3-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2a0f3-133">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2a0f3-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a0f3-134">See also</span></span>

- [<span data-ttu-id="2a0f3-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="2a0f3-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

