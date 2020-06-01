---
title: IsEncrypted
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsEncrypted
api_type:
- schema
ms.assetid: 68a30e92-c2b1-4af5-bb16-ba38afb80c43
description: El elemento IsEncrypted indica si los mensajes entrantes deben ser cifrados con S/MIME para que se aplique la condición o excepción.
ms.openlocfilehash: 7470fa3163596f87badfda2ca698b096e02f1196
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455306"
---
# <a name="isencrypted"></a><span data-ttu-id="625a8-103">IsEncrypted</span><span class="sxs-lookup"><span data-stu-id="625a8-103">IsEncrypted</span></span>

<span data-ttu-id="625a8-104">El elemento **IsEncrypted** indica si los mensajes entrantes deben ser cifrados con S/MIME para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="625a8-104">The **IsEncrypted** element indicates whether incoming messages must be S/MIME encrypted in order for the condition or exception to apply.</span></span> 
  
```XML
<IsEncrypted>true | false</IsEncrypted>
```

 <span data-ttu-id="625a8-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="625a8-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="625a8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="625a8-106">Attributes and elements</span></span>

<span data-ttu-id="625a8-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="625a8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="625a8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="625a8-108">Attributes</span></span>

<span data-ttu-id="625a8-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="625a8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="625a8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="625a8-110">Child elements</span></span>

<span data-ttu-id="625a8-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="625a8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="625a8-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="625a8-112">Parent elements</span></span>

|<span data-ttu-id="625a8-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="625a8-113">**Element**</span></span>|<span data-ttu-id="625a8-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="625a8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="625a8-115">Condiciones</span><span class="sxs-lookup"><span data-stu-id="625a8-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="625a8-116">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.</span><span class="sxs-lookup"><span data-stu-id="625a8-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="625a8-117">Excepciones</span><span class="sxs-lookup"><span data-stu-id="625a8-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="625a8-118">Representa todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="625a8-118">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="625a8-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="625a8-119">Text value</span></span>

<span data-ttu-id="625a8-120">Un valor de texto de **true** indica que el mensaje debe estar cifrado con S/MIME para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="625a8-120">A text value of **true** indicates that the message must be S/MIME encrypted in order for the condition or exception to apply.</span></span> <span data-ttu-id="625a8-121">Un valor de **false** indica que el mensaje no tiene que ser S/MIME para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="625a8-121">A value of **false** indicates that the message does not have to be S/MIME in order for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="625a8-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="625a8-122">Remarks</span></span>

<span data-ttu-id="625a8-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="625a8-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="625a8-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="625a8-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="625a8-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="625a8-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="625a8-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="625a8-126">Schema Name</span></span>  <br/> |<span data-ttu-id="625a8-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="625a8-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="625a8-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="625a8-128">Validation File</span></span>  <br/> |<span data-ttu-id="625a8-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="625a8-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="625a8-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="625a8-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="625a8-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="625a8-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="625a8-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="625a8-132">See also</span></span>



- [<span data-ttu-id="625a8-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="625a8-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

