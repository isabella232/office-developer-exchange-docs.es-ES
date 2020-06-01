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
description: El elemento ReceiveCopiesOfMeetingMessages indica si un delegado recibe copias de mensajes relacionados con la reunión que se dirigen a la entidad de la identidad. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: af6e220304f88c4db00ab675077dcd9bf581ea9e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468267"
---
# <a name="receivecopiesofmeetingmessages"></a><span data-ttu-id="10290-104">ReceiveCopiesOfMeetingMessages</span><span class="sxs-lookup"><span data-stu-id="10290-104">ReceiveCopiesOfMeetingMessages</span></span>

<span data-ttu-id="10290-105">El elemento **ReceiveCopiesOfMeetingMessages** indica si un delegado recibe copias de mensajes relacionados con la reunión que se dirigen a la entidad de la identidad.</span><span class="sxs-lookup"><span data-stu-id="10290-105">The **ReceiveCopiesOfMeetingMessages** element indicates whether a delegate receives copies of meeting-related messages that are addressed to the principal.</span></span> <span data-ttu-id="10290-106">Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="10290-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ReceiveCopiesOfMeetingMessages>true or false</ReceiveCopiesOfMeetingMessages>
```

 <span data-ttu-id="10290-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="10290-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="10290-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="10290-108">Attributes and elements</span></span>

<span data-ttu-id="10290-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="10290-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="10290-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="10290-110">Attributes</span></span>

<span data-ttu-id="10290-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="10290-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="10290-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="10290-112">Child elements</span></span>

<span data-ttu-id="10290-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="10290-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="10290-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="10290-114">Parent elements</span></span>

|<span data-ttu-id="10290-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="10290-115">**Element**</span></span>|<span data-ttu-id="10290-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="10290-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="10290-117">DelegateUser</span><span class="sxs-lookup"><span data-stu-id="10290-117">DelegateUser</span></span>](delegateuser.md) <br/> |<span data-ttu-id="10290-118">Identifica un único delegado para agregar o actualizar en un buzón.</span><span class="sxs-lookup"><span data-stu-id="10290-118">Identifies a single delegate to add or update in a mailbox.</span></span> <span data-ttu-id="10290-119">Este elemento se introdujo en Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="10290-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="10290-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="10290-120">Text value</span></span>

<span data-ttu-id="10290-121">Un valor de texto de **true** indica que un delegado recibe una copia de los mensajes de reunión.</span><span class="sxs-lookup"><span data-stu-id="10290-121">A text value of **true** indicates that a delegate receives a copy of meeting messages.</span></span> <span data-ttu-id="10290-122">Un valor de texto **falso** indica que un delegado no recibe una copia de los mensajes de reunión.</span><span class="sxs-lookup"><span data-stu-id="10290-122">A text value of **false** indicates that a delegate does not receive a copy of meeting messages.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="10290-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="10290-123">Remarks</span></span>

<span data-ttu-id="10290-124">Cuando **ReceiveCopiesOfMeetingMessages** se establece en **false**, el delegado puede seguir enviando mensajes en nombre de la entidad de identidad, pero no recibirá ningún mensaje relacionado con la reunión.</span><span class="sxs-lookup"><span data-stu-id="10290-124">When **ReceiveCopiesOfMeetingMessages** is set to **false**, the delegate can still send message on behalf of the principal, but will not receive any meeting-related messages.</span></span>
  
<span data-ttu-id="10290-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="10290-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="10290-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="10290-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10290-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="10290-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="10290-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="10290-128">Schema Name</span></span>  <br/> |<span data-ttu-id="10290-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="10290-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="10290-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="10290-130">Validation File</span></span>  <br/> |<span data-ttu-id="10290-131">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="10290-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="10290-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="10290-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="10290-133">Falso</span><span class="sxs-lookup"><span data-stu-id="10290-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="10290-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="10290-134">See also</span></span>



[<span data-ttu-id="10290-135">Operación AddDelegate</span><span class="sxs-lookup"><span data-stu-id="10290-135">AddDelegate operation</span></span>](adddelegate-operation.md)
  
[<span data-ttu-id="10290-136">Operación UpdateDelegate</span><span class="sxs-lookup"><span data-stu-id="10290-136">UpdateDelegate operation</span></span>](updatedelegate-operation.md)


- [<span data-ttu-id="10290-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="10290-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="10290-138">Adición de delegados</span><span class="sxs-lookup"><span data-stu-id="10290-138">Adding Delegates</span></span>](https://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

