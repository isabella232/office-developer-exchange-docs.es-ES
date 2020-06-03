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
description: El elemento RoutingType define el tipo de dirección para el buzón.
ms.openlocfilehash: d4229f2857a5c99cc9bb7ff9b9b103de099a0055
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465089"
---
# <a name="routingtype-emailaddresstype"></a><span data-ttu-id="912bc-103">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="912bc-103">RoutingType (EmailAddressType)</span></span>

<span data-ttu-id="912bc-104">El elemento **RoutingType** define el tipo de dirección para el buzón.</span><span class="sxs-lookup"><span data-stu-id="912bc-104">The **RoutingType** element defines the address type for the mailbox.</span></span> 
  
```XML
<RoutingType/>
```

 <span data-ttu-id="912bc-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="912bc-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="912bc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="912bc-106">Attributes and elements</span></span>

<span data-ttu-id="912bc-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="912bc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="912bc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="912bc-108">Attributes</span></span>

<span data-ttu-id="912bc-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="912bc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="912bc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="912bc-110">Child elements</span></span>

<span data-ttu-id="912bc-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="912bc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="912bc-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="912bc-112">Parent elements</span></span>

|<span data-ttu-id="912bc-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="912bc-113">**Element**</span></span>|<span data-ttu-id="912bc-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="912bc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="912bc-115">Acciones</span><span class="sxs-lookup"><span data-stu-id="912bc-115">ActingAs</span></span>](actingas.md) <br/> |<span data-ttu-id="912bc-116">Identifica quién envía el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="912bc-116">Identifies who the caller is sending as.</span></span>  <br/> |
|[<span data-ttu-id="912bc-117">Buzón</span><span class="sxs-lookup"><span data-stu-id="912bc-117">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="912bc-118">Identifica una dirección de correo electrónico completamente resuelta.</span><span class="sxs-lookup"><span data-stu-id="912bc-118">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="912bc-119">RoomList</span><span class="sxs-lookup"><span data-stu-id="912bc-119">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="912bc-120">Identifica una lista de salas de reuniones.</span><span class="sxs-lookup"><span data-stu-id="912bc-120">Identifies a list of meeting rooms.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="912bc-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="912bc-121">Text value</span></span>

<span data-ttu-id="912bc-122">El valor de texto representa un tipo de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="912bc-122">The text value represents a routing type.</span></span> <span data-ttu-id="912bc-123">SMTP es el valor de texto típico de este elemento.</span><span class="sxs-lookup"><span data-stu-id="912bc-123">SMTP is the typical text value for this element.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="912bc-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="912bc-124">Remarks</span></span>

<span data-ttu-id="912bc-125">Este elemento es opcional en el elemento [Mailbox](mailbox.md) .</span><span class="sxs-lookup"><span data-stu-id="912bc-125">This element is optional in the [Mailbox](mailbox.md) element.</span></span> <span data-ttu-id="912bc-126">Se usa otro elemento [RoutingType (EmailAddress)](routingtype-emailaddress.md) para las operaciones de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="912bc-126">Another [RoutingType (EmailAddress)](routingtype-emailaddress.md) element is used for Availability operations.</span></span> 
  
<span data-ttu-id="912bc-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="912bc-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="912bc-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="912bc-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="912bc-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="912bc-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="912bc-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="912bc-130">Schema Name</span></span>  <br/> |<span data-ttu-id="912bc-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="912bc-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="912bc-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="912bc-132">Validation File</span></span>  <br/> |<span data-ttu-id="912bc-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="912bc-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="912bc-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="912bc-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="912bc-135">Falso</span><span class="sxs-lookup"><span data-stu-id="912bc-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="912bc-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="912bc-136">See also</span></span>



- [<span data-ttu-id="912bc-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="912bc-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

