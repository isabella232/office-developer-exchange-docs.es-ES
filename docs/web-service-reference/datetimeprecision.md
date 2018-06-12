---
title: DateTimePrecision
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 822dc5a6-2d57-474b-8a7d-da150898e5b6
description: El elemento DateTimePrecision especifica la precisión para valores de fecha y hora devuelto.
ms.openlocfilehash: 4d11598628228b41adf021adbbaa77e6348534bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764034"
---
# <a name="datetimeprecision"></a><span data-ttu-id="b196e-103">DateTimePrecision</span><span class="sxs-lookup"><span data-stu-id="b196e-103">DateTimePrecision</span></span>

<span data-ttu-id="b196e-104">El elemento **DateTimePrecision** especifica la precisión para valores de fecha y hora devuelto.</span><span class="sxs-lookup"><span data-stu-id="b196e-104">The **DateTimePrecision** element specifies the precision for returned date/time values.</span></span> 
  
```XML
<DateTimePrecision />
```

<span data-ttu-id="b196e-105">**DateTimePrecisionType**</span><span class="sxs-lookup"><span data-stu-id="b196e-105">**DateTimePrecisionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b196e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b196e-106">Attributes and elements</span></span>

<span data-ttu-id="b196e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b196e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b196e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b196e-108">Attributes</span></span>

<span data-ttu-id="b196e-109">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b196e-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b196e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b196e-110">Child elements</span></span>

<span data-ttu-id="b196e-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b196e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b196e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b196e-112">Parent elements</span></span>

<span data-ttu-id="b196e-113">El elemento **DateTimePrecision** se encuentra en el encabezado SOAP.</span><span class="sxs-lookup"><span data-stu-id="b196e-113">The **DateTimePrecision** element is located in the SOAP header.</span></span> 
  
## <a name="text-value"></a><span data-ttu-id="b196e-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b196e-114">Text value</span></span>

<span data-ttu-id="b196e-115">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="b196e-115">A text value is required.</span></span> <span data-ttu-id="b196e-116">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="b196e-116">The following are the possible values:</span></span>
  
- <span data-ttu-id="b196e-117">Segundos</span><span class="sxs-lookup"><span data-stu-id="b196e-117">Seconds</span></span>
    
- <span data-ttu-id="b196e-118">Milisegundos</span><span class="sxs-lookup"><span data-stu-id="b196e-118">Milliseconds</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b196e-119">Notas</span><span class="sxs-lookup"><span data-stu-id="b196e-119">Remarks</span></span>

<span data-ttu-id="b196e-120">Fecha y hora cuando se usa un encabezado SOAP con el elemento **DateTimePrecision** establecido en "Segundos", se devuelven valores a los más cercanos segundos (00: 00:00).</span><span class="sxs-lookup"><span data-stu-id="b196e-120">When a SOAP header with the **DateTimePrecision** element set to "Seconds" is used, date/time values are returned to the nearest seconds (00:00:00).</span></span> <span data-ttu-id="b196e-121">Fecha y hora cuando se usan "Milisegundos", se devuelven valores al milisegundo más próximo (00:00:00.0000).</span><span class="sxs-lookup"><span data-stu-id="b196e-121">When "Milliseconds" is used, date/time values are returned to the nearest millisecond (00:00:00.0000).</span></span> 
  
<span data-ttu-id="b196e-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b196e-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="b196e-123">Este elemento se introdujo en Exchange Server 2010 Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="b196e-123">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b196e-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b196e-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b196e-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b196e-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b196e-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b196e-126">Schema Name</span></span>  <br/> |<span data-ttu-id="b196e-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b196e-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="b196e-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b196e-128">Validation File</span></span>  <br/> |<span data-ttu-id="b196e-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b196e-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b196e-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b196e-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="b196e-131">False</span><span class="sxs-lookup"><span data-stu-id="b196e-131">False</span></span>  <br/> |
   

