---
title: DateTimePrecision
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 822dc5a6-2d57-474b-8a7d-da150898e5b6
description: El elemento DateTimePrecision especifica la precisión de los valores de fecha y hora devueltos.
ms.openlocfilehash: 9d245dfb0123daae42ba9b9b4e98aff872b67d80
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529227"
---
# <a name="datetimeprecision"></a><span data-ttu-id="fcd70-103">DateTimePrecision</span><span class="sxs-lookup"><span data-stu-id="fcd70-103">DateTimePrecision</span></span>

<span data-ttu-id="fcd70-104">El elemento **DateTimePrecision** especifica la precisión de los valores de fecha y hora devueltos.</span><span class="sxs-lookup"><span data-stu-id="fcd70-104">The **DateTimePrecision** element specifies the precision for returned date/time values.</span></span> 
  
```XML
<DateTimePrecision />
```

<span data-ttu-id="fcd70-105">**DateTimePrecisionType**</span><span class="sxs-lookup"><span data-stu-id="fcd70-105">**DateTimePrecisionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="fcd70-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fcd70-106">Attributes and elements</span></span>

<span data-ttu-id="fcd70-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fcd70-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fcd70-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fcd70-108">Attributes</span></span>

<span data-ttu-id="fcd70-109">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fcd70-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fcd70-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fcd70-110">Child elements</span></span>

<span data-ttu-id="fcd70-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fcd70-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fcd70-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fcd70-112">Parent elements</span></span>

<span data-ttu-id="fcd70-113">El elemento **DateTimePrecision** se encuentra en el encabezado SOAP.</span><span class="sxs-lookup"><span data-stu-id="fcd70-113">The **DateTimePrecision** element is located in the SOAP header.</span></span> 
  
## <a name="text-value"></a><span data-ttu-id="fcd70-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fcd70-114">Text value</span></span>

<span data-ttu-id="fcd70-115">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="fcd70-115">A text value is required.</span></span> <span data-ttu-id="fcd70-116">Los valores posibles son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="fcd70-116">The following are the possible values:</span></span>
  
- <span data-ttu-id="fcd70-117">Segundos</span><span class="sxs-lookup"><span data-stu-id="fcd70-117">Seconds</span></span>
    
- <span data-ttu-id="fcd70-118">Milisegundos</span><span class="sxs-lookup"><span data-stu-id="fcd70-118">Milliseconds</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fcd70-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fcd70-119">Remarks</span></span>

<span data-ttu-id="fcd70-120">Cuando se usa un encabezado SOAP con el elemento **DateTimePrecision** establecido en "seconds", los valores de fecha y hora se devuelven a los segundos más próximos (00:00:00).</span><span class="sxs-lookup"><span data-stu-id="fcd70-120">When a SOAP header with the **DateTimePrecision** element set to "Seconds" is used, date/time values are returned to the nearest seconds (00:00:00).</span></span> <span data-ttu-id="fcd70-121">Cuando se usa "Milliseconds", los valores de fecha y hora se devuelven al milisegundo más cercano (00:00:00.0000).</span><span class="sxs-lookup"><span data-stu-id="fcd70-121">When "Milliseconds" is used, date/time values are returned to the nearest millisecond (00:00:00.0000).</span></span> 
  
<span data-ttu-id="fcd70-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fcd70-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="fcd70-123">Este elemento se introdujo en Exchange Server 2010 Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="fcd70-123">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fcd70-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fcd70-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fcd70-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="fcd70-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fcd70-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fcd70-126">Schema Name</span></span>  <br/> |<span data-ttu-id="fcd70-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="fcd70-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="fcd70-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fcd70-128">Validation File</span></span>  <br/> |<span data-ttu-id="fcd70-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="fcd70-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fcd70-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fcd70-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="fcd70-131">Falso</span><span class="sxs-lookup"><span data-stu-id="fcd70-131">False</span></span>  <br/> |
   

