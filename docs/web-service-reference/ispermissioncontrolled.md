---
title: IsPermissionControlled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsPermissionControlled
api_type:
- schema
ms.assetid: a2fd0340-f31f-4389-a1cd-7e93b40bb3c6
description: El elemento IsPermissionControlled indica si los mensajes entrantes deben ser controlados por permisos (protegido por RMS) para que se aplique la condición o excepción.
ms.openlocfilehash: 5fba06c1c56512f4a362f773f119ea346a4c0d2b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460389"
---
# <a name="ispermissioncontrolled"></a><span data-ttu-id="ed58a-103">IsPermissionControlled</span><span class="sxs-lookup"><span data-stu-id="ed58a-103">IsPermissionControlled</span></span>

<span data-ttu-id="ed58a-104">El elemento **IsPermissionControlled** indica si los mensajes entrantes deben ser controlados por permisos (protegido por RMS) para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="ed58a-104">The **IsPermissionControlled** element indicates whether incoming messages must be permission controlled (RMS protected) in order for the condition or exception to apply.</span></span> 
  
```XML
<IsPermissionControlled>true | false</IsPermissionControlled>
```

 <span data-ttu-id="ed58a-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ed58a-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ed58a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ed58a-106">Attributes and elements</span></span>

<span data-ttu-id="ed58a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ed58a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ed58a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ed58a-108">Attributes</span></span>

<span data-ttu-id="ed58a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ed58a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ed58a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ed58a-110">Child elements</span></span>

<span data-ttu-id="ed58a-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ed58a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ed58a-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ed58a-112">Parent elements</span></span>

|<span data-ttu-id="ed58a-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ed58a-113">**Element**</span></span>|<span data-ttu-id="ed58a-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ed58a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ed58a-115">Condiciones</span><span class="sxs-lookup"><span data-stu-id="ed58a-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="ed58a-116">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="ed58a-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="ed58a-117">Excepciones</span><span class="sxs-lookup"><span data-stu-id="ed58a-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="ed58a-118">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="ed58a-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ed58a-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ed58a-119">Text value</span></span>

<span data-ttu-id="ed58a-120">Un valor de texto de **true** indica que el mensaje debe estar protegido por RMS para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="ed58a-120">A text value of **true** indicates that the message must be RMS protected in order for the condition or exception to apply.</span></span> <span data-ttu-id="ed58a-121">Un valor de **false** indica que el mensaje no debe estar protegido con RMS para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="ed58a-121">A value of **false** indicates that the message must not be RMS protected in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ed58a-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ed58a-122">Remarks</span></span>

<span data-ttu-id="ed58a-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ed58a-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ed58a-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ed58a-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed58a-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed58a-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ed58a-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ed58a-126">Schema Name</span></span>  <br/> |<span data-ttu-id="ed58a-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ed58a-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ed58a-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ed58a-128">Validation File</span></span>  <br/> |<span data-ttu-id="ed58a-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ed58a-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ed58a-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ed58a-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="ed58a-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="ed58a-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ed58a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed58a-132">See also</span></span>



- [<span data-ttu-id="ed58a-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ed58a-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

