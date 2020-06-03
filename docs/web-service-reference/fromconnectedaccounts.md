---
title: FromConnectedAccounts
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FromConnectedAccounts
api_type:
- schema
ms.assetid: d4d7ddd7-078d-4f1a-a26b-22dce0c49f3a
description: El elemento FromConnectedAccounts representa los nombres de cuenta de correo electrónico desde los que se deben agregar los mensajes entrantes para que se aplique la condición o excepción.
ms.openlocfilehash: 159ae064827c2f9c2b470580ad5457264e8dae93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464052"
---
# <a name="fromconnectedaccounts"></a><span data-ttu-id="59a70-103">FromConnectedAccounts</span><span class="sxs-lookup"><span data-stu-id="59a70-103">FromConnectedAccounts</span></span>

<span data-ttu-id="59a70-104">El elemento **FromConnectedAccounts** representa los nombres de cuenta de correo electrónico desde los que se deben agregar los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="59a70-104">The **FromConnectedAccounts** element represents the e-mail account names from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span> 
  
```XML
<FromConnectedAccounts>
    <String/>
</FromConnectedAccounts>
```

 <span data-ttu-id="59a70-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="59a70-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="59a70-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="59a70-106">Attributes and elements</span></span>

<span data-ttu-id="59a70-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="59a70-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="59a70-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="59a70-108">Attributes</span></span>

<span data-ttu-id="59a70-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="59a70-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="59a70-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="59a70-110">Child elements</span></span>

|<span data-ttu-id="59a70-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="59a70-111">**Element**</span></span>|<span data-ttu-id="59a70-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="59a70-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59a70-113">String</span><span class="sxs-lookup"><span data-stu-id="59a70-113">String</span></span>](string.md) <br/> |<span data-ttu-id="59a70-114">Representa un nombre de cuenta de correo electrónico desde el que se deben agregar los mensajes entrantes para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="59a70-114">Represents an e-mail account name from which incoming messages have to have been aggregated in order for the condition or exception to apply.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="59a70-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="59a70-115">Parent elements</span></span>

|<span data-ttu-id="59a70-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="59a70-116">**Element**</span></span>|<span data-ttu-id="59a70-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="59a70-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="59a70-118">Condiciones</span><span class="sxs-lookup"><span data-stu-id="59a70-118">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="59a70-119">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="59a70-119">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="59a70-120">Excepciones</span><span class="sxs-lookup"><span data-stu-id="59a70-120">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="59a70-121">Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="59a70-121">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="59a70-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="59a70-122">Text value</span></span>

<span data-ttu-id="59a70-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="59a70-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="59a70-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="59a70-124">Remarks</span></span>

<span data-ttu-id="59a70-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="59a70-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="59a70-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="59a70-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59a70-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="59a70-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="59a70-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="59a70-128">Schema Name</span></span>  <br/> |<span data-ttu-id="59a70-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="59a70-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="59a70-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="59a70-130">Validation File</span></span>  <br/> |<span data-ttu-id="59a70-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="59a70-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="59a70-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="59a70-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="59a70-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="59a70-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="59a70-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="59a70-134">See also</span></span>



- [<span data-ttu-id="59a70-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="59a70-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

