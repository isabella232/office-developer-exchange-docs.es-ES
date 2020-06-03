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
description: El elemento UpdateDelegate define una solicitud para actualizar delegados en un buzón. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 17d69eb8c539217d39e1dd0c2616261d02ad304d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468876"
---
# <a name="updatedelegate"></a><span data-ttu-id="c72cc-104">UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="c72cc-104">UpdateDelegate</span></span>

<span data-ttu-id="c72cc-105">El elemento **UpdateDelegate** define una solicitud para actualizar delegados en un buzón.</span><span class="sxs-lookup"><span data-stu-id="c72cc-105">The **UpdateDelegate** element defines a request to update delegates in a mailbox.</span></span> <span data-ttu-id="c72cc-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c72cc-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UpdateDelegate>
      <DelegateUsers/>
   <DeliverMeetingRequests/>
      <Mailbox/>
</UpdateDelegate>
```

 <span data-ttu-id="c72cc-107">**UpdateDelegateType**</span><span class="sxs-lookup"><span data-stu-id="c72cc-107">**UpdateDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c72cc-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c72cc-108">Attributes and elements</span></span>

<span data-ttu-id="c72cc-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c72cc-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c72cc-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="c72cc-110">Attributes</span></span>

<span data-ttu-id="c72cc-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c72cc-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c72cc-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c72cc-112">Child elements</span></span>

|<span data-ttu-id="c72cc-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c72cc-113">**Element**</span></span>|<span data-ttu-id="c72cc-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c72cc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c72cc-115">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="c72cc-115">DelegateUsers</span></span>](delegateusers.md) <br/> |<span data-ttu-id="c72cc-116">Contiene una matriz de elementos [DelegateUser](delegateuser.md) que identifican los delegados y las actualizaciones que se van a aplicar a los delegados.</span><span class="sxs-lookup"><span data-stu-id="c72cc-116">Contains an array of [DelegateUser](delegateuser.md) elements that identify the delegates and the updates to apply to the delegates.</span></span> <span data-ttu-id="c72cc-117">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="c72cc-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="c72cc-118">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="c72cc-118">DeliverMeetingRequests</span></span>](delivermeetingrequests.md) <br/> |<span data-ttu-id="c72cc-119">Define cómo se administran las convocatorias de reunión entre el delegado y la entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="c72cc-119">Defines how meeting requests are handled between the delegate and the principal.</span></span> <span data-ttu-id="c72cc-120">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="c72cc-120">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="c72cc-121">Buzón</span><span class="sxs-lookup"><span data-stu-id="c72cc-121">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="c72cc-122">Identifica un objeto de servicio de directorio de Active Directory habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="c72cc-122">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c72cc-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c72cc-123">Parent elements</span></span>

<span data-ttu-id="c72cc-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c72cc-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c72cc-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c72cc-125">Remarks</span></span>

<span data-ttu-id="c72cc-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="c72cc-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c72cc-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c72cc-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c72cc-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="c72cc-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c72cc-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c72cc-129">Schema Name</span></span>  <br/> |<span data-ttu-id="c72cc-130">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c72cc-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c72cc-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c72cc-131">Validation File</span></span>  <br/> |<span data-ttu-id="c72cc-132">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c72cc-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c72cc-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c72cc-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="c72cc-134">Falso</span><span class="sxs-lookup"><span data-stu-id="c72cc-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c72cc-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c72cc-135">See also</span></span>



[<span data-ttu-id="c72cc-136">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="c72cc-136">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="c72cc-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c72cc-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

