---
title: FromAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FromAddresses
api_type:
- schema
ms.assetid: b219f315-c20a-4633-af3e-94bd3e4526b6
description: El elemento FromAddresses indica las direcciones de correo electrónico desde las que se deben enviar los mensajes entrantes para que se aplique la condición o excepción.
ms.openlocfilehash: 4fbb44d02f5010c4395cf691cb6160da4dbb6930
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459542"
---
# <a name="fromaddresses"></a><span data-ttu-id="88436-103">FromAddresses</span><span class="sxs-lookup"><span data-stu-id="88436-103">FromAddresses</span></span>

<span data-ttu-id="88436-104">El elemento **FromAddresses** indica las direcciones de correo electrónico desde las que se deben enviar los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="88436-104">The **FromAddresses** element indicates the e-mail addresses from which incoming messages must be sent in order for the condition or exception to apply.</span></span> 
  
```XML
<FromAddresses>
   <Address/>
</FromAddresses>
```

 <span data-ttu-id="88436-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="88436-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="88436-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="88436-106">Attributes and elements</span></span>

<span data-ttu-id="88436-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="88436-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88436-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="88436-108">Attributes</span></span>

<span data-ttu-id="88436-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="88436-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="88436-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="88436-110">Child elements</span></span>

|<span data-ttu-id="88436-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="88436-111">**Element**</span></span>|<span data-ttu-id="88436-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="88436-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88436-113">Dirección (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="88436-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="88436-114">Representa una dirección de correo electrónico completamente resuelta.</span><span class="sxs-lookup"><span data-stu-id="88436-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="88436-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="88436-115">Parent elements</span></span>

|<span data-ttu-id="88436-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="88436-116">**Element**</span></span>|<span data-ttu-id="88436-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="88436-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88436-118">Condiciones</span><span class="sxs-lookup"><span data-stu-id="88436-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="88436-119">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="88436-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="88436-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="88436-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="88436-121">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="88436-121">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="88436-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="88436-122">Text value</span></span>

<span data-ttu-id="88436-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="88436-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="88436-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="88436-124">Remarks</span></span>

<span data-ttu-id="88436-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="88436-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="88436-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="88436-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88436-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="88436-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="88436-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="88436-128">Schema Name</span></span>  <br/> |<span data-ttu-id="88436-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="88436-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="88436-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="88436-130">Validation File</span></span>  <br/> |<span data-ttu-id="88436-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="88436-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="88436-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="88436-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="88436-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="88436-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88436-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="88436-134">See also</span></span>



- [<span data-ttu-id="88436-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="88436-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

