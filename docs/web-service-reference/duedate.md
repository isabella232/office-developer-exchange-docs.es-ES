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
ms.openlocfilehash: b88bb5c64ee48e02b1600c6865ce650e7bcdaa3b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463562"
---
# <a name="duedate"></a><span data-ttu-id="c5392-103">DueDate</span><span class="sxs-lookup"><span data-stu-id="c5392-103">DueDate</span></span>

<span data-ttu-id="c5392-104">El elemento **DueDate** representa la fecha de vencimiento de un elemento.</span><span class="sxs-lookup"><span data-stu-id="c5392-104">The **DueDate** element represents the date an item is due.</span></span> 
  
```xml
<DueDate/>
```

 <span data-ttu-id="c5392-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="c5392-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c5392-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c5392-106">Attributes and elements</span></span>

<span data-ttu-id="c5392-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c5392-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5392-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c5392-108">Attributes</span></span>

<span data-ttu-id="c5392-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c5392-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c5392-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c5392-110">Child elements</span></span>

<span data-ttu-id="c5392-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c5392-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c5392-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c5392-112">Parent elements</span></span>

|<span data-ttu-id="c5392-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c5392-113">**Element**</span></span>|<span data-ttu-id="c5392-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c5392-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5392-115">Tarea</span><span class="sxs-lookup"><span data-stu-id="c5392-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="c5392-116">Representa una tarea del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="c5392-116">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="c5392-117">Flag</span><span class="sxs-lookup"><span data-stu-id="c5392-117">Flag</span></span>](flag.md) <br/> |<span data-ttu-id="c5392-118">Especifica una marca en un elemento de buzón.</span><span class="sxs-lookup"><span data-stu-id="c5392-118">Specifies a flag on a mailbox item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c5392-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="c5392-119">Text value</span></span>

<span data-ttu-id="c5392-120">Si se usa este elemento, se necesita un valor de texto que represente la fecha y la hora.</span><span class="sxs-lookup"><span data-stu-id="c5392-120">A text value that represents the date and time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5392-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c5392-121">Remarks</span></span>

<span data-ttu-id="c5392-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c5392-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5392-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c5392-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5392-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5392-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c5392-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c5392-125">Schema name</span></span>  <br/> |<span data-ttu-id="c5392-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="c5392-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="c5392-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c5392-127">Validation file</span></span>  <br/> |<span data-ttu-id="c5392-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="c5392-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c5392-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c5392-129">Can be empty</span></span>  <br/> |<span data-ttu-id="c5392-130">Falso</span><span class="sxs-lookup"><span data-stu-id="c5392-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5392-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5392-131">See also</span></span>

- [<span data-ttu-id="c5392-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c5392-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

