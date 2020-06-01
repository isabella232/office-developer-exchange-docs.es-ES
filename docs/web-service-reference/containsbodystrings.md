---
title: ContainsBodyStrings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContainsBodyStrings
api_type:
- schema
ms.assetid: 70639472-64bb-456a-8b40-dce727542443
description: El elemento ContainsBodyStrings indica las cadenas que deben aparecer en el cuerpo de los mensajes entrantes para que se aplique la condición o excepción.
ms.openlocfilehash: 008261ab94b1bed33cc72cacf7abe7aa58927d1a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463807"
---
# <a name="containsbodystrings"></a><span data-ttu-id="2d8aa-103">ContainsBodyStrings</span><span class="sxs-lookup"><span data-stu-id="2d8aa-103">ContainsBodyStrings</span></span>

<span data-ttu-id="2d8aa-104">El elemento **ContainsBodyStrings** indica las cadenas que deben aparecer en el cuerpo de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="2d8aa-104">The **ContainsBodyStrings** element indicates the strings that must appear in the body of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ContainsBodyStrings>
    <String/>
</ContainsBodyStrings>
```

 <span data-ttu-id="2d8aa-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="2d8aa-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2d8aa-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2d8aa-106">Attributes and elements</span></span>

<span data-ttu-id="2d8aa-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2d8aa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d8aa-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2d8aa-108">Attributes</span></span>

<span data-ttu-id="2d8aa-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2d8aa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2d8aa-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2d8aa-110">Child elements</span></span>

|<span data-ttu-id="2d8aa-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2d8aa-111">**Element**</span></span>|<span data-ttu-id="2d8aa-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2d8aa-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d8aa-113">String</span><span class="sxs-lookup"><span data-stu-id="2d8aa-113">String</span></span>](string.md) <br/> |<span data-ttu-id="2d8aa-114">Representa una cadena que debe aparecer en el cuerpo de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="2d8aa-114">Represents a string that must appear in the body of incoming messages in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2d8aa-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2d8aa-115">Parent elements</span></span>

|<span data-ttu-id="2d8aa-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2d8aa-116">**Element**</span></span>|<span data-ttu-id="2d8aa-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2d8aa-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d8aa-118">Condiciones</span><span class="sxs-lookup"><span data-stu-id="2d8aa-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="2d8aa-119">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="2d8aa-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="2d8aa-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="2d8aa-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="2d8aa-121">Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="2d8aa-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2d8aa-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2d8aa-122">Text value</span></span>

<span data-ttu-id="2d8aa-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2d8aa-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2d8aa-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2d8aa-124">Remarks</span></span>

<span data-ttu-id="2d8aa-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2d8aa-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2d8aa-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2d8aa-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d8aa-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="2d8aa-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2d8aa-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2d8aa-128">Schema Name</span></span>  <br/> |<span data-ttu-id="2d8aa-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="2d8aa-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2d8aa-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2d8aa-130">Validation File</span></span>  <br/> |<span data-ttu-id="2d8aa-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2d8aa-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2d8aa-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2d8aa-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="2d8aa-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="2d8aa-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d8aa-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d8aa-134">See also</span></span>



- [<span data-ttu-id="2d8aa-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2d8aa-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

