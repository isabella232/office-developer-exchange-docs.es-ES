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
description: El elemento IsNDR indica si los mensajes entrantes deben ser informes de no entrega (NDR) con el fin de que se aplique la condición o excepción.
ms.openlocfilehash: 3476331ccece347686b7f98edf49df5d48b8562e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458162"
---
# <a name="isndr"></a><span data-ttu-id="0e260-103">IsNDR</span><span class="sxs-lookup"><span data-stu-id="0e260-103">IsNDR</span></span>

<span data-ttu-id="0e260-104">El elemento **IsNDR** indica si los mensajes entrantes deben ser informes de no entrega (NDR) con el fin de que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="0e260-104">The **IsNDR** element indicates whether incoming messages must be non-delivery reports (NDRs) in order for the condition or exception to apply.</span></span> 
  
```XML
<IsNDR>true | false</IsNDR>
```

 <span data-ttu-id="0e260-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0e260-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0e260-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0e260-106">Attributes and elements</span></span>

<span data-ttu-id="0e260-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0e260-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0e260-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0e260-108">Attributes</span></span>

<span data-ttu-id="0e260-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0e260-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0e260-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0e260-110">Child elements</span></span>

<span data-ttu-id="0e260-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0e260-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0e260-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0e260-112">Parent elements</span></span>

|<span data-ttu-id="0e260-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0e260-113">**Element**</span></span>|<span data-ttu-id="0e260-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0e260-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0e260-115">Condiciones</span><span class="sxs-lookup"><span data-stu-id="0e260-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="0e260-116">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="0e260-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="0e260-117">Excepciones</span><span class="sxs-lookup"><span data-stu-id="0e260-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="0e260-118">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="0e260-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0e260-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0e260-119">Text value</span></span>

<span data-ttu-id="0e260-120">Un valor de texto de **true** indica que el mensaje debe ser un NDR para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="0e260-120">A text value of **true** indicates that the message must be an NDR in order for the condition or exception to apply.</span></span> <span data-ttu-id="0e260-121">Un valor de **false** indica que el mensaje no debe ser un NDR en orden para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="0e260-121">A value of **false** indicates that the message must not be an NDR in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0e260-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e260-122">Remarks</span></span>

<span data-ttu-id="0e260-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0e260-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0e260-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0e260-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e260-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="0e260-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0e260-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0e260-126">Schema Name</span></span>  <br/> |<span data-ttu-id="0e260-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0e260-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0e260-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0e260-128">Validation File</span></span>  <br/> |<span data-ttu-id="0e260-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0e260-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0e260-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0e260-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="0e260-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="0e260-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e260-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e260-132">See also</span></span>



- [<span data-ttu-id="0e260-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0e260-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

