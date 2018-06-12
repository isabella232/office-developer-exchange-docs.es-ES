---
title: Fuera de la oficina
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OutOfOffice
api_type:
- schema
ms.assetid: fe1256ab-5c0f-467d-abb3-b38a2dc312ae
description: El elemento de fuera de la oficina representa el mensaje de respuesta y un tiempo de duración para enviar el mensaje de respuesta.
ms.openlocfilehash: 4e1e06ee332c44aeba03e1343c8c3258a2c9631e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836675"
---
# <a name="outofoffice"></a><span data-ttu-id="23f16-103">Fuera de la oficina</span><span class="sxs-lookup"><span data-stu-id="23f16-103">OutOfOffice</span></span>

<span data-ttu-id="23f16-104">El elemento de **fuera de la oficina** representa el mensaje de respuesta y un tiempo de duración para enviar el mensaje de respuesta.</span><span class="sxs-lookup"><span data-stu-id="23f16-104">The **OutOfOffice** element represents the response message and a duration time for sending the response message.</span></span> 
  
```XML
<OutOfOffice>
   <ReplyBody/>
   <Duration/>
</OutOfOffice>
```

 <span data-ttu-id="23f16-105">**OutOfOfficeMailTip**</span><span class="sxs-lookup"><span data-stu-id="23f16-105">**OutOfOfficeMailTip**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="23f16-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="23f16-106">Attributes and elements</span></span>

<span data-ttu-id="23f16-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="23f16-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="23f16-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="23f16-108">Attributes</span></span>

<span data-ttu-id="23f16-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="23f16-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="23f16-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="23f16-110">Child elements</span></span>

|<span data-ttu-id="23f16-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="23f16-111">**Element**</span></span>|<span data-ttu-id="23f16-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="23f16-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23f16-113">ReplyBody</span><span class="sxs-lookup"><span data-stu-id="23f16-113">ReplyBody</span></span>](replybody.md) <br/> |<span data-ttu-id="23f16-114">Contiene un mensaje de fuera de oficina (OOF) y el idioma utilizado para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="23f16-114">Contains an Out of Office (OOF) message and the language used for the message.</span></span>  <br/> |
|[<span data-ttu-id="23f16-115">Duración (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="23f16-115">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> |<span data-ttu-id="23f16-116">Contiene la duración que está habilitado el estado de fuera de la oficina si el elemento [OofState](oofstate.md) está establecido en programado.</span><span class="sxs-lookup"><span data-stu-id="23f16-116">Contains the duration that the OOF status is enabled if the [OofState](oofstate.md) element is set to Scheduled.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="23f16-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="23f16-117">Parent elements</span></span>

|<span data-ttu-id="23f16-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="23f16-118">**Element**</span></span>|<span data-ttu-id="23f16-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="23f16-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23f16-120">Sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="23f16-120">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="23f16-121">Representa los valores de distintos tipos de sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="23f16-121">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="23f16-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="23f16-122">Text value</span></span>

<span data-ttu-id="23f16-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="23f16-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="23f16-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="23f16-124">Remarks</span></span>

<span data-ttu-id="23f16-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="23f16-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="23f16-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="23f16-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23f16-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="23f16-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="23f16-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="23f16-128">Schema Name</span></span>  <br/> |<span data-ttu-id="23f16-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="23f16-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="23f16-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="23f16-130">Validation File</span></span>  <br/> |<span data-ttu-id="23f16-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="23f16-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="23f16-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="23f16-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="23f16-133">False</span><span class="sxs-lookup"><span data-stu-id="23f16-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="23f16-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="23f16-134">See also</span></span>



- [<span data-ttu-id="23f16-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="23f16-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

