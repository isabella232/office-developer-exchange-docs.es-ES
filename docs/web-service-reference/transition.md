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
description: El elemento Transition representa una transición de zona horaria.
ms.openlocfilehash: 05495eb4a493feedc88532cc4bc8b949493481f5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467497"
---
# <a name="transition"></a><span data-ttu-id="81a05-103">Transición</span><span class="sxs-lookup"><span data-stu-id="81a05-103">Transition</span></span>

<span data-ttu-id="81a05-104">El elemento **Transition** representa una transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="81a05-104">The **Transition** element represents a time zone transition.</span></span> 
  
```xml
<Transition>
   <To/>
</Transition>
```

 <span data-ttu-id="81a05-105">**TransitionType**</span><span class="sxs-lookup"><span data-stu-id="81a05-105">**TransitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="81a05-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="81a05-106">Attributes and elements</span></span>

<span data-ttu-id="81a05-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="81a05-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="81a05-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="81a05-108">Attributes</span></span>

<span data-ttu-id="81a05-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="81a05-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="81a05-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="81a05-110">Child elements</span></span>

|<span data-ttu-id="81a05-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="81a05-111">**Element**</span></span>|<span data-ttu-id="81a05-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="81a05-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81a05-113">To</span><span class="sxs-lookup"><span data-stu-id="81a05-113">To</span></span>](to.md) <br/> |<span data-ttu-id="81a05-114">Especifica el [punto](period.md) o [TransitionsGroup](transitionsgroup.md) que es el destino de la transición de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="81a05-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="81a05-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="81a05-115">Parent elements</span></span>

|<span data-ttu-id="81a05-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="81a05-116">**Element**</span></span>|<span data-ttu-id="81a05-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="81a05-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81a05-118">Transiciones</span><span class="sxs-lookup"><span data-stu-id="81a05-118">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="81a05-119">Representa una colección de transiciones de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="81a05-119">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81a05-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="81a05-120">Remarks</span></span>

<span data-ttu-id="81a05-121">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="81a05-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="81a05-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="81a05-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81a05-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="81a05-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="81a05-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="81a05-124">Schema Name</span></span>  <br/> |<span data-ttu-id="81a05-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="81a05-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="81a05-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="81a05-126">Validation File</span></span>  <br/> |<span data-ttu-id="81a05-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="81a05-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="81a05-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="81a05-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="81a05-129">Falso</span><span class="sxs-lookup"><span data-stu-id="81a05-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81a05-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="81a05-130">See also</span></span>



- [<span data-ttu-id="81a05-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="81a05-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

