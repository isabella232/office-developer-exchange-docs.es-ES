---
title: ServerReplyWithMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ServerReplyWithMessage
api_type:
- schema
ms.assetid: 113c6ff2-9592-44f0-b542-54e4d5122ccb
description: El elemento ServerReplyWithMessage indica el identificador de la plantilla del mensaje de que se envía como una respuesta a los mensajes entrantes.
ms.openlocfilehash: f2d927ae18ac68523d4cdd173f0474fbbeb36c98
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837390"
---
# <a name="serverreplywithmessage"></a><span data-ttu-id="340ee-103">ServerReplyWithMessage</span><span class="sxs-lookup"><span data-stu-id="340ee-103">ServerReplyWithMessage</span></span>

<span data-ttu-id="340ee-104">El elemento **ServerReplyWithMessage** indica el identificador de la plantilla del mensaje de que se envía como una respuesta a los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="340ee-104">The **ServerReplyWithMessage** element indicates the ID of the template message that is to be sent as a reply to incoming messages.</span></span> 
  
```XML
<ServerReplyWithMessage>
    <ItemId>
</ServerReplyWithMessage>
```

 <span data-ttu-id="340ee-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="340ee-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="340ee-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="340ee-106">Attributes and elements</span></span>

<span data-ttu-id="340ee-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="340ee-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="340ee-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="340ee-108">Attributes</span></span>

<span data-ttu-id="340ee-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="340ee-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="340ee-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="340ee-110">Child elements</span></span>

|<span data-ttu-id="340ee-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="340ee-111">**Element**</span></span>|<span data-ttu-id="340ee-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="340ee-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="340ee-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="340ee-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="340ee-114">Representa el único identificador y cambiar la clave de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="340ee-114">Represents the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="340ee-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="340ee-115">Parent elements</span></span>

|<span data-ttu-id="340ee-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="340ee-116">**Element**</span></span>|<span data-ttu-id="340ee-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="340ee-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="340ee-118">Acciones</span><span class="sxs-lookup"><span data-stu-id="340ee-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="340ee-119">Representa el conjunto de acciones que están disponibles para ser tomadas en un mensaje cuando se cumplen las condiciones.</span><span class="sxs-lookup"><span data-stu-id="340ee-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="340ee-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="340ee-120">Text value</span></span>

<span data-ttu-id="340ee-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="340ee-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="340ee-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="340ee-122">Remarks</span></span>

<span data-ttu-id="340ee-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="340ee-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="340ee-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="340ee-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="340ee-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="340ee-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="340ee-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="340ee-126">Schema Name</span></span>  <br/> |<span data-ttu-id="340ee-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="340ee-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="340ee-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="340ee-128">Validation File</span></span>  <br/> |<span data-ttu-id="340ee-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="340ee-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="340ee-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="340ee-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="340ee-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="340ee-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="340ee-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="340ee-132">See also</span></span>



- [<span data-ttu-id="340ee-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="340ee-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

