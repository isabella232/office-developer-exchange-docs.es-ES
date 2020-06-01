---
title: DailyRegeneration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DailyRegeneration
api_type:
- schema
ms.assetid: cafb57e4-c518-45e0-b565-2babd0dab1df
description: El elemento DailyRegeneration describe la frecuencia, en días, en la que se regenera una tarea.
ms.openlocfilehash: 518e4666031131f4a5fc80cc72c28a2110b468c5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462167"
---
# <a name="dailyregeneration"></a><span data-ttu-id="da388-103">DailyRegeneration</span><span class="sxs-lookup"><span data-stu-id="da388-103">DailyRegeneration</span></span>

<span data-ttu-id="da388-104">El elemento **DailyRegeneration** describe la frecuencia, en días, en la que se regenera una tarea.</span><span class="sxs-lookup"><span data-stu-id="da388-104">The **DailyRegeneration** element describes the frequency, in days, in which a task is regenerated.</span></span> 
  
```xml
<DailyRegeneration>
   <Interval/>
</DailyRegeneration>
```

<span data-ttu-id="da388-105">**DailyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="da388-105">**DailyRegeneratingPatternType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="da388-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="da388-106">Attributes and elements</span></span>

<span data-ttu-id="da388-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="da388-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="da388-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="da388-108">Attributes</span></span>

<span data-ttu-id="da388-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="da388-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="da388-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="da388-110">Child elements</span></span>

|<span data-ttu-id="da388-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="da388-111">**Element**</span></span>|<span data-ttu-id="da388-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="da388-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da388-113">Intervalo de</span><span class="sxs-lookup"><span data-stu-id="da388-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="da388-114">Define el intervalo, en días, entre dos elementos periódicos consecutivos.</span><span class="sxs-lookup"><span data-stu-id="da388-114">Defines the interval, in days, between two consecutive recurring items.</span></span> <span data-ttu-id="da388-115">El valor debe estar comprendido entre 1 y 999.</span><span class="sxs-lookup"><span data-stu-id="da388-115">The value must be in the range of 1 to 999.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="da388-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="da388-116">Parent elements</span></span>

|<span data-ttu-id="da388-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="da388-117">**Element**</span></span>|<span data-ttu-id="da388-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="da388-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="da388-119">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="da388-119">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="da388-120">Contiene información de periodicidad para tareas periódicas.</span><span class="sxs-lookup"><span data-stu-id="da388-120">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da388-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="da388-121">Remarks</span></span>

<span data-ttu-id="da388-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="da388-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="da388-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="da388-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="da388-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="da388-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="da388-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="da388-125">Schema name</span></span>  <br/> |<span data-ttu-id="da388-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="da388-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="da388-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="da388-127">Validation file</span></span>  <br/> |<span data-ttu-id="da388-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="da388-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="da388-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="da388-129">Can be empty</span></span>  <br/> |<span data-ttu-id="da388-130">Falso</span><span class="sxs-lookup"><span data-stu-id="da388-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da388-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="da388-131">See also</span></span>

- [<span data-ttu-id="da388-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="da388-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

