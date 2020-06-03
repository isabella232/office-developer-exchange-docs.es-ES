---
title: FileAses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f81efc37-bb70-4d52-a614-cec87d1b0f04
description: El elemento FileAses especifica una matriz de elementos StringAttributedValue y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: 9d97c2c7210e9ae20326d7327c9de4159d5df5a6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461082"
---
# <a name="fileases"></a><span data-ttu-id="b1032-103">FileAses</span><span class="sxs-lookup"><span data-stu-id="b1032-103">FileAses</span></span>

<span data-ttu-id="b1032-104">El elemento **FileAses** especifica una matriz de elementos **StringAttributedValue** y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="b1032-104">The **FileAses** element specifies an array of **StringAttributedValue** elements and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<FileAses>
    <StringAttributedValue/>
</FileAses>
```

 <span data-ttu-id="b1032-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="b1032-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b1032-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b1032-106">Attributes and elements</span></span>

<span data-ttu-id="b1032-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b1032-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1032-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b1032-108">Attributes</span></span>

<span data-ttu-id="b1032-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b1032-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b1032-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b1032-110">Child elements</span></span>

|<span data-ttu-id="b1032-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b1032-111">**Element**</span></span>|<span data-ttu-id="b1032-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b1032-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1032-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="b1032-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="b1032-114">Especifica una instancia de una matriz de atributos asociada a un elemento de rol.</span><span class="sxs-lookup"><span data-stu-id="b1032-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b1032-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b1032-115">Parent elements</span></span>

|<span data-ttu-id="b1032-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b1032-116">**Element**</span></span>|<span data-ttu-id="b1032-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b1032-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1032-118">Rol</span><span class="sxs-lookup"><span data-stu-id="b1032-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="b1032-119">Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="b1032-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1032-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b1032-120">Remarks</span></span>

<span data-ttu-id="b1032-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b1032-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b1032-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b1032-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b1032-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b1032-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1032-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1032-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b1032-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b1032-125">Schema Name</span></span>  <br/> |<span data-ttu-id="b1032-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="b1032-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="b1032-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b1032-127">Validation File</span></span>  <br/> |<span data-ttu-id="b1032-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="b1032-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="b1032-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b1032-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="b1032-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1032-130">See also</span></span>



- [<span data-ttu-id="b1032-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b1032-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

