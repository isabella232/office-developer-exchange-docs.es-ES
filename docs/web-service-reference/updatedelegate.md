---
title: UpdateDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateDelegate
api_type:
- schema
ms.assetid: c6ae99c4-18b0-4136-90ab-12cf15e15f91
description: El elemento UpdateDelegate define una solicitud para actualizar los delegados en un buzón de correo. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 32322e48acfa5f1058786162565a185a3e565d6e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840806"
---
# <a name="updatedelegate"></a><span data-ttu-id="7bfb2-104">UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="7bfb2-104">UpdateDelegate</span></span>

<span data-ttu-id="7bfb2-105">El elemento **UpdateDelegate** define una solicitud para actualizar los delegados en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="7bfb2-105">The **UpdateDelegate** element defines a request to update delegates in a mailbox.</span></span> <span data-ttu-id="7bfb2-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="7bfb2-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UpdateDelegate>
      <DelegateUsers/>
   <DeliverMeetingRequests/>
      <Mailbox/>
</UpdateDelegate>
```

 <span data-ttu-id="7bfb2-107">**UpdateDelegateType**</span><span class="sxs-lookup"><span data-stu-id="7bfb2-107">**UpdateDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7bfb2-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7bfb2-108">Attributes and elements</span></span>

<span data-ttu-id="7bfb2-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7bfb2-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7bfb2-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="7bfb2-110">Attributes</span></span>

<span data-ttu-id="7bfb2-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7bfb2-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7bfb2-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7bfb2-112">Child elements</span></span>

|<span data-ttu-id="7bfb2-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="7bfb2-113">**Element**</span></span>|<span data-ttu-id="7bfb2-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7bfb2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7bfb2-115">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="7bfb2-115">DelegateUsers</span></span>](delegateusers.md) <br/> |<span data-ttu-id="7bfb2-116">Contiene una matriz de elementos de [UsuarioDelegado](delegateuser.md) que identifican los delegados y las actualizaciones se pueden aplicar a los delegados.</span><span class="sxs-lookup"><span data-stu-id="7bfb2-116">Contains an array of [DelegateUser](delegateuser.md) elements that identify the delegates and the updates to apply to the delegates.</span></span> <span data-ttu-id="7bfb2-117">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="7bfb2-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="7bfb2-118">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="7bfb2-118">DeliverMeetingRequests</span></span>](delivermeetingrequests.md) <br/> |<span data-ttu-id="7bfb2-119">Define cómo se controlan las convocatorias de reunión entre el delegado y la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7bfb2-119">Defines how meeting requests are handled between the delegate and the principal.</span></span> <span data-ttu-id="7bfb2-120">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="7bfb2-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="7bfb2-121">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="7bfb2-121">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="7bfb2-122">Identifica un objeto de servicio de directorio de Active Directory habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="7bfb2-122">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7bfb2-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7bfb2-123">Parent elements</span></span>

<span data-ttu-id="7bfb2-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7bfb2-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7bfb2-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7bfb2-125">Remarks</span></span>

<span data-ttu-id="7bfb2-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="7bfb2-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7bfb2-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7bfb2-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7bfb2-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7bfb2-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7bfb2-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7bfb2-129">Schema Name</span></span>  <br/> |<span data-ttu-id="7bfb2-130">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="7bfb2-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7bfb2-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7bfb2-131">Validation File</span></span>  <br/> |<span data-ttu-id="7bfb2-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7bfb2-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7bfb2-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7bfb2-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="7bfb2-134">False</span><span class="sxs-lookup"><span data-stu-id="7bfb2-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7bfb2-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="7bfb2-135">See also</span></span>



[<span data-ttu-id="7bfb2-136">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="7bfb2-136">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="7bfb2-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="7bfb2-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

