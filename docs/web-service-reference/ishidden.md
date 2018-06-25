---
title: IsHidden
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2377b584-bd1e-49fc-b80a-a6634721a297
description: El elemento IsHidden contiene un valor booleano que indica si el contacto subyacente debe ser oculto o que se muestra como parte del rol.
ms.openlocfilehash: ee20bf0af287e3cddaedb5bc6d3c63ef9a7a7006
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836032"
---
# <a name="ishidden"></a><span data-ttu-id="97754-103">IsHidden</span><span class="sxs-lookup"><span data-stu-id="97754-103">IsHidden</span></span>

<span data-ttu-id="97754-104">El elemento **IsHidden** contiene un valor booleano que indica si el contacto subyacente debe ser oculto o que se muestra como parte del rol.</span><span class="sxs-lookup"><span data-stu-id="97754-104">The **IsHidden** element contains a Boolean value that indicates whether the underlying contact should be hidden or displayed as part of the persona.</span></span> 
  
```XML
<IsHidden>true | false</IsHidden>
```

 <span data-ttu-id="97754-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="97754-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="97754-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="97754-106">Attributes and elements</span></span>

<span data-ttu-id="97754-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="97754-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="97754-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="97754-108">Attributes</span></span>

<span data-ttu-id="97754-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="97754-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="97754-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="97754-110">Child elements</span></span>

<span data-ttu-id="97754-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="97754-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="97754-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="97754-112">Parent elements</span></span>

|<span data-ttu-id="97754-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="97754-113">**Element**</span></span>|<span data-ttu-id="97754-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="97754-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="97754-115">Atribución (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="97754-115">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md) <br/> |<span data-ttu-id="97754-116">Especifica una instancia de una matriz de atributos de un elemento de la **Persona** .</span><span class="sxs-lookup"><span data-stu-id="97754-116">Specifies an instance in an array of attributes for a **Persona** element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="97754-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="97754-117">Text value</span></span>

<span data-ttu-id="97754-118">Un valor de texto de **true** para el elemento **IsHidden** indica que el contacto subyacente debe ser oculto o que se muestra como parte del rol.</span><span class="sxs-lookup"><span data-stu-id="97754-118">A text value of **true** for the **IsHidden** element indicates that the underlying contact should be hidden or displayed as part of the persona.</span></span> <span data-ttu-id="97754-119">Un valor de **false** indica que el contacto subyacente no se oculta o se muestran como parte de la persona.</span><span class="sxs-lookup"><span data-stu-id="97754-119">A value of **false** indicates that the underlying contact should not be hidden or displayed as part of the persona.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="97754-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="97754-120">Remarks</span></span>

<span data-ttu-id="97754-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="97754-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="97754-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="97754-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="97754-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="97754-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="97754-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="97754-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="97754-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="97754-125">Schema Name</span></span>  <br/> |<span data-ttu-id="97754-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="97754-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="97754-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="97754-127">Validation File</span></span>  <br/> |<span data-ttu-id="97754-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="97754-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="97754-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="97754-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="97754-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="97754-130">See also</span></span>



- [<span data-ttu-id="97754-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="97754-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

