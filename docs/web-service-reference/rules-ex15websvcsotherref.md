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
description: El elemento rules contiene una matriz de reglas de protección.
ms.openlocfilehash: d848abfe0c97d07836f28bc75806f506c5433d44
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464941"
---
# <a name="rules"></a><span data-ttu-id="309ff-103">Reglas</span><span class="sxs-lookup"><span data-stu-id="309ff-103">Rules</span></span>

<span data-ttu-id="309ff-104">El elemento **rules** contiene una matriz de reglas de protección.</span><span class="sxs-lookup"><span data-stu-id="309ff-104">The **Rules** element contains an array of protection rules.</span></span> 
  
```xml
<Rules>   <Rule/></Rules>
```

 <span data-ttu-id="309ff-105">**ArrayOfProtectionRulesType**</span><span class="sxs-lookup"><span data-stu-id="309ff-105">**ArrayOfProtectionRulesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="309ff-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="309ff-106">Attributes and elements</span></span>

<span data-ttu-id="309ff-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="309ff-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="309ff-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="309ff-108">Attributes</span></span>

<span data-ttu-id="309ff-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="309ff-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="309ff-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="309ff-110">Child elements</span></span>

|<span data-ttu-id="309ff-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="309ff-111">**Element**</span></span>|<span data-ttu-id="309ff-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="309ff-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="309ff-113">Rule</span><span class="sxs-lookup"><span data-stu-id="309ff-113">Rule</span></span>](rule.md) <br/> |<span data-ttu-id="309ff-114">Contiene una regla de protección única.</span><span class="sxs-lookup"><span data-stu-id="309ff-114">Contains a single protection rule.</span></span> <span data-ttu-id="309ff-115">Este elemento se puede producir cero o más veces.</span><span class="sxs-lookup"><span data-stu-id="309ff-115">This element can occur zero or more times.</span></span> <span data-ttu-id="309ff-116">Este elemento se produce cero veces cuando la organización no define ninguna regla de protección.</span><span class="sxs-lookup"><span data-stu-id="309ff-116">This element occurs zero times when no protection rules are defined by the organization.</span></span> <span data-ttu-id="309ff-117">Se produce una o varias veces si la organización define al menos una regla.</span><span class="sxs-lookup"><span data-stu-id="309ff-117">It occurs one or more times if at least one rule is defined by the organization.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="309ff-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="309ff-118">Parent elements</span></span>

|<span data-ttu-id="309ff-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="309ff-119">**Element**</span></span>|<span data-ttu-id="309ff-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="309ff-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="309ff-121">ProtectionRulesConfiguration</span><span class="sxs-lookup"><span data-stu-id="309ff-121">ProtectionRulesConfiguration</span></span>](protectionrulesconfiguration.md) <br/> |<span data-ttu-id="309ff-122">Contiene la configuración del servicio para el servicio de reglas de protección.</span><span class="sxs-lookup"><span data-stu-id="309ff-122">Contains service configuration for the protection rules service.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="309ff-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="309ff-123">Remarks</span></span>

<span data-ttu-id="309ff-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="309ff-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="309ff-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="309ff-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="309ff-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="309ff-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="309ff-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="309ff-127">Schema Name</span></span>  <br/> |<span data-ttu-id="309ff-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="309ff-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="309ff-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="309ff-129">Validation File</span></span>  <br/> |<span data-ttu-id="309ff-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="309ff-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="309ff-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="309ff-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="309ff-132">Falso</span><span class="sxs-lookup"><span data-stu-id="309ff-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="309ff-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="309ff-133">See also</span></span>



- [<span data-ttu-id="309ff-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="309ff-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

