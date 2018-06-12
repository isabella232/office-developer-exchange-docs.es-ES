---
title: ReturnQueueEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReturnQueueEvents
api_type:
- schema
ms.assetid: 69d22417-320c-4c6f-9fb4-2020f2480bb2
description: El elemento ReturnQueueEvents indica que la persona que está ejecutando la tarea está en una función con privilegios.
ms.openlocfilehash: 02f4ca86ffa14117105ec186ae039065cb626670
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837233"
---
# <a name="returnqueueevents"></a><span data-ttu-id="6a2bd-103">ReturnQueueEvents</span><span class="sxs-lookup"><span data-stu-id="6a2bd-103">ReturnQueueEvents</span></span>

<span data-ttu-id="6a2bd-104">El elemento **ReturnQueueEvents** indica que la persona que está ejecutando la tarea está en una función con privilegios.</span><span class="sxs-lookup"><span data-stu-id="6a2bd-104">The **ReturnQueueEvents** element indicates that the person who is running the task is in a privileged role.</span></span> 
  
```XML
<ReturnQueueEvents>true | false</ReturnQueueEvents>
```

 <span data-ttu-id="6a2bd-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6a2bd-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6a2bd-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6a2bd-106">Attributes and elements</span></span>

<span data-ttu-id="6a2bd-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6a2bd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6a2bd-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6a2bd-108">Attributes</span></span>

<span data-ttu-id="6a2bd-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6a2bd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6a2bd-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6a2bd-110">Child elements</span></span>

<span data-ttu-id="6a2bd-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6a2bd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6a2bd-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6a2bd-112">Parent elements</span></span>

|<span data-ttu-id="6a2bd-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="6a2bd-113">**Element**</span></span>|<span data-ttu-id="6a2bd-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6a2bd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6a2bd-115">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="6a2bd-115">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="6a2bd-116">Contiene la solicitud para la [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md) recuperar el mensaje completo informe de seguimiento para el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="6a2bd-116">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6a2bd-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6a2bd-117">Text value</span></span>

<span data-ttu-id="6a2bd-118">Se requiere un valor de texto que representa un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="6a2bd-118">A text value that represents a Boolean value is required.</span></span> <span data-ttu-id="6a2bd-119">Un valor de **true** indica que la persona que está ejecutando la tarea está en una función con privilegios; un valor de **false** indica que la persona que ejecuta la tarea no está en una función que tiene privilegios.</span><span class="sxs-lookup"><span data-stu-id="6a2bd-119">A value of **true** indicates that the person who is running the task is in a privileged role; a value of **false** indicates that the person who is running the task is not in a privileged role.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6a2bd-120">Notas</span><span class="sxs-lookup"><span data-stu-id="6a2bd-120">Remarks</span></span>

<span data-ttu-id="6a2bd-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6a2bd-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6a2bd-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6a2bd-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6a2bd-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6a2bd-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6a2bd-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6a2bd-124">Schema Name</span></span>  <br/> |<span data-ttu-id="6a2bd-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="6a2bd-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6a2bd-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6a2bd-126">Validation File</span></span>  <br/> |<span data-ttu-id="6a2bd-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6a2bd-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6a2bd-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6a2bd-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="6a2bd-129">False</span><span class="sxs-lookup"><span data-stu-id="6a2bd-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6a2bd-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="6a2bd-130">See also</span></span>



[<span data-ttu-id="6a2bd-131">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="6a2bd-131">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="6a2bd-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="6a2bd-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

