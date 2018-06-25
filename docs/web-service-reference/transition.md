---
title: Transición
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Transition
api_type:
- schema
ms.assetid: 23ce171a-a9c9-47ed-a366-822777048eea
description: El elemento de transición representa una transición de la zona horaria.
ms.openlocfilehash: 5dcd2f0dae7c3df2dcf660d6fe1a41b216c67b59
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840727"
---
# <a name="transition"></a><span data-ttu-id="5f4db-103">Transición</span><span class="sxs-lookup"><span data-stu-id="5f4db-103">Transition</span></span>

<span data-ttu-id="5f4db-104">El elemento de **transición** representa una transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="5f4db-104">The **Transition** element represents a time zone transition.</span></span> 
  
```xml
<Transition>
   <To/>
</Transition>
```

 <span data-ttu-id="5f4db-105">**TransiciónEscriba el**</span><span class="sxs-lookup"><span data-stu-id="5f4db-105">**TransitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5f4db-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5f4db-106">Attributes and elements</span></span>

<span data-ttu-id="5f4db-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5f4db-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f4db-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5f4db-108">Attributes</span></span>

<span data-ttu-id="5f4db-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5f4db-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5f4db-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5f4db-110">Child elements</span></span>

|<span data-ttu-id="5f4db-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="5f4db-111">**Element**</span></span>|<span data-ttu-id="5f4db-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f4db-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f4db-113">To</span><span class="sxs-lookup"><span data-stu-id="5f4db-113">To</span></span>](to.md) <br/> |<span data-ttu-id="5f4db-114">Especifica el [período](period.md) o [TransitionsGroup](transitionsgroup.md) que es el destino de la transición de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="5f4db-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5f4db-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5f4db-115">Parent elements</span></span>

|<span data-ttu-id="5f4db-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="5f4db-116">**Element**</span></span>|<span data-ttu-id="5f4db-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5f4db-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f4db-118">Transiciones</span><span class="sxs-lookup"><span data-stu-id="5f4db-118">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="5f4db-119">Representa una colección de transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="5f4db-119">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f4db-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f4db-120">Remarks</span></span>

<span data-ttu-id="5f4db-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="5f4db-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5f4db-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5f4db-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f4db-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5f4db-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5f4db-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5f4db-124">Schema Name</span></span>  <br/> |<span data-ttu-id="5f4db-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="5f4db-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="5f4db-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5f4db-126">Validation File</span></span>  <br/> |<span data-ttu-id="5f4db-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5f4db-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5f4db-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5f4db-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="5f4db-129">False</span><span class="sxs-lookup"><span data-stu-id="5f4db-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5f4db-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f4db-130">See also</span></span>



- [<span data-ttu-id="5f4db-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="5f4db-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

