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
ms.openlocfilehash: a08b83ad6e114c194073716c82228ea20ae1d3b7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466503"
---
# <a name="adddelegate"></a><span data-ttu-id="4c602-104">AddDelegate</span><span class="sxs-lookup"><span data-stu-id="4c602-104">AddDelegate</span></span>

<span data-ttu-id="4c602-105">El elemento **AddDelegate** define una solicitud para agregar delegados a un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="4c602-105">The **AddDelegate** element defines a request to add delegates to a mailbox.</span></span> <span data-ttu-id="4c602-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4c602-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<AddDelegate>
   <DelegateUsers/>
   <DeliverMeetingRequests/>
   <Mailbox/>
</AddDelegate>
```

 <span data-ttu-id="4c602-107">**AddDelegateType**</span><span class="sxs-lookup"><span data-stu-id="4c602-107">**AddDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4c602-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4c602-108">Attributes and elements</span></span>

<span data-ttu-id="4c602-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4c602-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c602-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="4c602-110">Attributes</span></span>

<span data-ttu-id="4c602-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4c602-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4c602-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4c602-112">Child elements</span></span>

|<span data-ttu-id="4c602-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4c602-113">**Element**</span></span>|<span data-ttu-id="4c602-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4c602-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4c602-115">DelegateUsers</span><span class="sxs-lookup"><span data-stu-id="4c602-115">DelegateUsers</span></span>](delegateusers.md) <br/> |<span data-ttu-id="4c602-116">Contiene las identidades de los delegados que se van a agregar a o actualizar en un buzón.</span><span class="sxs-lookup"><span data-stu-id="4c602-116">Contains the identities of delegates to add to or update in a mailbox.</span></span> <span data-ttu-id="4c602-117">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4c602-117">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="4c602-118">DeliverMeetingRequests</span><span class="sxs-lookup"><span data-stu-id="4c602-118">DeliverMeetingRequests</span></span>](delivermeetingrequests.md) <br/> |<span data-ttu-id="4c602-119">Define cómo se administran las convocatorias de reunión entre el delegado y la entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="4c602-119">Defines how meeting requests are handled between the delegate and the principal.</span></span> <span data-ttu-id="4c602-120">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4c602-120">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="4c602-121">Buzón</span><span class="sxs-lookup"><span data-stu-id="4c602-121">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="4c602-122">Identifica un objeto de servicio de directorio de Active Directory habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="4c602-122">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4c602-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4c602-123">Parent elements</span></span>

<span data-ttu-id="4c602-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4c602-124">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c602-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4c602-125">Remarks</span></span>

<span data-ttu-id="4c602-126">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="4c602-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4c602-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4c602-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c602-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="4c602-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4c602-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4c602-129">Schema Name</span></span>  <br/> |<span data-ttu-id="4c602-130">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="4c602-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4c602-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4c602-131">Validation File</span></span>  <br/> |<span data-ttu-id="4c602-132">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4c602-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4c602-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4c602-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="4c602-134">Falso</span><span class="sxs-lookup"><span data-stu-id="4c602-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4c602-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c602-135">See also</span></span>

- [<span data-ttu-id="4c602-136">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="4c602-136">AddDelegate operation</span></span>](adddelegate-operation.md)
- [<span data-ttu-id="4c602-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4c602-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="4c602-138">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="4c602-138">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

