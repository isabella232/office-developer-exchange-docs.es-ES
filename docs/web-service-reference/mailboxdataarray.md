---
title: MailboxDataArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxDataArray
api_type:
- schema
ms.assetid: a14af788-beee-452c-b5d0-37bcb4ef02ff
description: El elemento MailboxDataArray contiene una lista de buzones de correo para consultar la información de disponibilidad.
ms.openlocfilehash: b76e71ee9127dc2221e0065a27d3c781f8b5786a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836283"
---
# <a name="mailboxdataarray"></a><span data-ttu-id="e09d9-103">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="e09d9-103">MailboxDataArray</span></span>

<span data-ttu-id="e09d9-104">El elemento **MailboxDataArray** contiene una lista de buzones de correo para consultar la información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="e09d9-104">The **MailboxDataArray** element contains a list of mailboxes to query for availability information.</span></span> 
  
- [<span data-ttu-id="e09d9-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="e09d9-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
- [<span data-ttu-id="e09d9-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="e09d9-106">MailboxDataArray</span></span>](mailboxdataarray.md)
  
- [<span data-ttu-id="e09d9-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="e09d9-107">MailboxData</span></span>](mailboxdata.md)
  
```xml
<MailboxDataArray>
   <MailboxData>...</MailboxData>
</MailboxDataArray>
```

<span data-ttu-id="e09d9-108">**ArrayOfMailboxData**</span><span class="sxs-lookup"><span data-stu-id="e09d9-108">**ArrayOfMailboxData**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e09d9-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e09d9-109">Attributes and elements</span></span>

<span data-ttu-id="e09d9-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e09d9-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e09d9-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="e09d9-111">Attributes</span></span>

<span data-ttu-id="e09d9-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e09d9-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e09d9-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e09d9-113">Child elements</span></span>

|<span data-ttu-id="e09d9-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="e09d9-114">**Element**</span></span>|<span data-ttu-id="e09d9-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e09d9-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e09d9-116">MailboxData</span><span class="sxs-lookup"><span data-stu-id="e09d9-116">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="e09d9-117">Representa un usuario de buzón de correo individual y opciones para el tipo de datos que se devolverá sobre el usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="e09d9-117">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e09d9-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e09d9-118">Parent elements</span></span>

|<span data-ttu-id="e09d9-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="e09d9-119">**Element**</span></span>|<span data-ttu-id="e09d9-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e09d9-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e09d9-121">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="e09d9-121">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="e09d9-122">Contiene los argumentos utilizados para obtener información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="e09d9-122">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="e09d9-123">Esto es un elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="e09d9-123">This is a root element.</span></span>  <br/> <span data-ttu-id="e09d9-124">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="e09d9-124">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e09d9-125">Notas</span><span class="sxs-lookup"><span data-stu-id="e09d9-125">Remarks</span></span>

<span data-ttu-id="e09d9-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft® Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="e09d9-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e09d9-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e09d9-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e09d9-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e09d9-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e09d9-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e09d9-129">Schema Name</span></span>  <br/> |<span data-ttu-id="e09d9-130">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="e09d9-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e09d9-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e09d9-131">Validation File</span></span>  <br/> |<span data-ttu-id="e09d9-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e09d9-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e09d9-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e09d9-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="e09d9-134">False</span><span class="sxs-lookup"><span data-stu-id="e09d9-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e09d9-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="e09d9-135">See also</span></span>

- [<span data-ttu-id="e09d9-136">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="e09d9-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="e09d9-137">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="e09d9-137">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="e09d9-138">Obtención de disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="e09d9-138">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

