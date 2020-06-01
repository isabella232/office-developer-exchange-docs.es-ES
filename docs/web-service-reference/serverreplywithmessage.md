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
description: El elemento ServerReplyWithMessage indica el identificador del mensaje de plantilla que se va a enviar como respuesta a los mensajes entrantes.
ms.openlocfilehash: faaa054018a17be3ff59b9fc385b3d846d39c3f1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461978"
---
# <a name="serverreplywithmessage"></a><span data-ttu-id="1d6cd-103">ServerReplyWithMessage</span><span class="sxs-lookup"><span data-stu-id="1d6cd-103">ServerReplyWithMessage</span></span>

<span data-ttu-id="1d6cd-104">El elemento **ServerReplyWithMessage** indica el identificador del mensaje de plantilla que se va a enviar como respuesta a los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-104">The **ServerReplyWithMessage** element indicates the ID of the template message that is to be sent as a reply to incoming messages.</span></span> 
  
```XML
<ServerReplyWithMessage>
    <ItemId>
</ServerReplyWithMessage>
```

 <span data-ttu-id="1d6cd-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="1d6cd-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1d6cd-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1d6cd-106">Attributes and elements</span></span>

<span data-ttu-id="1d6cd-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d6cd-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1d6cd-108">Attributes</span></span>

<span data-ttu-id="1d6cd-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1d6cd-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1d6cd-110">Child elements</span></span>

|<span data-ttu-id="1d6cd-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1d6cd-111">**Element**</span></span>|<span data-ttu-id="1d6cd-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d6cd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d6cd-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="1d6cd-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="1d6cd-114">Representa el identificador único y la clave de cambio de un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-114">Represents the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1d6cd-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1d6cd-115">Parent elements</span></span>

|<span data-ttu-id="1d6cd-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1d6cd-116">**Element**</span></span>|<span data-ttu-id="1d6cd-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1d6cd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d6cd-118">Actions</span><span class="sxs-lookup"><span data-stu-id="1d6cd-118">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="1d6cd-119">Representa el conjunto de acciones que se pueden realizar en un mensaje cuando se cumplen las condiciones.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-119">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1d6cd-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1d6cd-120">Text value</span></span>

<span data-ttu-id="1d6cd-121">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1d6cd-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1d6cd-122">Remarks</span></span>

<span data-ttu-id="1d6cd-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d6cd-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1d6cd-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d6cd-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d6cd-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1d6cd-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1d6cd-126">Schema Name</span></span>  <br/> |<span data-ttu-id="1d6cd-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1d6cd-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1d6cd-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1d6cd-128">Validation File</span></span>  <br/> |<span data-ttu-id="1d6cd-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="1d6cd-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1d6cd-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1d6cd-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="1d6cd-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="1d6cd-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d6cd-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d6cd-132">See also</span></span>



- [<span data-ttu-id="1d6cd-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="1d6cd-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

