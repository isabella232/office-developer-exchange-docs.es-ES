---
title: MonthlyRegeneration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MonthlyRegeneration
api_type:
- schema
ms.assetid: 9a52ca97-a663-41fe-b61a-61d8c53833ca
description: El elemento MonthlyRegeneration describe la frecuencia, en meses, de la tarea que se regenera.
ms.openlocfilehash: c941bc2606790646d2797df27c854996901c0bc6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462741"
---
# <a name="monthlyregeneration"></a><span data-ttu-id="86f01-103">MonthlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="86f01-103">MonthlyRegeneration</span></span>

<span data-ttu-id="86f01-104">El elemento **MonthlyRegeneration** describe la frecuencia, en meses, de la tarea que se regenera.</span><span class="sxs-lookup"><span data-stu-id="86f01-104">The **MonthlyRegeneration** element describes the frequency, in months, of which task is regenerated.</span></span> 
  
```xml
<MonthlyRegeneration>
   <Interval/>
</MonthlyRegeneration>
```

 <span data-ttu-id="86f01-105">**MonthlyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="86f01-105">**MonthlyRegeneratingPatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="86f01-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="86f01-106">Attributes and elements</span></span>

<span data-ttu-id="86f01-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="86f01-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="86f01-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="86f01-108">Attributes</span></span>

<span data-ttu-id="86f01-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="86f01-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="86f01-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="86f01-110">Child elements</span></span>

|<span data-ttu-id="86f01-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="86f01-111">**Element**</span></span>|<span data-ttu-id="86f01-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86f01-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86f01-113">Intervalo de</span><span class="sxs-lookup"><span data-stu-id="86f01-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="86f01-114">Define el intervalo, en meses, entre dos elementos periódicos consecutivos.</span><span class="sxs-lookup"><span data-stu-id="86f01-114">Defines the interval, in months, between two consecutive recurring items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="86f01-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="86f01-115">Parent elements</span></span>

|<span data-ttu-id="86f01-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="86f01-116">**Element**</span></span>|<span data-ttu-id="86f01-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="86f01-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86f01-118">Periodicidad (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="86f01-118">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="86f01-119">Contiene información de periodicidad para tareas periódicas.</span><span class="sxs-lookup"><span data-stu-id="86f01-119">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86f01-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="86f01-120">Remarks</span></span>

<span data-ttu-id="86f01-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="86f01-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="86f01-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="86f01-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86f01-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="86f01-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="86f01-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="86f01-124">Schema name</span></span>  <br/> |<span data-ttu-id="86f01-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="86f01-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="86f01-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="86f01-126">Validation file</span></span>  <br/> |<span data-ttu-id="86f01-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="86f01-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="86f01-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="86f01-128">Can be empty</span></span>  <br/> |<span data-ttu-id="86f01-129">Falso</span><span class="sxs-lookup"><span data-stu-id="86f01-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="86f01-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="86f01-130">See also</span></span>



- [<span data-ttu-id="86f01-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="86f01-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

