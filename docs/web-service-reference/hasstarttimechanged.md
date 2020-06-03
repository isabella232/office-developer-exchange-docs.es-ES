---
title: HasStartTimeChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 04a6968d-7fb5-47ee-b66e-dc99c35dbb63
description: El elemento HasStartTimeChanged especifica si la hora de inicio de una reunión ha cambiado.
ms.openlocfilehash: 1355917005d956d05064bfc095055fb72aa16c57
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462748"
---
# <a name="hasstarttimechanged"></a><span data-ttu-id="7644b-103">HasStartTimeChanged</span><span class="sxs-lookup"><span data-stu-id="7644b-103">HasStartTimeChanged</span></span>

<span data-ttu-id="7644b-104">El elemento **HasStartTimeChanged** especifica si la hora de inicio de una reunión ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="7644b-104">The **HasStartTimeChanged** element specifies whether the start time for a meeting has changed.</span></span> 
  
```XML
<HasStartTimeChanged> true | false </HasStartTimeChanged>
```

 <span data-ttu-id="7644b-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7644b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7644b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7644b-106">Attributes and elements</span></span>

<span data-ttu-id="7644b-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7644b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7644b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7644b-108">Attributes</span></span>

<span data-ttu-id="7644b-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7644b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7644b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7644b-110">Child elements</span></span>

<span data-ttu-id="7644b-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7644b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7644b-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7644b-112">Parent elements</span></span>

|<span data-ttu-id="7644b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7644b-113">**Element**</span></span>|<span data-ttu-id="7644b-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7644b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7644b-115">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="7644b-115">ChangeHighlights</span></span>](changehighlights.md) <br/> |<span data-ttu-id="7644b-116">Especifica qué ha cambiado entre dos versiones de un mensaje de convocatoria de reunión.</span><span class="sxs-lookup"><span data-stu-id="7644b-116">Specifies what has changed between two versions of a meeting request message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7644b-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7644b-117">Text value</span></span>

<span data-ttu-id="7644b-118">Un valor de texto de **true** para el elemento **HasStartTimeChanged** indica que la hora de inicio de una reunión ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="7644b-118">A text value of **true** for the **HasStartTimeChanged** element indicates that the start time for a meeting has changed.</span></span> <span data-ttu-id="7644b-119">Un valor de **false** indica que la hora de inicio no ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="7644b-119">A value of **false** indicates that the start time has not changed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7644b-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7644b-120">Remarks</span></span>

<span data-ttu-id="7644b-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7644b-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7644b-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7644b-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7644b-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7644b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7644b-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="7644b-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7644b-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7644b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="7644b-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="7644b-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="7644b-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7644b-127">Validation File</span></span>  <br/> |<span data-ttu-id="7644b-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="7644b-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="7644b-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7644b-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="7644b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="7644b-130">See also</span></span>



- [<span data-ttu-id="7644b-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7644b-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

