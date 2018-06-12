---
title: Organizador
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Organizer
api_type:
- schema
ms.assetid: 63892b57-3805-4d60-b9f7-20552a69c241
description: El elemento del organizador representa el organizador de una reunión.
ms.openlocfilehash: b723578a1b52cd5f6e9bd869a15430453adfa291
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836662"
---
# <a name="organizer"></a><span data-ttu-id="d6884-103">Organizador</span><span class="sxs-lookup"><span data-stu-id="d6884-103">Organizer</span></span>

<span data-ttu-id="d6884-104">El elemento del **Organizador** representa el organizador de una reunión.</span><span class="sxs-lookup"><span data-stu-id="d6884-104">The **Organizer** element represents the organizer of a meeting.</span></span> 
  
```xml
<Organizer>
   <Mailbox/>
</Organizer>
```

<span data-ttu-id="d6884-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="d6884-105">**SingleRecipientType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d6884-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d6884-106">Attributes and elements</span></span>

<span data-ttu-id="d6884-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d6884-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d6884-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d6884-108">Attributes</span></span>

<span data-ttu-id="d6884-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d6884-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d6884-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d6884-110">Child elements</span></span>

|<span data-ttu-id="d6884-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6884-111">**Element**</span></span>|<span data-ttu-id="d6884-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d6884-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d6884-113">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="d6884-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="d6884-114">Identifica un objeto de servicio de directorio de Active Directory habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="d6884-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d6884-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d6884-115">Parent elements</span></span>

|<span data-ttu-id="d6884-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6884-116">**Element**</span></span>|<span data-ttu-id="d6884-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d6884-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d6884-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="d6884-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="d6884-119">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d6884-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d6884-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="d6884-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="d6884-121">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="d6884-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d6884-122">Notas</span><span class="sxs-lookup"><span data-stu-id="d6884-122">Remarks</span></span>

<span data-ttu-id="d6884-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="d6884-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d6884-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d6884-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6884-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d6884-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d6884-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d6884-126">Schema name</span></span>  <br/> |<span data-ttu-id="d6884-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d6884-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="d6884-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d6884-128">Validation file</span></span>  <br/> |<span data-ttu-id="d6884-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d6884-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d6884-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d6884-130">Can be empty</span></span>  <br/> |<span data-ttu-id="d6884-131">False</span><span class="sxs-lookup"><span data-stu-id="d6884-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6884-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="d6884-132">See also</span></span>

- [<span data-ttu-id="d6884-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="d6884-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

