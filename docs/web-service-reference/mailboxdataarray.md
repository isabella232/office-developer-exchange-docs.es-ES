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
description: El elemento MailboxDataArray contiene una lista de buzones para consultar la información de disponibilidad.
ms.openlocfilehash: 894bf97a0d633d7eef0434331ccf1580fcba386e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468197"
---
# <a name="mailboxdataarray"></a><span data-ttu-id="bb8e3-103">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="bb8e3-103">MailboxDataArray</span></span>

<span data-ttu-id="bb8e3-104">El elemento **MailboxDataArray** contiene una lista de buzones para consultar la información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="bb8e3-104">The **MailboxDataArray** element contains a list of mailboxes to query for availability information.</span></span> 
  
- [<span data-ttu-id="bb8e3-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="bb8e3-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
- [<span data-ttu-id="bb8e3-106">MailboxDataArray</span><span class="sxs-lookup"><span data-stu-id="bb8e3-106">MailboxDataArray</span></span>](mailboxdataarray.md)
  
- [<span data-ttu-id="bb8e3-107">MailboxData</span><span class="sxs-lookup"><span data-stu-id="bb8e3-107">MailboxData</span></span>](mailboxdata.md)
  
```xml
<MailboxDataArray>
   <MailboxData>...</MailboxData>
</MailboxDataArray>
```

<span data-ttu-id="bb8e3-108">**ArrayOfMailboxData**</span><span class="sxs-lookup"><span data-stu-id="bb8e3-108">**ArrayOfMailboxData**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="bb8e3-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bb8e3-109">Attributes and elements</span></span>

<span data-ttu-id="bb8e3-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bb8e3-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb8e3-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="bb8e3-111">Attributes</span></span>

<span data-ttu-id="bb8e3-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="bb8e3-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bb8e3-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bb8e3-113">Child elements</span></span>

|<span data-ttu-id="bb8e3-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bb8e3-114">**Element**</span></span>|<span data-ttu-id="bb8e3-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb8e3-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb8e3-116">MailboxData</span><span class="sxs-lookup"><span data-stu-id="bb8e3-116">MailboxData</span></span>](mailboxdata.md) <br/> |<span data-ttu-id="bb8e3-117">Representa un usuario de buzón individual y opciones para el tipo de datos que se devolverán sobre el usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="bb8e3-117">Represents an individual mailbox user and options for the type of data to be returned about the mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bb8e3-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bb8e3-118">Parent elements</span></span>

|<span data-ttu-id="bb8e3-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bb8e3-119">**Element**</span></span>|<span data-ttu-id="bb8e3-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb8e3-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb8e3-121">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="bb8e3-121">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="bb8e3-122">Contiene los argumentos usados para obtener información de disponibilidad del usuario.</span><span class="sxs-lookup"><span data-stu-id="bb8e3-122">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="bb8e3-123">Se trata de un elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="bb8e3-123">This is a root element.</span></span>  <br/> <span data-ttu-id="bb8e3-124">A continuación se encuentra la expresión XPath de este elemento:</span><span class="sxs-lookup"><span data-stu-id="bb8e3-124">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb8e3-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb8e3-125">Remarks</span></span>

<span data-ttu-id="bb8e3-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft® Exchange Server 2007 que tenga instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="bb8e3-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft® Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bb8e3-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bb8e3-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb8e3-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="bb8e3-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bb8e3-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bb8e3-129">Schema Name</span></span>  <br/> |<span data-ttu-id="bb8e3-130">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="bb8e3-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bb8e3-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bb8e3-131">Validation File</span></span>  <br/> |<span data-ttu-id="bb8e3-132">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="bb8e3-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bb8e3-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bb8e3-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="bb8e3-134">Falso</span><span class="sxs-lookup"><span data-stu-id="bb8e3-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb8e3-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb8e3-135">See also</span></span>

- [<span data-ttu-id="bb8e3-136">Operación GetUserAvailability</span><span class="sxs-lookup"><span data-stu-id="bb8e3-136">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="bb8e3-137">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="bb8e3-137">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
- [<span data-ttu-id="bb8e3-138">Obtener disponibilidad del usuario</span><span class="sxs-lookup"><span data-stu-id="bb8e3-138">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

