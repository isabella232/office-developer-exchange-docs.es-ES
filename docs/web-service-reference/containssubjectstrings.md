---
title: ContainsSubjectStrings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContainsSubjectStrings
api_type:
- schema
ms.assetid: c6ec1d8d-8dd8-4c9a-a3e1-50e24958eb0d
description: El elemento ContainsSubjectStrings indica las cadenas que deben aparecer en el asunto de los mensajes entrantes para que se aplique la condición o excepción.
ms.openlocfilehash: 8b078f61d08864970a123f81688981ffba2864ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458960"
---
# <a name="containssubjectstrings"></a><span data-ttu-id="7780d-103">ContainsSubjectStrings</span><span class="sxs-lookup"><span data-stu-id="7780d-103">ContainsSubjectStrings</span></span>

<span data-ttu-id="7780d-104">El elemento **ContainsSubjectStrings** indica las cadenas que deben aparecer en el asunto de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="7780d-104">The **ContainsSubjectStrings** element indicates the strings that must appear in the subject of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ContainsSubjectStrings>
    <String/>
</ContainsSubjectStrings>
```

 <span data-ttu-id="7780d-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="7780d-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7780d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7780d-106">Attributes and elements</span></span>

<span data-ttu-id="7780d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7780d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7780d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7780d-108">Attributes</span></span>

<span data-ttu-id="7780d-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7780d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7780d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7780d-110">Child elements</span></span>

|<span data-ttu-id="7780d-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7780d-111">**Element**</span></span>|<span data-ttu-id="7780d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7780d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7780d-113">String</span><span class="sxs-lookup"><span data-stu-id="7780d-113">String</span></span>](string.md) <br/> |<span data-ttu-id="7780d-114">Representa una cadena que debe aparecer en el asunto de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="7780d-114">Represents a string that must appear in the subject of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7780d-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7780d-115">Parent elements</span></span>

|<span data-ttu-id="7780d-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7780d-116">**Element**</span></span>|<span data-ttu-id="7780d-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7780d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7780d-118">Condiciones</span><span class="sxs-lookup"><span data-stu-id="7780d-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="7780d-119">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="7780d-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="7780d-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="7780d-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="7780d-121">Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="7780d-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7780d-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7780d-122">Text value</span></span>

<span data-ttu-id="7780d-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7780d-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7780d-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7780d-124">Remarks</span></span>

<span data-ttu-id="7780d-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7780d-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7780d-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7780d-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7780d-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="7780d-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7780d-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7780d-128">Schema Name</span></span>  <br/> |<span data-ttu-id="7780d-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="7780d-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7780d-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7780d-130">Validation File</span></span>  <br/> |<span data-ttu-id="7780d-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7780d-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7780d-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7780d-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="7780d-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="7780d-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7780d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="7780d-134">See also</span></span>



- [<span data-ttu-id="7780d-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="7780d-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

