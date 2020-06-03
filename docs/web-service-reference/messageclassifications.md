---
title: MessageClassifications
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageClassifications
api_type:
- schema
ms.assetid: 041b3d48-8f43-47f3-869f-72b66bef372a
description: El elemento MessageClassifications representa las clasificaciones de mensajes que se deben marcar en los mensajes entrantes para que se aplique la condición o excepción.
ms.openlocfilehash: 63481aa8903c4e9637870130eb9154118471c3b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467973"
---
# <a name="messageclassifications"></a><span data-ttu-id="cb246-103">MessageClassifications</span><span class="sxs-lookup"><span data-stu-id="cb246-103">MessageClassifications</span></span>

<span data-ttu-id="cb246-104">El elemento **MessageClassifications** representa las clasificaciones de mensajes que se deben marcar en los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="cb246-104">The **MessageClassifications** element represents the message classifications that must be stamped on incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<MessageClassifications>
    <String/>
</MessageClassifications>
```

 <span data-ttu-id="cb246-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="cb246-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cb246-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cb246-106">Attributes and elements</span></span>

<span data-ttu-id="cb246-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cb246-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb246-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cb246-108">Attributes</span></span>

<span data-ttu-id="cb246-109">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cb246-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cb246-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cb246-110">Child elements</span></span>

|<span data-ttu-id="cb246-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cb246-111">**Element**</span></span>|<span data-ttu-id="cb246-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cb246-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb246-113">String</span><span class="sxs-lookup"><span data-stu-id="cb246-113">String</span></span>](string.md) <br/> |<span data-ttu-id="cb246-114">Representa una clasificación de mensaje.</span><span class="sxs-lookup"><span data-stu-id="cb246-114">Represents a message classification.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cb246-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cb246-115">Parent elements</span></span>

|<span data-ttu-id="cb246-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cb246-116">**Element**</span></span>|<span data-ttu-id="cb246-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cb246-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb246-118">Condiciones</span><span class="sxs-lookup"><span data-stu-id="cb246-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="cb246-119">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="cb246-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="cb246-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="cb246-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="cb246-121">Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="cb246-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cb246-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cb246-122">Text value</span></span>

<span data-ttu-id="cb246-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="cb246-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cb246-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb246-124">Remarks</span></span>

<span data-ttu-id="cb246-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="cb246-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb246-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cb246-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb246-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="cb246-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cb246-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cb246-128">Schema Name</span></span>  <br/> |<span data-ttu-id="cb246-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="cb246-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cb246-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cb246-130">Validation File</span></span>  <br/> |<span data-ttu-id="cb246-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="cb246-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cb246-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cb246-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="cb246-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="cb246-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb246-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb246-134">See also</span></span>



- [<span data-ttu-id="cb246-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cb246-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

