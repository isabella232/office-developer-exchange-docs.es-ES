---
title: IsVoicemail
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsVoicemail
api_type:
- schema
ms.assetid: 96d81d6e-4b75-43ad-b151-2dd4fd57db94
description: El elemento IsVoicemail indica si los mensajes entrantes deben ser mensajes de correo de voz en orden para que se aplique la condición o excepción.
ms.openlocfilehash: 8c60513a54cbf2398fde4b71ab1fbcf8a5efb608
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458141"
---
# <a name="isvoicemail"></a><span data-ttu-id="57278-103">IsVoicemail</span><span class="sxs-lookup"><span data-stu-id="57278-103">IsVoicemail</span></span>

<span data-ttu-id="57278-104">El elemento **IsVoicemail** indica si los mensajes entrantes deben ser mensajes de correo de voz en orden para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="57278-104">The **IsVoicemail** element indicates whether incoming messages must be voice mail messages in order for the condition or exception to apply.</span></span> 
  
```XML
<IsVoicemail>true | false</IsVoicemail>
```

 <span data-ttu-id="57278-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="57278-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="57278-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="57278-106">Attributes and elements</span></span>

<span data-ttu-id="57278-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="57278-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="57278-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="57278-108">Attributes</span></span>

<span data-ttu-id="57278-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="57278-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="57278-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="57278-110">Child elements</span></span>

<span data-ttu-id="57278-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="57278-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="57278-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="57278-112">Parent elements</span></span>

|<span data-ttu-id="57278-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="57278-113">**Element**</span></span>|<span data-ttu-id="57278-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="57278-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="57278-115">Condiciones</span><span class="sxs-lookup"><span data-stu-id="57278-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="57278-116">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="57278-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="57278-117">Excepciones</span><span class="sxs-lookup"><span data-stu-id="57278-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="57278-118">Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="57278-118">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="57278-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="57278-119">Text value</span></span>

<span data-ttu-id="57278-120">Un valor de texto de **true** indica que el mensaje debe ser un mensaje de correo de voz para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="57278-120">A text value of **true** indicates that the message must be a voice mail message in order for the condition or exception to apply.</span></span> <span data-ttu-id="57278-121">Un valor de **false** indica que el mensaje no debe ser un mensaje de correo de voz para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="57278-121">A value of **false** indicates that the message must not be a voice mail message in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="57278-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="57278-122">Remarks</span></span>

<span data-ttu-id="57278-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="57278-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="57278-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="57278-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="57278-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="57278-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="57278-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="57278-126">Schema Name</span></span>  <br/> |<span data-ttu-id="57278-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="57278-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="57278-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="57278-128">Validation File</span></span>  <br/> |<span data-ttu-id="57278-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="57278-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="57278-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="57278-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="57278-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="57278-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="57278-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="57278-132">See also</span></span>



- [<span data-ttu-id="57278-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="57278-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

