---
title: DueDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DueDate
api_type:
- schema
ms.assetid: dd9b6c43-a512-4b3b-a071-4abde02ed55f
description: El elemento DueDate representa la fecha de vencimiento de un elemento.
ms.openlocfilehash: b24891972f240bc6ee5d0fe868445b96abdc089a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764285"
---
# <a name="duedate"></a><span data-ttu-id="139be-103">DueDate</span><span class="sxs-lookup"><span data-stu-id="139be-103">DueDate</span></span>

<span data-ttu-id="139be-104">El elemento **DueDate** representa la fecha de vencimiento de un elemento.</span><span class="sxs-lookup"><span data-stu-id="139be-104">The **DueDate** element represents the date an item is due.</span></span> 
  
```xml
<DueDate/>
```

 <span data-ttu-id="139be-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="139be-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="139be-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="139be-106">Attributes and elements</span></span>

<span data-ttu-id="139be-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="139be-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="139be-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="139be-108">Attributes</span></span>

<span data-ttu-id="139be-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="139be-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="139be-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="139be-110">Child elements</span></span>

<span data-ttu-id="139be-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="139be-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="139be-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="139be-112">Parent elements</span></span>

|<span data-ttu-id="139be-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="139be-113">**Element**</span></span>|<span data-ttu-id="139be-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="139be-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="139be-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="139be-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="139be-116">Representa una tarea en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="139be-116">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="139be-117">Flag</span><span class="sxs-lookup"><span data-stu-id="139be-117">Flag</span></span>](flag.md) <br/> |<span data-ttu-id="139be-118">Especifica una marca en un elemento de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="139be-118">Specifies a flag on a mailbox item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="139be-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="139be-119">Text value</span></span>

<span data-ttu-id="139be-120">Si se usa este elemento, es necesario un valor de texto que representa la fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="139be-120">A text value that represents the date and time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="139be-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="139be-121">Remarks</span></span>

<span data-ttu-id="139be-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="139be-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="139be-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="139be-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="139be-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="139be-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="139be-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="139be-125">Schema name</span></span>  <br/> |<span data-ttu-id="139be-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="139be-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="139be-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="139be-127">Validation file</span></span>  <br/> |<span data-ttu-id="139be-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="139be-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="139be-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="139be-129">Can be empty</span></span>  <br/> |<span data-ttu-id="139be-130">False</span><span class="sxs-lookup"><span data-stu-id="139be-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="139be-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="139be-131">See also</span></span>

- [<span data-ttu-id="139be-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="139be-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

