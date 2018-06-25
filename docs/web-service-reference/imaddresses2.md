---
title: ImAddresses2
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 328f29b9-3a9c-4d9a-a85f-5ffff84e266a
description: El elemento ImAddresses2 especifica una matriz de direcciones de mensajería instantánea y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: f61084f22eb9d38766c45e63dfbacc0882ccaaca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835870"
---
# <a name="imaddresses2"></a><span data-ttu-id="594b3-103">ImAddresses2</span><span class="sxs-lookup"><span data-stu-id="594b3-103">ImAddresses2</span></span>

<span data-ttu-id="594b3-104">El elemento **ImAddresses2** especifica una matriz de direcciones de mensajería instantánea y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="594b3-104">The **ImAddresses2** element specifies an array of instant message addresses and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<ImAddresses2>
    <StringAttributedValue/>
</ImAddresses2>
```

 <span data-ttu-id="594b3-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="594b3-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="594b3-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="594b3-106">Attributes and elements</span></span>

<span data-ttu-id="594b3-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="594b3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="594b3-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="594b3-108">Attributes</span></span>

<span data-ttu-id="594b3-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="594b3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="594b3-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="594b3-110">Child elements</span></span>

|<span data-ttu-id="594b3-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="594b3-111">**Element**</span></span>|<span data-ttu-id="594b3-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="594b3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="594b3-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="594b3-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="594b3-114">Especifica una instancia de una matriz de atributos asociados con un elemento de la persona.</span><span class="sxs-lookup"><span data-stu-id="594b3-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="594b3-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="594b3-115">Parent elements</span></span>

|<span data-ttu-id="594b3-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="594b3-116">**Element**</span></span>|<span data-ttu-id="594b3-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="594b3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="594b3-118">Rol</span><span class="sxs-lookup"><span data-stu-id="594b3-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="594b3-119">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="594b3-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="594b3-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="594b3-120">Remarks</span></span>

<span data-ttu-id="594b3-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="594b3-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="594b3-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="594b3-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="594b3-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="594b3-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="594b3-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="594b3-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="594b3-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="594b3-125">Schema Name</span></span>  <br/> |<span data-ttu-id="594b3-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="594b3-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="594b3-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="594b3-127">Validation File</span></span>  <br/> |<span data-ttu-id="594b3-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="594b3-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="594b3-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="594b3-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="594b3-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="594b3-130">See also</span></span>



- [<span data-ttu-id="594b3-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="594b3-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

