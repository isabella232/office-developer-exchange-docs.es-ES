---
title: NumberOfOccurrences
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NumberOfOccurrences
api_type:
- schema
ms.assetid: 9ec86ceb-b271-4718-97ca-b6a532ea7223
description: El elemento NumberOfOccurrences contiene el número de repeticiones de un elemento periódico.
ms.openlocfilehash: f9b72611e87c5f2b98deb14c25988e574a324491
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462545"
---
# <a name="numberofoccurrences"></a><span data-ttu-id="1bafe-103">NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="1bafe-103">NumberOfOccurrences</span></span>

<span data-ttu-id="1bafe-104">El elemento **NumberOfOccurrences** contiene el número de repeticiones de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="1bafe-104">The **NumberOfOccurrences** element contains the number of occurrences of a recurring item.</span></span> 
  
```xml
<NumberOfOccurrences/>
```

 <span data-ttu-id="1bafe-105">**int**</span><span class="sxs-lookup"><span data-stu-id="1bafe-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1bafe-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1bafe-106">Attributes and elements</span></span>

<span data-ttu-id="1bafe-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1bafe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1bafe-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1bafe-108">Attributes</span></span>

<span data-ttu-id="1bafe-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1bafe-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1bafe-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1bafe-110">Child elements</span></span>

<span data-ttu-id="1bafe-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1bafe-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1bafe-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1bafe-112">Parent elements</span></span>

|<span data-ttu-id="1bafe-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1bafe-113">**Element**</span></span>|<span data-ttu-id="1bafe-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1bafe-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1bafe-115">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="1bafe-115">NumberedRecurrence</span></span>](numberedrecurrence.md) <br/> |<span data-ttu-id="1bafe-116">Describe la fecha de inicio y el número de repeticiones de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="1bafe-116">Describes the start date and the number of occurrences of a recurring item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1bafe-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1bafe-117">Text value</span></span>

<span data-ttu-id="1bafe-118">El valor de texto es un entero que representa el número de repeticiones de un elemento periódico.</span><span class="sxs-lookup"><span data-stu-id="1bafe-118">The text value is an integer that represents the number of occurrences of a recurring item.</span></span> <span data-ttu-id="1bafe-119">El valor debe ser un número entero entre 1 y 999.</span><span class="sxs-lookup"><span data-stu-id="1bafe-119">The value must be an integer in the range of 1 to 999.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1bafe-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1bafe-120">Remarks</span></span>

<span data-ttu-id="1bafe-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="1bafe-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1bafe-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1bafe-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1bafe-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="1bafe-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1bafe-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1bafe-124">Schema name</span></span>  <br/> |<span data-ttu-id="1bafe-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="1bafe-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="1bafe-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1bafe-126">Validation file</span></span>  <br/> |<span data-ttu-id="1bafe-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="1bafe-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1bafe-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1bafe-128">Can be empty</span></span>  <br/> |<span data-ttu-id="1bafe-129">Falso</span><span class="sxs-lookup"><span data-stu-id="1bafe-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1bafe-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="1bafe-130">See also</span></span>



- [<span data-ttu-id="1bafe-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1bafe-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

