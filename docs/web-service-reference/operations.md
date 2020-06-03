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
description: El elemento Operations contiene una matriz de operaciones de regla que se pueden realizar en una bandeja de entrada.
ms.openlocfilehash: 4bbec4ad6424f802bb6781a870d65f23705e88c4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462489"
---
# <a name="operations"></a><span data-ttu-id="adc77-103">Operaciones</span><span class="sxs-lookup"><span data-stu-id="adc77-103">Operations</span></span>

<span data-ttu-id="adc77-104">El elemento **Operations** contiene una matriz de operaciones de regla que se pueden realizar en una bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="adc77-104">The **Operations** element contains an array of rule operations that can be performed on an Inbox.</span></span> 
  
[<span data-ttu-id="adc77-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="adc77-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
```XML
<Operations>
    <CreateRuleOperation/>
    <SetRuleOperation/>
    <DeleteRuleOperation/>
</Operations>
```

 <span data-ttu-id="adc77-106">**ArrayOfRuleOperationsType**</span><span class="sxs-lookup"><span data-stu-id="adc77-106">**ArrayOfRuleOperationsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="adc77-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="adc77-107">Attributes and elements</span></span>

<span data-ttu-id="adc77-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="adc77-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="adc77-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="adc77-109">Attributes</span></span>

<span data-ttu-id="adc77-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="adc77-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="adc77-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="adc77-111">Child elements</span></span>

|<span data-ttu-id="adc77-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="adc77-112">**Element**</span></span>|<span data-ttu-id="adc77-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="adc77-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="adc77-114">CreateRuleOperation</span><span class="sxs-lookup"><span data-stu-id="adc77-114">CreateRuleOperation</span></span>](createruleoperation.md) <br/> |<span data-ttu-id="adc77-115">Representa una operación para crear una nueva regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="adc77-115">Represents an operation to create a new Inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="adc77-116">SetRuleOperation</span><span class="sxs-lookup"><span data-stu-id="adc77-116">SetRuleOperation</span></span>](setruleoperation.md) <br/> |<span data-ttu-id="adc77-117">Representa una operación para actualizar una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="adc77-117">Represents an operation to update an Inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="adc77-118">DeleteRuleOperation</span><span class="sxs-lookup"><span data-stu-id="adc77-118">DeleteRuleOperation</span></span>](deleteruleoperation.md) <br/> |<span data-ttu-id="adc77-119">Representa una operación para eliminar una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="adc77-119">Represents an operation to delete an Inbox rule.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="adc77-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="adc77-120">Parent elements</span></span>

|<span data-ttu-id="adc77-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="adc77-121">**Element**</span></span>|<span data-ttu-id="adc77-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="adc77-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="adc77-123">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="adc77-123">UpdateInboxRules</span></span>](updateinboxrules.md) <br/> |<span data-ttu-id="adc77-124">Define una solicitud para actualizar las reglas de la bandeja de entrada en un buzón de correo en el almacén del servidor.</span><span class="sxs-lookup"><span data-stu-id="adc77-124">Defines a request to update the Inbox rules in a mailbox in the server store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="adc77-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="adc77-125">Remarks</span></span>

<span data-ttu-id="adc77-126">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="adc77-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="adc77-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="adc77-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="adc77-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="adc77-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="adc77-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="adc77-129">Schema Name</span></span>  <br/> |<span data-ttu-id="adc77-130">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="adc77-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="adc77-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="adc77-131">Validation File</span></span>  <br/> |<span data-ttu-id="adc77-132">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="adc77-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="adc77-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="adc77-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="adc77-134">Falso</span><span class="sxs-lookup"><span data-stu-id="adc77-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="adc77-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="adc77-135">See also</span></span>



[<span data-ttu-id="adc77-136">Operación de UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="adc77-136">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)


- [<span data-ttu-id="adc77-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="adc77-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

