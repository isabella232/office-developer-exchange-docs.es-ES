---
title: MarkAsRead
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MarkAsRead
api_type:
- schema
ms.assetid: 404842e1-fbdb-480d-a1d8-ba1ab2c9fb1e
description: El elemento MarkAsRead indica si los mensajes se marcan como leídos.
ms.openlocfilehash: b453ad73912e99b6fd3aed84b03a7d2fc2b6a294
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836355"
---
# <a name="markasread"></a><span data-ttu-id="ba4a0-103">MarkAsRead</span><span class="sxs-lookup"><span data-stu-id="ba4a0-103">MarkAsRead</span></span>

<span data-ttu-id="ba4a0-104">El elemento **MarkAsRead** indica si los mensajes se marcan como leídos.</span><span class="sxs-lookup"><span data-stu-id="ba4a0-104">The **MarkAsRead** element indicates whether messages are to be marked as read.</span></span> 
  
```XML
<MarkAsRead>true | false</MarkAsRead>
```

 <span data-ttu-id="ba4a0-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ba4a0-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba4a0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ba4a0-106">Attributes and elements</span></span>

<span data-ttu-id="ba4a0-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ba4a0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba4a0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ba4a0-108">Attributes</span></span>

<span data-ttu-id="ba4a0-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ba4a0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba4a0-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ba4a0-110">Child elements</span></span>

<span data-ttu-id="ba4a0-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ba4a0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ba4a0-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ba4a0-112">Parent elements</span></span>

|<span data-ttu-id="ba4a0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba4a0-113">**Element**</span></span>|<span data-ttu-id="ba4a0-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ba4a0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba4a0-115">Acciones</span><span class="sxs-lookup"><span data-stu-id="ba4a0-115">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="ba4a0-116">Representa el conjunto de acciones que están disponibles para ser tomadas en un mensaje cuando se cumplen las condiciones.</span><span class="sxs-lookup"><span data-stu-id="ba4a0-116">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ba4a0-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ba4a0-117">Text value</span></span>

<span data-ttu-id="ba4a0-118">Un valor de texto de **true** indica que el mensaje debe estar marcado como leídos.</span><span class="sxs-lookup"><span data-stu-id="ba4a0-118">A text value of **true** indicates that the message must be marked as read.</span></span> <span data-ttu-id="ba4a0-119">Un valor de **false** indica que los mensajes no deben estar marcados como leídos.</span><span class="sxs-lookup"><span data-stu-id="ba4a0-119">A value of **false** indicates that messages must not be marked as read.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ba4a0-120">Notas</span><span class="sxs-lookup"><span data-stu-id="ba4a0-120">Remarks</span></span>

<span data-ttu-id="ba4a0-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ba4a0-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba4a0-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ba4a0-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba4a0-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ba4a0-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ba4a0-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ba4a0-124">Schema Name</span></span>  <br/> |<span data-ttu-id="ba4a0-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ba4a0-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ba4a0-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ba4a0-126">Validation File</span></span>  <br/> |<span data-ttu-id="ba4a0-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ba4a0-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ba4a0-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ba4a0-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="ba4a0-129">Verdadero</span><span class="sxs-lookup"><span data-stu-id="ba4a0-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba4a0-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="ba4a0-130">See also</span></span>



- [<span data-ttu-id="ba4a0-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ba4a0-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

