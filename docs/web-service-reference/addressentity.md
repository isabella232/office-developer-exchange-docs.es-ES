---
title: AddressEntity
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ead22eab-f1e7-48b4-a165-db0e49fe86a8
description: El elemento AddressEntity especifica una única entidad de dirección.
ms.openlocfilehash: c597557fe02a9c0ff7ed3c9862e1662cfbae596a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466909"
---
# <a name="addressentity"></a><span data-ttu-id="7ca14-103">AddressEntity</span><span class="sxs-lookup"><span data-stu-id="7ca14-103">AddressEntity</span></span>

<span data-ttu-id="7ca14-104">El elemento **AddressEntity** especifica una única entidad de dirección.</span><span class="sxs-lookup"><span data-stu-id="7ca14-104">The **AddressEntity** element specifies a single address entity.</span></span> 
  
```XML
<AddressEntity>
    <Address></Address>
    <Position></Position>
</AddressEntity>
```

 <span data-ttu-id="7ca14-105">**AddressEntityType**</span><span class="sxs-lookup"><span data-stu-id="7ca14-105">**AddressEntityType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7ca14-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7ca14-106">Attributes and elements</span></span>

<span data-ttu-id="7ca14-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7ca14-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7ca14-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7ca14-108">Attributes</span></span>

<span data-ttu-id="7ca14-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7ca14-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7ca14-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7ca14-110">Child elements</span></span>

|<span data-ttu-id="7ca14-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7ca14-111">**Element**</span></span>|<span data-ttu-id="7ca14-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7ca14-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ca14-113">Address (cadena)</span><span class="sxs-lookup"><span data-stu-id="7ca14-113">Address (string)</span></span>](address-string.md) <br/> |<span data-ttu-id="7ca14-114">Especifica una dirección.</span><span class="sxs-lookup"><span data-stu-id="7ca14-114">Specifies an address.</span></span>  <br/> |
|[<span data-ttu-id="7ca14-115">Position</span><span class="sxs-lookup"><span data-stu-id="7ca14-115">Position</span></span>](position.md) <br/> |<span data-ttu-id="7ca14-116">Especifica la posición en un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="7ca14-116">Specifies the position in an email message.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7ca14-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7ca14-117">Parent elements</span></span>

|<span data-ttu-id="7ca14-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7ca14-118">**Element**</span></span>|<span data-ttu-id="7ca14-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7ca14-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7ca14-120">Direcciones (ArrayOfAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="7ca14-120">Addresses (ArrayOfAddressEntitiesType)</span></span>](addresses-arrayofaddressentitiestype.md) <br/> |<span data-ttu-id="7ca14-121">Especifica una matriz de elementos **AddressEntity** .</span><span class="sxs-lookup"><span data-stu-id="7ca14-121">Specifies an array of **AddressEntity** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7ca14-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7ca14-122">Text value</span></span>

<span data-ttu-id="7ca14-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7ca14-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7ca14-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7ca14-124">Remarks</span></span>

<span data-ttu-id="7ca14-125">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7ca14-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7ca14-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7ca14-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7ca14-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7ca14-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ca14-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="7ca14-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7ca14-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7ca14-129">Schema Name</span></span>  <br/> |<span data-ttu-id="7ca14-130">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="7ca14-130">Type schema</span></span>  <br/> |
|<span data-ttu-id="7ca14-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7ca14-131">Validation File</span></span>  <br/> |<span data-ttu-id="7ca14-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="7ca14-132">types.xsd</span></span>  <br/> |
|<span data-ttu-id="7ca14-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7ca14-133">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="7ca14-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ca14-134">See also</span></span>

- [<span data-ttu-id="7ca14-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7ca14-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

