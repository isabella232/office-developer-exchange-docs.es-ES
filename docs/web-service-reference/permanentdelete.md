---
title: PermanentDelete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PermanentDelete
api_type:
- schema
ms.assetid: 1a0e0f46-1472-4eb7-bb54-f193a2603587
description: El elemento PermanentDelete indica si los mensajes se eliminan permanentemente y no se ha guardado en la carpeta Elementos eliminados.
ms.openlocfilehash: 40cf80e054bb70a3f6d687e8d4361f1d4331a7f8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836724"
---
# <a name="permanentdelete"></a><span data-ttu-id="e4d5d-103">PermanentDelete</span><span class="sxs-lookup"><span data-stu-id="e4d5d-103">PermanentDelete</span></span>

<span data-ttu-id="e4d5d-104">El elemento **PermanentDelete** indica si los mensajes se eliminan permanentemente y no se ha guardado en la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="e4d5d-104">The **PermanentDelete** element indicates whether messages are to be permanently deleted and not saved to the Deleted Items folder.</span></span> 
  
```XML
<PermanentDelete>true | false</PermanentDelete>
```

 <span data-ttu-id="e4d5d-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e4d5d-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e4d5d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e4d5d-106">Attributes and elements</span></span>

<span data-ttu-id="e4d5d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e4d5d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e4d5d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e4d5d-108">Attributes</span></span>

<span data-ttu-id="e4d5d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e4d5d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e4d5d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e4d5d-110">Child elements</span></span>

<span data-ttu-id="e4d5d-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e4d5d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e4d5d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e4d5d-112">Parent elements</span></span>

|<span data-ttu-id="e4d5d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e4d5d-113">**Element**</span></span>|<span data-ttu-id="e4d5d-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e4d5d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e4d5d-115">Acciones</span><span class="sxs-lookup"><span data-stu-id="e4d5d-115">Actions</span></span>](actions.md) <br/> |<span data-ttu-id="e4d5d-116">Representa el conjunto de acciones que están disponibles para ser tomadas en un mensaje cuando se cumplen las condiciones.</span><span class="sxs-lookup"><span data-stu-id="e4d5d-116">Represents the set of actions that are available to be taken on a message when the conditions are fulfilled.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e4d5d-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e4d5d-117">Text value</span></span>

<span data-ttu-id="e4d5d-118">Un valor de texto de **true** indica que el mensaje debe estar marcado para ser eliminado de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="e4d5d-118">A text value of **true** indicates that the message must be marked to be permanently deleted.</span></span> <span data-ttu-id="e4d5d-119">Un valor de **false** indica que el mensaje no debe estar marcado para eliminar de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="e4d5d-119">A value of **false** indicates that the message must not be marked to be permanently deleted.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e4d5d-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e4d5d-120">Remarks</span></span>

<span data-ttu-id="e4d5d-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e4d5d-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e4d5d-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e4d5d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e4d5d-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e4d5d-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e4d5d-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e4d5d-124">Schema Name</span></span>  <br/> |<span data-ttu-id="e4d5d-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e4d5d-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e4d5d-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e4d5d-126">Validation File</span></span>  <br/> |<span data-ttu-id="e4d5d-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e4d5d-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e4d5d-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e4d5d-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="e4d5d-129">Verdadero</span><span class="sxs-lookup"><span data-stu-id="e4d5d-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e4d5d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4d5d-130">See also</span></span>



- [<span data-ttu-id="e4d5d-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e4d5d-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

