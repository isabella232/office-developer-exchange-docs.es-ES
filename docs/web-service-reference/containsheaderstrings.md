---
title: ContainsHeaderStrings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContainsHeaderStrings
api_type:
- schema
ms.assetid: 5f68427b-990a-4a27-bfb3-fce3115b02d7
description: El elemento ContainsHeaderStrings indica las cadenas que deben aparecer en los encabezados de los mensajes entrantes para que se aplique la condición o excepción.
ms.openlocfilehash: 23e3d0e7cff9c78edbac10a6275514af93cab325
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458995"
---
# <a name="containsheaderstrings"></a><span data-ttu-id="aac8f-103">ContainsHeaderStrings</span><span class="sxs-lookup"><span data-stu-id="aac8f-103">ContainsHeaderStrings</span></span>

<span data-ttu-id="aac8f-104">El elemento **ContainsHeaderStrings** indica las cadenas que deben aparecer en los encabezados de los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="aac8f-104">The **ContainsHeaderStrings** element indicates the strings that must appear in the headers of incoming messages in order for the condition or exception to apply.</span></span> 
  
```XML
<ContainsHeaderStrings>
    <String/>
</ContainsHeaderStrings>
```

 <span data-ttu-id="aac8f-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="aac8f-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aac8f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="aac8f-106">Attributes and elements</span></span>

<span data-ttu-id="aac8f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="aac8f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aac8f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="aac8f-108">Attributes</span></span>

<span data-ttu-id="aac8f-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="aac8f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aac8f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aac8f-110">Child elements</span></span>

|<span data-ttu-id="aac8f-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aac8f-111">**Element**</span></span>|<span data-ttu-id="aac8f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aac8f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aac8f-113">String</span><span class="sxs-lookup"><span data-stu-id="aac8f-113">String</span></span>](string.md) <br/> |<span data-ttu-id="aac8f-114">Representa una cadena que debe aparecer en los encabezados de los mensajes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="aac8f-114">Represents a string that must appear in message headers in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aac8f-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="aac8f-115">Parent elements</span></span>

|<span data-ttu-id="aac8f-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="aac8f-116">**Element**</span></span>|<span data-ttu-id="aac8f-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aac8f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aac8f-118">Condiciones</span><span class="sxs-lookup"><span data-stu-id="aac8f-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="aac8f-119">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="aac8f-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="aac8f-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="aac8f-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="aac8f-121">Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="aac8f-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="aac8f-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="aac8f-122">Text value</span></span>

<span data-ttu-id="aac8f-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aac8f-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aac8f-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aac8f-124">Remarks</span></span>

<span data-ttu-id="aac8f-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="aac8f-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aac8f-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="aac8f-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aac8f-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="aac8f-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="aac8f-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="aac8f-128">Schema Name</span></span>  <br/> |<span data-ttu-id="aac8f-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="aac8f-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="aac8f-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="aac8f-130">Validation File</span></span>  <br/> |<span data-ttu-id="aac8f-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="aac8f-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="aac8f-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="aac8f-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="aac8f-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="aac8f-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aac8f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="aac8f-134">See also</span></span>



- [<span data-ttu-id="aac8f-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="aac8f-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

