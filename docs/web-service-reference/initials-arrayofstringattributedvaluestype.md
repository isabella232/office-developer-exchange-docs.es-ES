---
title: Iniciales (ArrayOfStringAttributedValuesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 060c0cf1-c632-484c-87f5-f577017a7090
description: El elemento iniciales especifica una matriz de valores iniciales y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: 5b9fe4062bcc0d60de828ed6b0cb08faa45b5c19
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835926"
---
# <a name="initials-arrayofstringattributedvaluestype"></a><span data-ttu-id="7669d-103">Iniciales (ArrayOfStringAttributedValuesType)</span><span class="sxs-lookup"><span data-stu-id="7669d-103">Initials (ArrayOfStringAttributedValuesType)</span></span>

<span data-ttu-id="7669d-104">El elemento **iniciales** especifica una matriz de valores iniciales y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="7669d-104">The **Initials** element specifies an array of initials values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Initials>
    <StringAttributedValue/>
</Initials>
```

 <span data-ttu-id="7669d-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="7669d-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7669d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7669d-106">Attributes and elements</span></span>

<span data-ttu-id="7669d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7669d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7669d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7669d-108">Attributes</span></span>

<span data-ttu-id="7669d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7669d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7669d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7669d-110">Child elements</span></span>

|<span data-ttu-id="7669d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7669d-111">**Element**</span></span>|<span data-ttu-id="7669d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7669d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7669d-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="7669d-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="7669d-114">Especifica una instancia de una matriz de atributos asociados con un elemento de la persona.</span><span class="sxs-lookup"><span data-stu-id="7669d-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7669d-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7669d-115">Parent elements</span></span>

|<span data-ttu-id="7669d-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="7669d-116">**Element**</span></span>|<span data-ttu-id="7669d-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7669d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7669d-118">Rol</span><span class="sxs-lookup"><span data-stu-id="7669d-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="7669d-119">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="7669d-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7669d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7669d-120">Remarks</span></span>

<span data-ttu-id="7669d-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7669d-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7669d-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7669d-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7669d-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7669d-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7669d-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7669d-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7669d-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7669d-125">Schema Name</span></span>  <br/> |<span data-ttu-id="7669d-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="7669d-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="7669d-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7669d-127">Validation File</span></span>  <br/> |<span data-ttu-id="7669d-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7669d-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="7669d-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7669d-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="7669d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="7669d-130">See also</span></span>



- [<span data-ttu-id="7669d-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7669d-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

