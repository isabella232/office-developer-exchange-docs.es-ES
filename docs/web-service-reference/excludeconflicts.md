---
title: ExcludeConflicts
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExcludeConflicts
api_type:
- schema
ms.assetid: ec33ef23-8537-41eb-8d89-7eb906a1fad7
description: El elemento ExcludeConflicts especifica si se deben devolver sugerida veces para tiempos de calendario que entre en conflicto entre los asistentes.
ms.openlocfilehash: 66b69d57246942e551de2f683949870823e2e4e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764476"
---
# <a name="excludeconflicts"></a><span data-ttu-id="65b83-103">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="65b83-103">ExcludeConflicts</span></span>

<span data-ttu-id="65b83-104">El elemento **ExcludeConflicts** especifica si se deben devolver sugerida veces para tiempos de calendario que entre en conflicto entre los asistentes.</span><span class="sxs-lookup"><span data-stu-id="65b83-104">The **ExcludeConflicts** element specifies whether to return suggested times for calendar times that conflict among the attendees.</span></span> 
  
[<span data-ttu-id="65b83-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="65b83-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="65b83-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="65b83-106">MailboxDataArray</span></span>](mailboxdataarray.md)
  
[<span data-ttu-id="65b83-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="65b83-107">MailboxData</span></span>](mailboxdata.md)
  
[<span data-ttu-id="65b83-108">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="65b83-108">ExcludeConflicts</span></span>](excludeconflicts.md)
  
```xml
<ExcludeConflicts>true or false</ExcludeConflicts>
```

 <span data-ttu-id="65b83-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="65b83-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="65b83-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="65b83-110">Attributes and elements</span></span>

<span data-ttu-id="65b83-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="65b83-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65b83-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="65b83-112">Attributes</span></span>

<span data-ttu-id="65b83-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="65b83-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="65b83-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="65b83-114">Child elements</span></span>

<span data-ttu-id="65b83-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="65b83-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="65b83-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="65b83-116">Parent elements</span></span>

|<span data-ttu-id="65b83-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="65b83-117">**Element**</span></span>|<span data-ttu-id="65b83-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65b83-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65b83-119">MailboxData</span><span class="sxs-lookup"><span data-stu-id="65b83-119">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="65b83-120">Representa un usuario de buzón de correo individual y opciones para el tipo de datos que se devolverá sobre el usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="65b83-120">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> <span data-ttu-id="65b83-121">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="65b83-121">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="65b83-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="65b83-122">Text value</span></span>

<span data-ttu-id="65b83-123">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="65b83-123">A text value is required.</span></span> <span data-ttu-id="65b83-124">Los valores posibles son un valor booleano **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="65b83-124">The possible values are a Boolean **true** or **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="65b83-125">Notas</span><span class="sxs-lookup"><span data-stu-id="65b83-125">Remarks</span></span>

<span data-ttu-id="65b83-126">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="65b83-126">This element is required.</span></span>
  
> [!NOTE]
> <span data-ttu-id="65b83-127">El esquema que describe este elemento se encuentra en el directorio /EWS/ del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="65b83-127">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="65b83-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="65b83-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65b83-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="65b83-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="65b83-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="65b83-130">Schema Name</span></span>  <br/> |<span data-ttu-id="65b83-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="65b83-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="65b83-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="65b83-132">Validation File</span></span>  <br/> |<span data-ttu-id="65b83-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="65b83-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="65b83-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="65b83-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="65b83-135">False</span><span class="sxs-lookup"><span data-stu-id="65b83-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65b83-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="65b83-136">See also</span></span>



[<span data-ttu-id="65b83-137">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="65b83-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="65b83-138">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="65b83-138">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)


[<span data-ttu-id="65b83-139">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="65b83-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

