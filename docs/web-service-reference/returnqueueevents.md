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
description: El elemento ReturnQueueEvents indica que la persona que ejecuta la tarea está en un rol privilegiado.
ms.openlocfilehash: 9d07bc8c3d32f1cd532febaf4ae04e4a2d31d243
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466594"
---
# <a name="returnqueueevents"></a><span data-ttu-id="fa3a9-103">ReturnQueueEvents</span><span class="sxs-lookup"><span data-stu-id="fa3a9-103">ReturnQueueEvents</span></span>

<span data-ttu-id="fa3a9-104">El elemento **ReturnQueueEvents** indica que la persona que ejecuta la tarea está en un rol privilegiado.</span><span class="sxs-lookup"><span data-stu-id="fa3a9-104">The **ReturnQueueEvents** element indicates that the person who is running the task is in a privileged role.</span></span> 
  
```XML
<ReturnQueueEvents>true | false</ReturnQueueEvents>
```

 <span data-ttu-id="fa3a9-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="fa3a9-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa3a9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="fa3a9-106">Attributes and elements</span></span>

<span data-ttu-id="fa3a9-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="fa3a9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa3a9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fa3a9-108">Attributes</span></span>

<span data-ttu-id="fa3a9-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fa3a9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa3a9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="fa3a9-110">Child elements</span></span>

<span data-ttu-id="fa3a9-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="fa3a9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fa3a9-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="fa3a9-112">Parent elements</span></span>

|<span data-ttu-id="fa3a9-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fa3a9-113">**Element**</span></span>|<span data-ttu-id="fa3a9-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fa3a9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa3a9-115">GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="fa3a9-115">GetMessageTrackingReport</span></span>](getmessagetrackingreport.md) <br/> |<span data-ttu-id="fa3a9-116">Contiene la solicitud de la [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md) para recuperar el informe completo de seguimiento de mensajes del identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="fa3a9-116">Contains the request for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md) to retrieve the full message tracking report for the specified ID.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fa3a9-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="fa3a9-117">Text value</span></span>

<span data-ttu-id="fa3a9-118">Se requiere un valor de texto que representa un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="fa3a9-118">A text value that represents a Boolean value is required.</span></span> <span data-ttu-id="fa3a9-119">Un valor de **true** indica que la persona que ejecuta la tarea está en una función privilegiada; un valor de **false** indica que la persona que ejecuta la tarea no tiene un rol privilegiado.</span><span class="sxs-lookup"><span data-stu-id="fa3a9-119">A value of **true** indicates that the person who is running the task is in a privileged role; a value of **false** indicates that the person who is running the task is not in a privileged role.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fa3a9-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fa3a9-120">Remarks</span></span>

<span data-ttu-id="fa3a9-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="fa3a9-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa3a9-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="fa3a9-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa3a9-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa3a9-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fa3a9-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="fa3a9-124">Schema Name</span></span>  <br/> |<span data-ttu-id="fa3a9-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="fa3a9-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fa3a9-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="fa3a9-126">Validation File</span></span>  <br/> |<span data-ttu-id="fa3a9-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="fa3a9-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fa3a9-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="fa3a9-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="fa3a9-129">Falso</span><span class="sxs-lookup"><span data-stu-id="fa3a9-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa3a9-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa3a9-130">See also</span></span>



[<span data-ttu-id="fa3a9-131">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="fa3a9-131">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="fa3a9-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="fa3a9-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

