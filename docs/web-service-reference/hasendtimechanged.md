---
title: HasEndTimeChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0eb444d-8e2e-478b-b785-2b9787ffb226
description: El elemento HasEndTimeChanged especifica si ha cambiado la hora de finalización de una reunión.
ms.openlocfilehash: 15ad52c7b7581cce5ca96ba5ff4e8a1c130a02cf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461789"
---
# <a name="hasendtimechanged"></a><span data-ttu-id="fc935-103">HasEndTimeChanged</span><span class="sxs-lookup"><span data-stu-id="fc935-103">HasEndTimeChanged</span></span>

<span data-ttu-id="fc935-104">El elemento **HasEndTimeChanged** especifica si ha cambiado la hora de finalización de una reunión.</span><span class="sxs-lookup"><span data-stu-id="fc935-104">The **HasEndTimeChanged** element specifies whether the end time for a meeting has changed.</span></span> 
  
```XML
<HasEndTimeChanged>true | false</HasEndTimeChanged>
```

 <span data-ttu-id="fc935-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fc935-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fc935-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fc935-106">Attributes and elements</span></span>

<span data-ttu-id="fc935-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fc935-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fc935-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fc935-108">Attributes</span></span>

<span data-ttu-id="fc935-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fc935-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fc935-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fc935-110">Child elements</span></span>

<span data-ttu-id="fc935-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fc935-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fc935-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fc935-112">Parent elements</span></span>

|<span data-ttu-id="fc935-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fc935-113">**Element**</span></span>|<span data-ttu-id="fc935-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fc935-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc935-115">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="fc935-115">ChangeHighlights</span></span>](changehighlights.md) <br/> |<span data-ttu-id="fc935-116">Especifica qué ha cambiado entre dos versiones de un mensaje de convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="fc935-116">Specifies what has changed between two versions of a meeting request message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fc935-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fc935-117">Text value</span></span>

<span data-ttu-id="fc935-118">Un valor de texto de **true** para el elemento **HasEndTimeChanged** indica que la hora de finalización de una reunión ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="fc935-118">A text value of **true** for the **HasEndTimeChanged** element indicates that the end time of a meeting has changed.</span></span> <span data-ttu-id="fc935-119">Un valor de **false** indica que la hora de finalización de una reunión no ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="fc935-119">A value of **false** indicates that the end time of a meeting has not changed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fc935-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fc935-120">Remarks</span></span>

<span data-ttu-id="fc935-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="fc935-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fc935-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fc935-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fc935-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fc935-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc935-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="fc935-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fc935-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fc935-125">Schema Name</span></span>  <br/> |<span data-ttu-id="fc935-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="fc935-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="fc935-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fc935-127">Validation File</span></span>  <br/> |<span data-ttu-id="fc935-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="fc935-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="fc935-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fc935-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="fc935-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc935-130">See also</span></span>



- [<span data-ttu-id="fc935-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fc935-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

