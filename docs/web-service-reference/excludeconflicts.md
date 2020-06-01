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
description: El elemento ExcludeConflicts especifica si se devuelven las horas sugeridas para las horas de calendario que entran en conflicto entre los asistentes.
ms.openlocfilehash: d20c594ae600abf110681ea678b2d95a23bf7809
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456979"
---
# <a name="excludeconflicts"></a><span data-ttu-id="641d7-103">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="641d7-103">ExcludeConflicts</span></span>

<span data-ttu-id="641d7-104">El elemento **ExcludeConflicts** especifica si se devuelven las horas sugeridas para las horas de calendario que entran en conflicto entre los asistentes.</span><span class="sxs-lookup"><span data-stu-id="641d7-104">The **ExcludeConflicts** element specifies whether to return suggested times for calendar times that conflict among the attendees.</span></span> 
  
[<span data-ttu-id="641d7-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="641d7-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="641d7-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="641d7-106">MailboxDataArray</span></span>](mailboxdataarray.md)
  
[<span data-ttu-id="641d7-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="641d7-107">MailboxData</span></span>](mailboxdata.md)
  
[<span data-ttu-id="641d7-108">ExcludeConflicts</span><span class="sxs-lookup"><span data-stu-id="641d7-108">ExcludeConflicts</span></span>](excludeconflicts.md)
  
```xml
<ExcludeConflicts>true or false</ExcludeConflicts>
```

 <span data-ttu-id="641d7-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="641d7-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="641d7-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="641d7-110">Attributes and elements</span></span>

<span data-ttu-id="641d7-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="641d7-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="641d7-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="641d7-112">Attributes</span></span>

<span data-ttu-id="641d7-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="641d7-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="641d7-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="641d7-114">Child elements</span></span>

<span data-ttu-id="641d7-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="641d7-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="641d7-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="641d7-116">Parent elements</span></span>

|<span data-ttu-id="641d7-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="641d7-117">**Element**</span></span>|<span data-ttu-id="641d7-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="641d7-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="641d7-119">MailboxData</span><span class="sxs-lookup"><span data-stu-id="641d7-119">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="641d7-120">Representa un usuario de buzón individual y opciones para el tipo de datos que se devolverán sobre el usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="641d7-120">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> <span data-ttu-id="641d7-121">A continuación se encuentra la expresión XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="641d7-121">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="641d7-122">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="641d7-122">Text value</span></span>

<span data-ttu-id="641d7-123">Se requiere un valor de texto.</span><span class="sxs-lookup"><span data-stu-id="641d7-123">A text value is required.</span></span> <span data-ttu-id="641d7-124">Los valores posibles son un valor booleano **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="641d7-124">The possible values are a Boolean **true** or **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="641d7-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="641d7-125">Remarks</span></span>

<span data-ttu-id="641d7-126">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="641d7-126">This element is required.</span></span>
  
> [!NOTE]
> <span data-ttu-id="641d7-127">El esquema que describe este elemento se encuentra en el directorio/EWS/del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="641d7-127">The schema that describes this element is located in the /EWS/ directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="641d7-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="641d7-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="641d7-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="641d7-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="641d7-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="641d7-130">Schema Name</span></span>  <br/> |<span data-ttu-id="641d7-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="641d7-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="641d7-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="641d7-132">Validation File</span></span>  <br/> |<span data-ttu-id="641d7-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="641d7-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="641d7-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="641d7-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="641d7-135">Falso</span><span class="sxs-lookup"><span data-stu-id="641d7-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="641d7-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="641d7-136">See also</span></span>



[<span data-ttu-id="641d7-137">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="641d7-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="641d7-138">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="641d7-138">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)


[<span data-ttu-id="641d7-139">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="641d7-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

