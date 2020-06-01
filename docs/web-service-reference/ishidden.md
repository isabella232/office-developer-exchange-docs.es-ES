---
title: IsHidden
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2377b584-bd1e-49fc-b80a-a6634721a297
description: El elemento IsHidden contiene un valor booleano que indica si el contacto subyacente se debe ocultar o mostrar como parte del rol.
ms.openlocfilehash: a22628e9ab4a46de04fe395f2d6c1b70083a5c77
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464241"
---
# <a name="ishidden"></a><span data-ttu-id="0852e-103">IsHidden</span><span class="sxs-lookup"><span data-stu-id="0852e-103">IsHidden</span></span>

<span data-ttu-id="0852e-104">El elemento **IsHidden** contiene un valor booleano que indica si el contacto subyacente se debe ocultar o mostrar como parte del rol.</span><span class="sxs-lookup"><span data-stu-id="0852e-104">The **IsHidden** element contains a Boolean value that indicates whether the underlying contact should be hidden or displayed as part of the persona.</span></span> 
  
```XML
<IsHidden>true | false</IsHidden>
```

 <span data-ttu-id="0852e-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0852e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0852e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0852e-106">Attributes and elements</span></span>

<span data-ttu-id="0852e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0852e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0852e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0852e-108">Attributes</span></span>

<span data-ttu-id="0852e-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0852e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0852e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0852e-110">Child elements</span></span>

<span data-ttu-id="0852e-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0852e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0852e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0852e-112">Parent elements</span></span>

|<span data-ttu-id="0852e-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0852e-113">**Element**</span></span>|<span data-ttu-id="0852e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0852e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0852e-115">Atribución (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="0852e-115">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md) <br/> |<span data-ttu-id="0852e-116">Especifica una instancia de una matriz de atributos para un elemento de **rol** .</span><span class="sxs-lookup"><span data-stu-id="0852e-116">Specifies an instance in an array of attributes for a **Persona** element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0852e-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0852e-117">Text value</span></span>

<span data-ttu-id="0852e-118">Un valor de texto de **true** para el elemento **IsHidden** indica que el contacto subyacente se debe ocultar o mostrar como parte del rol.</span><span class="sxs-lookup"><span data-stu-id="0852e-118">A text value of **true** for the **IsHidden** element indicates that the underlying contact should be hidden or displayed as part of the persona.</span></span> <span data-ttu-id="0852e-119">Un valor de **false** indica que el contacto subyacente no se debe ocultar ni mostrar como parte del rol.</span><span class="sxs-lookup"><span data-stu-id="0852e-119">A value of **false** indicates that the underlying contact should not be hidden or displayed as part of the persona.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0852e-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0852e-120">Remarks</span></span>

<span data-ttu-id="0852e-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0852e-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0852e-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0852e-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0852e-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0852e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0852e-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="0852e-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0852e-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0852e-125">Schema Name</span></span>  <br/> |<span data-ttu-id="0852e-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="0852e-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="0852e-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0852e-127">Validation File</span></span>  <br/> |<span data-ttu-id="0852e-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="0852e-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="0852e-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0852e-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0852e-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="0852e-130">See also</span></span>



- [<span data-ttu-id="0852e-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0852e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

