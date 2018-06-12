---
title: IsNDR
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsNDR
api_type:
- schema
ms.assetid: 194f5836-7793-463a-a090-4386d1c2487a
description: El elemento IsNDR indica si los mensajes entrantes deben ser informes de no entrega (NDR) en orden para la condición o la excepción que se debe aplicar.
ms.openlocfilehash: 651590d055a0532c904dbf6c481dca2f899d673f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836056"
---
# <a name="isndr"></a><span data-ttu-id="437e6-103">IsNDR</span><span class="sxs-lookup"><span data-stu-id="437e6-103">IsNDR</span></span>

<span data-ttu-id="437e6-104">El elemento **IsNDR** indica si los mensajes entrantes deben ser informes de no entrega (NDR) en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="437e6-104">The **IsNDR** element indicates whether incoming messages must be non-delivery reports (NDRs) in order for the condition or exception to apply.</span></span> 
  
```XML
<IsNDR>true | false</IsNDR>
```

 <span data-ttu-id="437e6-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="437e6-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="437e6-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="437e6-106">Attributes and elements</span></span>

<span data-ttu-id="437e6-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="437e6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="437e6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="437e6-108">Attributes</span></span>

<span data-ttu-id="437e6-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="437e6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="437e6-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="437e6-110">Child elements</span></span>

<span data-ttu-id="437e6-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="437e6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="437e6-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="437e6-112">Parent elements</span></span>

|<span data-ttu-id="437e6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="437e6-113">**Element**</span></span>|<span data-ttu-id="437e6-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="437e6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="437e6-115">Condiciones</span><span class="sxs-lookup"><span data-stu-id="437e6-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="437e6-116">Representa las condiciones que, cuando se cumplen los requisitos, se activará las acciones de regla para una regla.</span><span class="sxs-lookup"><span data-stu-id="437e6-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="437e6-117">Excepciones</span><span class="sxs-lookup"><span data-stu-id="437e6-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="437e6-118">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="437e6-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="437e6-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="437e6-119">Text value</span></span>

<span data-ttu-id="437e6-120">Un valor de texto de **true** indica que el mensaje debe ser un NDR en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="437e6-120">A text value of **true** indicates that the message must be an NDR in order for the condition or exception to apply.</span></span> <span data-ttu-id="437e6-121">Un valor de **false** indica que el mensaje no debe ser un NDR en orden para la condición o la excepción que se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="437e6-121">A value of **false** indicates that the message must not be an NDR in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="437e6-122">Notas</span><span class="sxs-lookup"><span data-stu-id="437e6-122">Remarks</span></span>

<span data-ttu-id="437e6-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="437e6-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="437e6-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="437e6-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="437e6-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="437e6-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="437e6-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="437e6-126">Schema Name</span></span>  <br/> |<span data-ttu-id="437e6-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="437e6-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="437e6-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="437e6-128">Validation File</span></span>  <br/> |<span data-ttu-id="437e6-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="437e6-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="437e6-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="437e6-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="437e6-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="437e6-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="437e6-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="437e6-132">See also</span></span>



- [<span data-ttu-id="437e6-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="437e6-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

