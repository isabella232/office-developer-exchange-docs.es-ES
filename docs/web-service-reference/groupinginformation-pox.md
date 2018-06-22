---
title: GroupingInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d8a007f-d79c-43c8-90e3-2c6d883f3a7c
description: El elemento GroupingInformation contiene un valor que se usa para agrupar el buzón del usuario para mantener la afinidad al suscribirse a las notificaciones a través de varios buzones de correo.
ms.openlocfilehash: bcde002c794ac79d9515befc0755c1f954ee8706
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835781"
---
# <a name="groupinginformation-pox"></a><span data-ttu-id="f0387-103">GroupingInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="f0387-103">GroupingInformation (POX)</span></span>

<span data-ttu-id="f0387-104">El elemento **GroupingInformation** contiene un valor que se usa para el buzón del usuario para [mantener la afinidad](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) de grupo al suscribirse a las notificaciones a través de varios buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="f0387-104">The **GroupingInformation** element contains a value that is used to group the user's mailbox to [maintain affinity](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) when subscribing to notifications across multiple mailboxes.</span></span> 
  
[<span data-ttu-id="f0387-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="f0387-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="f0387-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="f0387-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="f0387-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="f0387-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="f0387-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="f0387-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="f0387-109">GroupingInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="f0387-109">GroupingInformation (POX)</span></span>](groupinginformation-pox.md)
  
```XML
<GroupingInformation/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="f0387-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f0387-110">Attributes and elements</span></span>

<span data-ttu-id="f0387-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f0387-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f0387-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="f0387-112">Attributes</span></span>

<span data-ttu-id="f0387-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f0387-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f0387-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f0387-114">Child elements</span></span>

<span data-ttu-id="f0387-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f0387-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f0387-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f0387-116">Parent elements</span></span>

|<span data-ttu-id="f0387-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="f0387-117">**Element**</span></span>|<span data-ttu-id="f0387-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f0387-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f0387-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="f0387-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="f0387-120">Contiene las especificaciones para conectar a un cliente con el servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f0387-120">Contains the specifications for connecting a client to the Exchange server.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f0387-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f0387-121">Text value</span></span>

<span data-ttu-id="f0387-122">El valor de texto se compara con el valor del elemento **GroupingInformation** para otros buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="f0387-122">The text value is compared to the value of the **GroupingInformation** element for other mailboxes.</span></span> <span data-ttu-id="f0387-123">Los buzones que tienen el mismo valor y usar el mismo extremo de servicios Web de Exchange (EWS) se pueden agrupar para mantener la afinidad.</span><span class="sxs-lookup"><span data-stu-id="f0387-123">Mailboxes that have the same value and use the same Exchange Web Services (EWS) endpoint can be grouped together to maintain affinity.</span></span> <span data-ttu-id="f0387-124">Para obtener más detalles, vea [mantener la afinidad entre un grupo de suscripciones y el servidor de buzones en Exchange](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f0387-124">For more details, see [Maintain affinity between a group of subscriptions and the Mailbox server in Exchange](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f0387-125">Notas</span><span class="sxs-lookup"><span data-stu-id="f0387-125">Remarks</span></span>

<span data-ttu-id="f0387-126">El elemento **GroupingInformation** sólo es aplicable a los elementos de **protocolo** que tienen un elemento secundario de [Tipo (POX)](type-pox.md) con un valor de "EXPR".</span><span class="sxs-lookup"><span data-stu-id="f0387-126">The **GroupingInformation** element is only applicable to **Protocol** elements that have a [Type (POX)](type-pox.md) child element with a value of "EXPR".</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f0387-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="f0387-127">See also</span></span>

- [<span data-ttu-id="f0387-128">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="f0387-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)
- [<span data-ttu-id="f0387-129">Mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de Exchange</span><span class="sxs-lookup"><span data-stu-id="f0387-129">Maintain affinity between a group of subscriptions and the Mailbox server in Exchange</span></span>](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)

