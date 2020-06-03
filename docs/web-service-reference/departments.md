---
title: Organismos
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0a6b0a4-f0dd-4945-af69-628da93f5452
description: El elemento departments especifica una matriz de nombres de departamento y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: 17590793e00a914cb53b479994bcc89e37bb0e31
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467938"
---
# <a name="departments"></a><span data-ttu-id="6942d-103">Organismos</span><span class="sxs-lookup"><span data-stu-id="6942d-103">Departments</span></span>

<span data-ttu-id="6942d-104">El **elemento** departments especifica una matriz de nombres de departamento y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="6942d-104">The **Departments** element specifies an array of department names and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Departments>
    <StringAttributedValue></StringAttributedValue>
</Departments>
```

 <span data-ttu-id="6942d-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="6942d-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6942d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6942d-106">Attributes and elements</span></span>

<span data-ttu-id="6942d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6942d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6942d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6942d-108">Attributes</span></span>

<span data-ttu-id="6942d-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6942d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6942d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6942d-110">Child elements</span></span>

|<span data-ttu-id="6942d-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6942d-111">**Element**</span></span>|<span data-ttu-id="6942d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6942d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6942d-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="6942d-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="6942d-114">Especifica una instancia de una matriz de atributos asociada a un elemento de rol.</span><span class="sxs-lookup"><span data-stu-id="6942d-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6942d-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6942d-115">Parent elements</span></span>

|<span data-ttu-id="6942d-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6942d-116">**Element**</span></span>|<span data-ttu-id="6942d-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6942d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6942d-118">Rol</span><span class="sxs-lookup"><span data-stu-id="6942d-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="6942d-119">Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="6942d-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6942d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6942d-120">Remarks</span></span>

<span data-ttu-id="6942d-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6942d-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6942d-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6942d-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6942d-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6942d-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6942d-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="6942d-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6942d-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6942d-125">Schema Name</span></span>  <br/> |<span data-ttu-id="6942d-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="6942d-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="6942d-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6942d-127">Validation File</span></span>  <br/> |<span data-ttu-id="6942d-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6942d-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="6942d-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6942d-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="6942d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6942d-130">See also</span></span>

- [<span data-ttu-id="6942d-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6942d-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

