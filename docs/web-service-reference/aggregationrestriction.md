---
title: AggregationRestriction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d05044f9-d2ff-4aca-956c-20c9cb2f7709
description: El elemento AggregationRestriction especifica un valor que se aplica a un conjunto de propiedades de rol como resultado de una solicitud FindPeople y filtra el resultado de acuerdo con la restricción especificada.
ms.openlocfilehash: f07e54235cf13b43da26ed1c56596d3c7c357bf2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463527"
---
# <a name="aggregationrestriction"></a><span data-ttu-id="9aca0-103">AggregationRestriction</span><span class="sxs-lookup"><span data-stu-id="9aca0-103">AggregationRestriction</span></span>

<span data-ttu-id="9aca0-104">El elemento **AggregationRestriction** especifica un valor que se aplica a un conjunto de propiedades de rol como resultado de una solicitud FindPeople y filtra el resultado de acuerdo con la restricción especificada.</span><span class="sxs-lookup"><span data-stu-id="9aca0-104">The **AggregationRestriction** element specifies a value that is applied to a set of Persona properties resulting from a FindPeople request and filters the result according to the specified restriction.</span></span> 
  
```XML
<AggregationRestriction>
   <SearchExpression/>
</AggregationRestriction>
```

 <span data-ttu-id="9aca0-105">**RestrictionType**</span><span class="sxs-lookup"><span data-stu-id="9aca0-105">**RestrictionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9aca0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9aca0-106">Attributes and elements</span></span>

<span data-ttu-id="9aca0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9aca0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9aca0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9aca0-108">Attributes</span></span>

<span data-ttu-id="9aca0-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9aca0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9aca0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9aca0-110">Child elements</span></span>

[<span data-ttu-id="9aca0-111">SearchExpression</span><span class="sxs-lookup"><span data-stu-id="9aca0-111">SearchExpression</span></span>](searchexpression.md)
  
### <a name="parent-elements"></a><span data-ttu-id="9aca0-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9aca0-112">Parent elements</span></span>

[<span data-ttu-id="9aca0-113">FindPeople</span><span class="sxs-lookup"><span data-stu-id="9aca0-113">FindPeople</span></span>](findpeople.md)
  
## <a name="remarks"></a><span data-ttu-id="9aca0-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9aca0-114">Remarks</span></span>

<span data-ttu-id="9aca0-115">El elemento **AggregationRestriction** puede contener cualquier elemento secundario que use el grupo de sustitución **SearchExpression** .</span><span class="sxs-lookup"><span data-stu-id="9aca0-115">The **AggregationRestriction** element can contain any child element that uses the **SearchExpression** substitution group.</span></span> <span data-ttu-id="9aca0-116">Los elementos que forman parte del grupo de sustitución de **SearchExpression** son: [Contains](contains.md), [Excludes](excludes.md), [EXISTS](exists.md), [Not](not.md), [or](or.md), [and](and.md), [IsEqualTo](isequalto.md), [IsNotEqualTo](isnotequalto.md), [IsGreaterThan](isgreaterthan.md), [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md), [IsLessThan](islessthan.md)y [IsLessThanOrEqualTo](islessthanorequalto.md).</span><span class="sxs-lookup"><span data-stu-id="9aca0-116">The elements that are a part of the **SearchExpression** substitution group are: [Contains](contains.md), [Excludes](excludes.md), [Exists](exists.md), [Not](not.md), [Or](or.md), [And](and.md), [IsEqualTo](isequalto.md), [IsNotEqualTo](isnotequalto.md), [IsGreaterThan](isgreaterthan.md), [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md), [IsLessThan](islessthan.md), and [IsLessThanOrEqualTo](islessthanorequalto.md).</span></span>
  
<span data-ttu-id="9aca0-117">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9aca0-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9aca0-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="9aca0-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9aca0-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9aca0-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9aca0-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="9aca0-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9aca0-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9aca0-121">Schema name</span></span>  <br/> |<span data-ttu-id="9aca0-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="9aca0-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9aca0-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9aca0-123">Validation file</span></span>  <br/> |<span data-ttu-id="9aca0-124">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9aca0-124">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9aca0-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9aca0-125">Can be empty</span></span>  <br/> |<span data-ttu-id="9aca0-126">false</span><span class="sxs-lookup"><span data-stu-id="9aca0-126">false</span></span>  <br/> |
   

