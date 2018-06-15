---
title: Direcciones (ArrayOfAddressesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 711acc90-8e5b-4658-92d2-16cd441db56e
description: El elemento de direcciones especifica una matriz de elementos de la dirección.
ms.openlocfilehash: c1ee79611da1d19ce85202f9e3c0f68c421e98c2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763419"
---
# <a name="addresses-arrayofaddressestype"></a><span data-ttu-id="34f27-103">Direcciones (ArrayOfAddressesType)</span><span class="sxs-lookup"><span data-stu-id="34f27-103">Addresses (ArrayOfAddressesType)</span></span>

<span data-ttu-id="34f27-104">El elemento de **direcciones** especifica una matriz de elementos de la **dirección** .</span><span class="sxs-lookup"><span data-stu-id="34f27-104">The **Addresses** element specifies an array of **Address** elements.</span></span> 
  
```XML
<Addresses>
    <Address></Address>
</Addresses>
```

 <span data-ttu-id="34f27-105">**ArrayOfAddressesType**</span><span class="sxs-lookup"><span data-stu-id="34f27-105">**ArrayOfAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="34f27-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="34f27-106">Attributes and elements</span></span>

<span data-ttu-id="34f27-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="34f27-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="34f27-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="34f27-108">Attributes</span></span>

<span data-ttu-id="34f27-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="34f27-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="34f27-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="34f27-110">Child elements</span></span>

|<span data-ttu-id="34f27-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="34f27-111">**Element**</span></span>|<span data-ttu-id="34f27-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="34f27-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="34f27-113">Dirección (ContactType)</span><span class="sxs-lookup"><span data-stu-id="34f27-113">Address (ContactType)</span></span>](address-contacttype.md) <br/> |<span data-ttu-id="34f27-114">Especifica la dirección de un contacto.</span><span class="sxs-lookup"><span data-stu-id="34f27-114">Specifies the address of a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="34f27-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="34f27-115">Parent elements</span></span>

|<span data-ttu-id="34f27-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="34f27-116">**Element**</span></span>|<span data-ttu-id="34f27-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="34f27-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="34f27-118">Contacto (ContactType)</span><span class="sxs-lookup"><span data-stu-id="34f27-118">Contact (ContactType)</span></span>](contact-contacttype.md) <br/> |<span data-ttu-id="34f27-119">Especifica un contacto en el almacén de contactos unificados.</span><span class="sxs-lookup"><span data-stu-id="34f27-119">Specifies a contact in the Unified Contact Store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34f27-120">Notas</span><span class="sxs-lookup"><span data-stu-id="34f27-120">Remarks</span></span>

<span data-ttu-id="34f27-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="34f27-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="34f27-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="34f27-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="34f27-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="34f27-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34f27-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="34f27-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="34f27-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="34f27-125">Schema Name</span></span>  <br/> |<span data-ttu-id="34f27-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="34f27-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="34f27-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="34f27-127">Validation File</span></span>  <br/> |<span data-ttu-id="34f27-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="34f27-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="34f27-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="34f27-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="34f27-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="34f27-130">See also</span></span>

- [<span data-ttu-id="34f27-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="34f27-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
