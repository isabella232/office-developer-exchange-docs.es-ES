---
title: GivenNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 64d86c24-07b8-448d-ad37-47f104777df3
description: El elemento GivenNames especifica una matriz de valores de nombre dados y los identificadores de sus atribuciones de origen para el rol asociado.
ms.openlocfilehash: c76d69344b59fb56377a13b9ea4a588acc382013
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530130"
---
# <a name="givennames"></a><span data-ttu-id="072be-103">GivenNames</span><span class="sxs-lookup"><span data-stu-id="072be-103">GivenNames</span></span>

<span data-ttu-id="072be-104">El elemento **GivenNames** especifica una matriz de valores de nombre dados y los identificadores de sus atribuciones de origen para el rol asociado.</span><span class="sxs-lookup"><span data-stu-id="072be-104">The **GivenNames** element specifies an array of given name values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```xml
<GivenNames>
    <StringAttributedValue/>
</GivenNames>
```

 <span data-ttu-id="072be-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="072be-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="072be-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="072be-106">Attributes and elements</span></span>

<span data-ttu-id="072be-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="072be-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="072be-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="072be-108">Attributes</span></span>

<span data-ttu-id="072be-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="072be-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="072be-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="072be-110">Child elements</span></span>

|<span data-ttu-id="072be-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="072be-111">**Element**</span></span>|<span data-ttu-id="072be-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="072be-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="072be-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="072be-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="072be-114">Especifica una instancia de una matriz de atributos asociada a un elemento de rol.</span><span class="sxs-lookup"><span data-stu-id="072be-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="072be-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="072be-115">Parent elements</span></span>

|<span data-ttu-id="072be-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="072be-116">**Element**</span></span>|<span data-ttu-id="072be-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="072be-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="072be-118">Rol</span><span class="sxs-lookup"><span data-stu-id="072be-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="072be-119">Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="072be-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="072be-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="072be-120">Remarks</span></span>

<span data-ttu-id="072be-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="072be-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="072be-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="072be-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="072be-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="072be-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="072be-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="072be-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="072be-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="072be-125">Schema Name</span></span>  <br/> |<span data-ttu-id="072be-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="072be-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="072be-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="072be-127">Validation File</span></span>  <br/> |<span data-ttu-id="072be-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="072be-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="072be-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="072be-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="072be-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="072be-130">See also</span></span>



- [<span data-ttu-id="072be-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="072be-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

