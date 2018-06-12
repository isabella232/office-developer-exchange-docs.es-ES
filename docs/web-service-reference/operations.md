---
title: Operaciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Operations
api_type:
- schema
ms.assetid: d8cd41b1-28ae-4c95-9ff6-8b25c8e18306
description: El elemento de operaciones contiene una matriz de las operaciones de la regla que se puede realizar en una bandeja de entrada.
ms.openlocfilehash: 1030703d5e496be391d557e99e1420f9fddfdb36
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836655"
---
# <a name="operations"></a><span data-ttu-id="599e6-103">Operaciones</span><span class="sxs-lookup"><span data-stu-id="599e6-103">Operations</span></span>

<span data-ttu-id="599e6-104">El elemento de **operaciones** contiene una matriz de las operaciones de la regla que se puede realizar en una bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="599e6-104">The **Operations** element contains an array of rule operations that can be performed on an Inbox.</span></span> 
  
[<span data-ttu-id="599e6-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="599e6-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
```XML
<Operations>
    <CreateRuleOperation/>
    <SetRuleOperation/>
    <DeleteRuleOperation/>
</Operations>
```

 <span data-ttu-id="599e6-106">**ArrayOfRuleOperationsType**</span><span class="sxs-lookup"><span data-stu-id="599e6-106">**ArrayOfRuleOperationsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="599e6-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="599e6-107">Attributes and elements</span></span>

<span data-ttu-id="599e6-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="599e6-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="599e6-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="599e6-109">Attributes</span></span>

<span data-ttu-id="599e6-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="599e6-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="599e6-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="599e6-111">Child elements</span></span>

|<span data-ttu-id="599e6-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="599e6-112">**Element**</span></span>|<span data-ttu-id="599e6-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="599e6-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="599e6-114">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="599e6-114">CreateRuleOperation</span></span>](createruleoperation.md) <br/> |<span data-ttu-id="599e6-115">Representa una operación para crear una nueva regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="599e6-115">Represents an operation to create a new Inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="599e6-116">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="599e6-116">SetRuleOperation</span></span>](setruleoperation.md) <br/> |<span data-ttu-id="599e6-117">Representa una operación para actualizar una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="599e6-117">Represents an operation to update an Inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="599e6-118">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="599e6-118">DeleteRuleOperation</span></span>](deleteruleoperation.md) <br/> |<span data-ttu-id="599e6-119">Representa una operación para eliminar una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="599e6-119">Represents an operation to delete an Inbox rule.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="599e6-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="599e6-120">Parent elements</span></span>

|<span data-ttu-id="599e6-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="599e6-121">**Element**</span></span>|<span data-ttu-id="599e6-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="599e6-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="599e6-123">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="599e6-123">UpdateInboxRules</span></span>](updateinboxrules.md) <br/> |<span data-ttu-id="599e6-124">Define una solicitud para actualizar las reglas de bandeja de entrada en un buzón en el almacén del servidor.</span><span class="sxs-lookup"><span data-stu-id="599e6-124">Defines a request to update the Inbox rules in a mailbox in the server store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="599e6-125">Notas</span><span class="sxs-lookup"><span data-stu-id="599e6-125">Remarks</span></span>

<span data-ttu-id="599e6-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="599e6-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="599e6-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="599e6-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="599e6-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="599e6-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="599e6-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="599e6-129">Schema Name</span></span>  <br/> |<span data-ttu-id="599e6-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="599e6-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="599e6-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="599e6-131">Validation File</span></span>  <br/> |<span data-ttu-id="599e6-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="599e6-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="599e6-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="599e6-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="599e6-134">False</span><span class="sxs-lookup"><span data-stu-id="599e6-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="599e6-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="599e6-135">See also</span></span>



[<span data-ttu-id="599e6-136">Operación de UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="599e6-136">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)


- [<span data-ttu-id="599e6-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="599e6-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

