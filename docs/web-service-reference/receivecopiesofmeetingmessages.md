---
title: ReceiveCopiesOfMeetingMessages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReceiveCopiesOfMeetingMessages
api_type:
- schema
ms.assetid: 65217ca8-6aea-47eb-a989-e6cce25f5f09
description: El elemento ReceiveCopiesOfMeetingMessages indica si un delegado reciba copias de los mensajes de reunión que se dirigen a la entidad de seguridad. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: e39a5d3255268b418fa956959da5ae0ea062d831
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836967"
---
# <a name="receivecopiesofmeetingmessages"></a><span data-ttu-id="f78aa-104">ReceiveCopiesOfMeetingMessages</span><span class="sxs-lookup"><span data-stu-id="f78aa-104">ReceiveCopiesOfMeetingMessages</span></span>

<span data-ttu-id="f78aa-105">El elemento **ReceiveCopiesOfMeetingMessages** indica si un delegado reciba copias de los mensajes de reunión que se dirigen a la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f78aa-105">The **ReceiveCopiesOfMeetingMessages** element indicates whether a delegate receives copies of meeting-related messages that are addressed to the principal.</span></span> <span data-ttu-id="f78aa-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f78aa-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ReceiveCopiesOfMeetingMessages>true or false</ReceiveCopiesOfMeetingMessages>
```

 <span data-ttu-id="f78aa-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f78aa-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f78aa-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f78aa-108">Attributes and elements</span></span>

<span data-ttu-id="f78aa-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f78aa-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f78aa-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="f78aa-110">Attributes</span></span>

<span data-ttu-id="f78aa-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f78aa-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f78aa-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f78aa-112">Child elements</span></span>

<span data-ttu-id="f78aa-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f78aa-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f78aa-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f78aa-114">Parent elements</span></span>

|<span data-ttu-id="f78aa-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="f78aa-115">**Element**</span></span>|<span data-ttu-id="f78aa-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f78aa-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f78aa-117">UsuarioDelegado</span><span class="sxs-lookup"><span data-stu-id="f78aa-117">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="f78aa-118">Identifica un único delegado para agregar o actualizar en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f78aa-118">Identifies a single delegate to add or update in a mailbox.</span></span> <span data-ttu-id="f78aa-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="f78aa-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f78aa-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f78aa-120">Text value</span></span>

<span data-ttu-id="f78aa-121">Un valor de texto de **true** indica que un delegado reciba una copia de los mensajes de la reunión.</span><span class="sxs-lookup"><span data-stu-id="f78aa-121">A text value of **true** indicates that a delegate receives a copy of meeting messages.</span></span> <span data-ttu-id="f78aa-122">Un valor de texto de **false** indica que un delegado no reciben una copia de los mensajes de la reunión.</span><span class="sxs-lookup"><span data-stu-id="f78aa-122">A text value of **false** indicates that a delegate does not receive a copy of meeting messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f78aa-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f78aa-123">Remarks</span></span>

<span data-ttu-id="f78aa-124">Cuando **ReceiveCopiesOfMeetingMessages** se establece en **false**, el delegado todavía puede enviar el mensaje en nombre de la entidad de seguridad, pero no recibirá todos los mensajes relacionados con la reunión.</span><span class="sxs-lookup"><span data-stu-id="f78aa-124">When **ReceiveCopiesOfMeetingMessages** is set to **false**, the delegate can still send message on behalf of the principal, but will not receive any meeting-related messages.</span></span>
  
<span data-ttu-id="f78aa-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="f78aa-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f78aa-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f78aa-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f78aa-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f78aa-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f78aa-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f78aa-128">Schema Name</span></span>  <br/> |<span data-ttu-id="f78aa-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="f78aa-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="f78aa-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f78aa-130">Validation File</span></span>  <br/> |<span data-ttu-id="f78aa-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f78aa-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f78aa-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f78aa-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="f78aa-133">False</span><span class="sxs-lookup"><span data-stu-id="f78aa-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f78aa-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f78aa-134">See also</span></span>



[<span data-ttu-id="f78aa-135">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="f78aa-135">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="f78aa-136">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="f78aa-136">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="f78aa-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f78aa-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="f78aa-138">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="f78aa-138">Adding Delegates</span></span>](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

