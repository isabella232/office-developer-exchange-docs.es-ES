---
title: AddDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AddDelegate
api_type:
- schema
ms.assetid: 646fb994-229e-4d90-8b95-6541191cb3ae
description: El elemento AddDelegate define una solicitud para agregar delegados a un buzón de correo. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: d1cb0ff3ea68904bf88e346f68afe7c349ae4394
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763400"
---
# <a name="adddelegate"></a><span data-ttu-id="eb304-104">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="eb304-104">AddDelegate</span></span>

<span data-ttu-id="eb304-105">El elemento **AddDelegate** define una solicitud para agregar delegados a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="eb304-105">The **AddDelegate** element defines a request to add delegates to a mailbox.</span></span> <span data-ttu-id="eb304-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="eb304-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<AddDelegate>
   <DelegateUsers/>
   <DeliverMeetingRequests/>
   <Mailbox/>
</AddDelegate>
```

 <span data-ttu-id="eb304-107">**AddDelegateType**</span><span class="sxs-lookup"><span data-stu-id="eb304-107">**AddDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb304-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="eb304-108">Attributes and elements</span></span>

<span data-ttu-id="eb304-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="eb304-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb304-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="eb304-110">Attributes</span></span>

<span data-ttu-id="eb304-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eb304-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eb304-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eb304-112">Child elements</span></span>

|<span data-ttu-id="eb304-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="eb304-113">**Element**</span></span>|<span data-ttu-id="eb304-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eb304-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb304-115">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="eb304-115">DelegateUsers</span></span>](delegateusers.md) <br/> |<span data-ttu-id="eb304-116">Contiene las identidades de delegados para agregar o actualizar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="eb304-116">Contains the identities of delegates to add to or update in a mailbox.</span></span> <span data-ttu-id="eb304-117">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="eb304-117">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="eb304-118">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="eb304-118">DeliverMeetingRequests</span></span>](delivermeetingrequests.md) <br/> |<span data-ttu-id="eb304-119">Define cómo se controlan las convocatorias de reunión entre el delegado y la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="eb304-119">Defines how meeting requests are handled between the delegate and the principal.</span></span> <span data-ttu-id="eb304-120">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="eb304-120">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="eb304-121">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="eb304-121">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="eb304-122">Identifica un objeto de servicio de directorio de Active Directory habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="eb304-122">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="eb304-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="eb304-123">Parent elements</span></span>

<span data-ttu-id="eb304-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eb304-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb304-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eb304-125">Remarks</span></span>

<span data-ttu-id="eb304-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="eb304-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb304-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="eb304-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb304-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eb304-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="eb304-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="eb304-129">Schema Name</span></span>  <br/> |<span data-ttu-id="eb304-130">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="eb304-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="eb304-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="eb304-131">Validation File</span></span>  <br/> |<span data-ttu-id="eb304-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="eb304-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eb304-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="eb304-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="eb304-134">False</span><span class="sxs-lookup"><span data-stu-id="eb304-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb304-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb304-135">See also</span></span>

- [<span data-ttu-id="eb304-136">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="eb304-136">AddDelegate operation</span></span>](adddelegate-operation.md)
- [<span data-ttu-id="eb304-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="eb304-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="eb304-138">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="eb304-138">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)
