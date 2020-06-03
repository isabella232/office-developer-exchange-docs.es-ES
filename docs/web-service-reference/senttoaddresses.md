---
title: SentToAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SentToAddresses
api_type:
- schema
ms.assetid: 086130d2-93b1-4de1-9553-10ec10322a0c
description: El elemento SentToAddresses indica las direcciones de correo electrónico a las que se deben enviar los mensajes entrantes para que se aplique la condición o excepción.
ms.openlocfilehash: 9a901a93b666144092bf9cc8ebbf03222ac7bf6b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457420"
---
# <a name="senttoaddresses"></a><span data-ttu-id="89e10-103">SentToAddresses</span><span class="sxs-lookup"><span data-stu-id="89e10-103">SentToAddresses</span></span>

<span data-ttu-id="89e10-104">El elemento **SentToAddresses** indica las direcciones de correo electrónico a las que se deben enviar los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="89e10-104">The **SentToAddresses** element indicates the e-mail addresses that incoming messages have to have been sent to in order for the condition or exception to apply.</span></span> 
  
```XML
<SentToAddresses>
   <Address/>
</SentToAddresses>
```

 <span data-ttu-id="89e10-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="89e10-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="89e10-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="89e10-106">Attributes and elements</span></span>

<span data-ttu-id="89e10-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="89e10-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="89e10-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="89e10-108">Attributes</span></span>

<span data-ttu-id="89e10-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="89e10-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="89e10-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="89e10-110">Child elements</span></span>

|<span data-ttu-id="89e10-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="89e10-111">**Element**</span></span>|<span data-ttu-id="89e10-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="89e10-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89e10-113">Dirección (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="89e10-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="89e10-114">Representa una dirección de correo electrónico completamente resuelta.</span><span class="sxs-lookup"><span data-stu-id="89e10-114">Represents a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="89e10-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="89e10-115">Parent elements</span></span>

|<span data-ttu-id="89e10-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="89e10-116">**Element**</span></span>|<span data-ttu-id="89e10-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="89e10-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89e10-118">Condiciones</span><span class="sxs-lookup"><span data-stu-id="89e10-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="89e10-119">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="89e10-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="89e10-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="89e10-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="89e10-121">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="89e10-121">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="89e10-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="89e10-122">Text value</span></span>

<span data-ttu-id="89e10-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="89e10-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="89e10-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="89e10-124">Remarks</span></span>

<span data-ttu-id="89e10-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="89e10-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="89e10-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="89e10-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89e10-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="89e10-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="89e10-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="89e10-128">Schema Name</span></span>  <br/> |<span data-ttu-id="89e10-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="89e10-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="89e10-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="89e10-130">Validation File</span></span>  <br/> |<span data-ttu-id="89e10-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="89e10-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="89e10-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="89e10-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="89e10-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="89e10-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89e10-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="89e10-134">See also</span></span>



- [<span data-ttu-id="89e10-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="89e10-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

