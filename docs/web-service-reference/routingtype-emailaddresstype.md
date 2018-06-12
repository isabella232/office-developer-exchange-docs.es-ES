---
title: RoutingType (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RoutingType
api_type:
- schema
ms.assetid: 683216be-9972-4f48-a148-c34bfe7f53e5
description: El elemento RoutingType define el tipo de dirección para el buzón de correo.
ms.openlocfilehash: a02c3b5711a657311428d67cccabd9c8c231db67
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837256"
---
# <a name="routingtype-emailaddresstype"></a><span data-ttu-id="30bfa-103">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="30bfa-103">RoutingType (EmailAddressType)</span></span>

<span data-ttu-id="30bfa-104">El elemento **RoutingType** define el tipo de dirección para el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="30bfa-104">The **RoutingType** element defines the address type for the mailbox.</span></span> 
  
```XML
<RoutingType/>
```

 <span data-ttu-id="30bfa-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="30bfa-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="30bfa-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="30bfa-106">Attributes and elements</span></span>

<span data-ttu-id="30bfa-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="30bfa-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="30bfa-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="30bfa-108">Attributes</span></span>

<span data-ttu-id="30bfa-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="30bfa-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="30bfa-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="30bfa-110">Child elements</span></span>

<span data-ttu-id="30bfa-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="30bfa-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="30bfa-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="30bfa-112">Parent elements</span></span>

|<span data-ttu-id="30bfa-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="30bfa-113">**Element**</span></span>|<span data-ttu-id="30bfa-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="30bfa-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30bfa-115">ActingAs</span><span class="sxs-lookup"><span data-stu-id="30bfa-115">ActingAs</span></span>](actingas.md) <br/> |<span data-ttu-id="30bfa-116">Identifique quién envía como el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="30bfa-116">Identifies who the caller is sending as.</span></span>  <br/> |
|[<span data-ttu-id="30bfa-117">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="30bfa-117">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="30bfa-118">Identifica una dirección de correo electrónico completa resuelta.</span><span class="sxs-lookup"><span data-stu-id="30bfa-118">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="30bfa-119">RoomList</span><span class="sxs-lookup"><span data-stu-id="30bfa-119">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="30bfa-120">Identifica una lista de las salas de reuniones.</span><span class="sxs-lookup"><span data-stu-id="30bfa-120">Identifies a list of meeting rooms.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="30bfa-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="30bfa-121">Text value</span></span>

<span data-ttu-id="30bfa-122">El valor de texto representa un tipo de distribución.</span><span class="sxs-lookup"><span data-stu-id="30bfa-122">The text value represents a routing type.</span></span> <span data-ttu-id="30bfa-123">SMTP es el valor de texto típico para este elemento.</span><span class="sxs-lookup"><span data-stu-id="30bfa-123">SMTP is the typical text value for this element.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="30bfa-124">Notas</span><span class="sxs-lookup"><span data-stu-id="30bfa-124">Remarks</span></span>

<span data-ttu-id="30bfa-125">Este elemento es opcional en el elemento de [buzón de correo](mailbox.md) .</span><span class="sxs-lookup"><span data-stu-id="30bfa-125">This element is optional in the [Mailbox](mailbox.md) element.</span></span> <span data-ttu-id="30bfa-126">Otro elemento de [RoutingType (EmailAddress)](routingtype-emailaddress.md) se usa para operaciones de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="30bfa-126">Another [RoutingType (EmailAddress)](routingtype-emailaddress.md) element is used for Availability operations.</span></span> 
  
<span data-ttu-id="30bfa-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="30bfa-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="30bfa-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="30bfa-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30bfa-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="30bfa-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="30bfa-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="30bfa-130">Schema Name</span></span>  <br/> |<span data-ttu-id="30bfa-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="30bfa-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="30bfa-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="30bfa-132">Validation File</span></span>  <br/> |<span data-ttu-id="30bfa-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="30bfa-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="30bfa-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="30bfa-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="30bfa-135">False</span><span class="sxs-lookup"><span data-stu-id="30bfa-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30bfa-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="30bfa-136">See also</span></span>



- [<span data-ttu-id="30bfa-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="30bfa-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

