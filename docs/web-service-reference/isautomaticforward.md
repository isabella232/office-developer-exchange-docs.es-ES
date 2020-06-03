---
title: IsAutomaticForward
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsAutomaticForward
api_type:
- schema
ms.assetid: 6876b849-a648-482e-8934-93eb5a0c465f
description: El elemento IsAutomaticForward indica si los mensajes entrantes deben ser reenviados automáticamente para que se aplique la condición o excepción.
ms.openlocfilehash: 800d38bab30245d88b3c09609e6235e6de8fed25
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455579"
---
# <a name="isautomaticforward"></a><span data-ttu-id="65345-103">IsAutomaticForward</span><span class="sxs-lookup"><span data-stu-id="65345-103">IsAutomaticForward</span></span>

<span data-ttu-id="65345-104">El elemento **IsAutomaticForward** indica si los mensajes entrantes deben ser reenviados automáticamente para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="65345-104">The **IsAutomaticForward** element indicates whether incoming messages must be automatic forwards in order for the condition or exception to apply.</span></span> 
  
```XML
<IsAutomaticForward/> true | false</IsAutomaticForward>
```

 <span data-ttu-id="65345-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="65345-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="65345-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="65345-106">Attributes and elements</span></span>

<span data-ttu-id="65345-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="65345-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65345-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="65345-108">Attributes</span></span>

<span data-ttu-id="65345-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="65345-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="65345-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="65345-110">Child elements</span></span>

<span data-ttu-id="65345-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="65345-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="65345-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="65345-112">Parent elements</span></span>

|<span data-ttu-id="65345-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="65345-113">**Element**</span></span>|<span data-ttu-id="65345-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65345-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65345-115">Condiciones</span><span class="sxs-lookup"><span data-stu-id="65345-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="65345-116">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="65345-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="65345-117">Excepciones</span><span class="sxs-lookup"><span data-stu-id="65345-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="65345-118">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="65345-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="65345-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="65345-119">Text value</span></span>

<span data-ttu-id="65345-120">Un valor de texto de **true** indica que el mensaje debe ser un envío automático para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="65345-120">A text value of **true** indicates that the message must be an automatic forward in order for the condition or exception to apply.</span></span> <span data-ttu-id="65345-121">Un valor de **false** indica que el mensaje no debe ser reenviado automáticamente para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="65345-121">A value of **false** indicates that the message must not be an automatic forward in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="65345-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="65345-122">Remarks</span></span>

<span data-ttu-id="65345-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="65345-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65345-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="65345-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65345-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="65345-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="65345-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="65345-126">Schema Name</span></span>  <br/> |<span data-ttu-id="65345-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="65345-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="65345-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="65345-128">Validation File</span></span>  <br/> |<span data-ttu-id="65345-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="65345-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="65345-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="65345-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="65345-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="65345-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65345-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="65345-132">See also</span></span>



- [<span data-ttu-id="65345-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="65345-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

