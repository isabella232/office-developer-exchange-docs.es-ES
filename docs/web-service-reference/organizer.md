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
description: El elemento Organizer representa el organizador de una reunión.
ms.openlocfilehash: c1188c9b3a894e86a08b8869045c3647e394f506
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462419"
---
# <a name="organizer"></a><span data-ttu-id="6f797-103">Organizador</span><span class="sxs-lookup"><span data-stu-id="6f797-103">Organizer</span></span>

<span data-ttu-id="6f797-104">El elemento **Organizer** representa el organizador de una reunión.</span><span class="sxs-lookup"><span data-stu-id="6f797-104">The **Organizer** element represents the organizer of a meeting.</span></span> 
  
```xml
<Organizer>
   <Mailbox/>
</Organizer>
```

<span data-ttu-id="6f797-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="6f797-105">**SingleRecipientType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6f797-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6f797-106">Attributes and elements</span></span>

<span data-ttu-id="6f797-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6f797-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f797-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6f797-108">Attributes</span></span>

<span data-ttu-id="6f797-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6f797-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f797-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6f797-110">Child elements</span></span>

|<span data-ttu-id="6f797-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6f797-111">**Element**</span></span>|<span data-ttu-id="6f797-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f797-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f797-113">Buzón</span><span class="sxs-lookup"><span data-stu-id="6f797-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="6f797-114">Identifica un objeto de servicio de directorio de Active Directory habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="6f797-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6f797-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6f797-115">Parent elements</span></span>

|<span data-ttu-id="6f797-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6f797-116">**Element**</span></span>|<span data-ttu-id="6f797-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f797-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f797-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="6f797-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="6f797-119">Representa un elemento de calendario de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6f797-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="6f797-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="6f797-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="6f797-121">Representa una convocatoria de reunión en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="6f797-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f797-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6f797-122">Remarks</span></span>

<span data-ttu-id="6f797-123">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="6f797-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f797-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6f797-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f797-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="6f797-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6f797-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6f797-126">Schema name</span></span>  <br/> |<span data-ttu-id="6f797-127">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="6f797-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="6f797-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6f797-128">Validation file</span></span>  <br/> |<span data-ttu-id="6f797-129">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="6f797-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6f797-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6f797-130">Can be empty</span></span>  <br/> |<span data-ttu-id="6f797-131">Falso</span><span class="sxs-lookup"><span data-stu-id="6f797-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f797-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f797-132">See also</span></span>

- [<span data-ttu-id="6f797-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="6f797-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

