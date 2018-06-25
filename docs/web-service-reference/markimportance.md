---
title: MarkImportance
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MarkImportance
api_type:
- schema
ms.assetid: 32b8b08f-65e9-4764-b40a-63245551f4a3
description: El elemento MarkImportance especifica la importancia que se mostrará en los mensajes.
ms.openlocfilehash: 32b1fa63ef47327e7d3af717ed9f452e43b16380
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836356"
---
# <a name="markimportance"></a><span data-ttu-id="f9068-103">MarkImportance</span><span class="sxs-lookup"><span data-stu-id="f9068-103">MarkImportance</span></span>

<span data-ttu-id="f9068-104">El elemento **MarkImportance** especifica la importancia que se mostrará en los mensajes.</span><span class="sxs-lookup"><span data-stu-id="f9068-104">The **MarkImportance** element specifies the importance that is to be stamped on messages.</span></span> 
  
```XML
<MarkImportance/>
```

 <span data-ttu-id="f9068-105">**ImportanceChoicesType**</span><span class="sxs-lookup"><span data-stu-id="f9068-105">**ImportanceChoicesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f9068-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f9068-106">Attributes and elements</span></span>

<span data-ttu-id="f9068-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f9068-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f9068-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f9068-108">Attributes</span></span>

<span data-ttu-id="f9068-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f9068-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f9068-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f9068-110">Child elements</span></span>

<span data-ttu-id="f9068-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f9068-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f9068-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f9068-112">Parent elements</span></span>

|<span data-ttu-id="f9068-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="f9068-113">**Element**</span></span>|<span data-ttu-id="f9068-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f9068-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9068-115">Acciones</span><span class="sxs-lookup"><span data-stu-id="f9068-115">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="f9068-116">Representa el conjunto de acciones que están disponibles para ser tomadas en un mensaje cuando se cumplen las condiciones.</span><span class="sxs-lookup"><span data-stu-id="f9068-116">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f9068-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f9068-117">Text value</span></span>

<span data-ttu-id="f9068-118">El valor de texto para este elemento está restringido a uno de los siguientes valores de cadena:</span><span class="sxs-lookup"><span data-stu-id="f9068-118">The text value for this element is restricted to one of the following string values:</span></span>
  
- <span data-ttu-id="f9068-119">Low</span><span class="sxs-lookup"><span data-stu-id="f9068-119">Low</span></span>
    
- <span data-ttu-id="f9068-120">Importance</span><span class="sxs-lookup"><span data-stu-id="f9068-120">Normal</span></span>
    
- <span data-ttu-id="f9068-121">High</span><span class="sxs-lookup"><span data-stu-id="f9068-121">High</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f9068-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f9068-122">Remarks</span></span>

<span data-ttu-id="f9068-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f9068-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f9068-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f9068-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9068-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f9068-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f9068-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f9068-126">Schema Name</span></span>  <br/> |<span data-ttu-id="f9068-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f9068-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f9068-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f9068-128">Validation File</span></span>  <br/> |<span data-ttu-id="f9068-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f9068-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f9068-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f9068-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="f9068-131">Verdadero</span><span class="sxs-lookup"><span data-stu-id="f9068-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f9068-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9068-132">See also</span></span>



- [<span data-ttu-id="f9068-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f9068-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

