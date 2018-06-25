---
title: Reglas
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Rules
api_type:
- schema
ms.assetid: 53f59054-8f68-4eaa-be9c-ccfc9383bcf2
description: El elemento reglas contiene una matriz de las reglas de protección.
ms.openlocfilehash: 5d511f977f3eb3273dc43f56356a059985b2a929
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837269"
---
# <a name="rules"></a><span data-ttu-id="606ed-103">Reglas</span><span class="sxs-lookup"><span data-stu-id="606ed-103">Rules</span></span>

<span data-ttu-id="606ed-104">El elemento **reglas** contiene una matriz de las reglas de protección.</span><span class="sxs-lookup"><span data-stu-id="606ed-104">The **Rules** element contains an array of protection rules.</span></span> 
  
```xml
<Rules>   <Rule/></Rules>
```

 <span data-ttu-id="606ed-105">**ArrayOfProtectionRulesType**</span><span class="sxs-lookup"><span data-stu-id="606ed-105">**ArrayOfProtectionRulesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="606ed-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="606ed-106">Attributes and elements</span></span>

<span data-ttu-id="606ed-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="606ed-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="606ed-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="606ed-108">Attributes</span></span>

<span data-ttu-id="606ed-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="606ed-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="606ed-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="606ed-110">Child elements</span></span>

|<span data-ttu-id="606ed-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="606ed-111">**Element**</span></span>|<span data-ttu-id="606ed-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="606ed-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="606ed-113">Rule</span><span class="sxs-lookup"><span data-stu-id="606ed-113">Rule</span></span>](rule.md) <br/> |<span data-ttu-id="606ed-114">Contiene una regla de protección única.</span><span class="sxs-lookup"><span data-stu-id="606ed-114">Contains a single protection rule.</span></span> <span data-ttu-id="606ed-115">Este elemento puede aparecer cero o más veces.</span><span class="sxs-lookup"><span data-stu-id="606ed-115">This element can occur zero or more times.</span></span> <span data-ttu-id="606ed-116">Este elemento produce cero veces cuando no hay reglas de protección se definen por la organización.</span><span class="sxs-lookup"><span data-stu-id="606ed-116">This element occurs zero times when no protection rules are defined by the organization.</span></span> <span data-ttu-id="606ed-117">Se produce una o varias veces, si se define al menos una regla por la organización.</span><span class="sxs-lookup"><span data-stu-id="606ed-117">It occurs one or more times if at least one rule is defined by the organization.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="606ed-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="606ed-118">Parent elements</span></span>

|<span data-ttu-id="606ed-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="606ed-119">**Element**</span></span>|<span data-ttu-id="606ed-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="606ed-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="606ed-121">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="606ed-121">ProtectionRulesConfiguration</span></span>](protectionrulesconfiguration.md) <br/> |<span data-ttu-id="606ed-122">Contiene la configuración del servicio para el servicio de protección de las reglas.</span><span class="sxs-lookup"><span data-stu-id="606ed-122">Contains service configuration for the protection rules service.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="606ed-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="606ed-123">Remarks</span></span>

<span data-ttu-id="606ed-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="606ed-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="606ed-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="606ed-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="606ed-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="606ed-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="606ed-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="606ed-127">Schema Name</span></span>  <br/> |<span data-ttu-id="606ed-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="606ed-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="606ed-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="606ed-129">Validation File</span></span>  <br/> |<span data-ttu-id="606ed-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="606ed-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="606ed-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="606ed-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="606ed-132">False</span><span class="sxs-lookup"><span data-stu-id="606ed-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="606ed-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="606ed-133">See also</span></span>



- [<span data-ttu-id="606ed-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="606ed-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

