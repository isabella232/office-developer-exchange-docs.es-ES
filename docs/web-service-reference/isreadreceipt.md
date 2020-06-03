---
title: IsReadReceipt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsReadReceipt
api_type:
- schema
ms.assetid: e60e525f-c136-469a-b68b-b3dc01f400a6
description: El elemento IsReadReceipt indica si los mensajes entrantes deben ser confirmaciones de lectura para que se aplique la condición o excepción.
ms.openlocfilehash: e86a7776bc43204dae9fc92f21d4304255ddb888
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463905"
---
# <a name="isreadreceipt"></a><span data-ttu-id="3d260-103">IsReadReceipt</span><span class="sxs-lookup"><span data-stu-id="3d260-103">IsReadReceipt</span></span>

<span data-ttu-id="3d260-104">El elemento **IsReadReceipt** indica si los mensajes entrantes deben ser confirmaciones de lectura para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="3d260-104">The **IsReadReceipt** element indicates whether incoming messages must be read receipts in order for the condition or exception to apply.</span></span> 
  
```XML
<IsReadReceipt> true | false</IsReadReceipt>
```

 <span data-ttu-id="3d260-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3d260-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3d260-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3d260-106">Attributes and elements</span></span>

<span data-ttu-id="3d260-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3d260-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3d260-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3d260-108">Attributes</span></span>

<span data-ttu-id="3d260-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3d260-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3d260-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3d260-110">Child elements</span></span>

<span data-ttu-id="3d260-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3d260-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3d260-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3d260-112">Parent elements</span></span>

|<span data-ttu-id="3d260-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3d260-113">**Element**</span></span>|<span data-ttu-id="3d260-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3d260-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3d260-115">Condiciones</span><span class="sxs-lookup"><span data-stu-id="3d260-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="3d260-116">Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla para esa regla.</span><span class="sxs-lookup"><span data-stu-id="3d260-116">Represents the conditions that, when fulfilled, will trigger the rule actions for that rule.</span></span>  <br/> |
|[<span data-ttu-id="3d260-117">Excepciones</span><span class="sxs-lookup"><span data-stu-id="3d260-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="3d260-118">Representa todas las condiciones de excepción de regla disponibles para la regla de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="3d260-118">Represents all the available rule exception conditions for the Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3d260-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3d260-119">Text value</span></span>

<span data-ttu-id="3d260-120">Un valor de texto de **true** indica que el mensaje debe ser una confirmación de lectura para que se aplique la condición o excepción.</span><span class="sxs-lookup"><span data-stu-id="3d260-120">A text value of **true** indicates that the message must be a read receipt in order for the condition or exception to apply.</span></span> <span data-ttu-id="3d260-121">Si el mensaje no tiene que ser una confirmación de lectura de la condición o excepción que se va a aplicar, el valor es **false**.</span><span class="sxs-lookup"><span data-stu-id="3d260-121">If the message does not have to be a read receipt for the condition or exception to apply, the value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3d260-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3d260-122">Remarks</span></span>

<span data-ttu-id="3d260-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3d260-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3d260-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3d260-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3d260-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="3d260-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3d260-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3d260-126">Schema Name</span></span>  <br/> |<span data-ttu-id="3d260-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3d260-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3d260-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3d260-128">Validation File</span></span>  <br/> |<span data-ttu-id="3d260-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3d260-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3d260-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3d260-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="3d260-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="3d260-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3d260-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d260-132">See also</span></span>



- [<span data-ttu-id="3d260-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="3d260-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

