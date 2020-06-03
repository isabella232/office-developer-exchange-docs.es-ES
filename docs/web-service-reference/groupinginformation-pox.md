---
title: GroupingInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d8a007f-d79c-43c8-90e3-2c6d883f3a7c
description: El elemento GroupingInformation contiene un valor que se usa para agrupar el buzón del usuario con el fin de mantener la afinidad al suscribirse a las notificaciones en varios buzones.
ms.openlocfilehash: 7cab5d68f7dd5ec1f6caded5b9da6cfee03f3a67
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530081"
---
# <a name="groupinginformation-pox"></a><span data-ttu-id="1926b-103">GroupingInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="1926b-103">GroupingInformation (POX)</span></span>

<span data-ttu-id="1926b-104">El elemento **GroupingInformation** contiene un valor que se usa para agrupar el buzón del usuario con el fin de [mantener la afinidad](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) al suscribirse a las notificaciones en varios buzones.</span><span class="sxs-lookup"><span data-stu-id="1926b-104">The **GroupingInformation** element contains a value that is used to group the user's mailbox to [maintain affinity](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) when subscribing to notifications across multiple mailboxes.</span></span> 
  
[<span data-ttu-id="1926b-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="1926b-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="1926b-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="1926b-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="1926b-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="1926b-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="1926b-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="1926b-108">Protocol (POX)</span></span>](protocol-pox.md)
  
[<span data-ttu-id="1926b-109">GroupingInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="1926b-109">GroupingInformation (POX)</span></span>](groupinginformation-pox.md)
  
```XML
<GroupingInformation/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="1926b-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1926b-110">Attributes and elements</span></span>

<span data-ttu-id="1926b-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1926b-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1926b-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="1926b-112">Attributes</span></span>

<span data-ttu-id="1926b-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1926b-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1926b-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1926b-114">Child elements</span></span>

<span data-ttu-id="1926b-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1926b-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1926b-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1926b-116">Parent elements</span></span>

|<span data-ttu-id="1926b-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="1926b-117">**Element**</span></span>|<span data-ttu-id="1926b-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1926b-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1926b-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="1926b-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="1926b-120">Contiene las especificaciones para conectar un cliente al servidor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1926b-120">Contains the specifications for connecting a client to the Exchange server.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1926b-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="1926b-121">Text value</span></span>

<span data-ttu-id="1926b-122">El valor de texto se compara con el valor del elemento **GroupingInformation** para otros buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="1926b-122">The text value is compared to the value of the **GroupingInformation** element for other mailboxes.</span></span> <span data-ttu-id="1926b-123">Los buzones que tienen el mismo valor y usan el mismo punto de conexión de servicios web Exchange (EWS) se pueden agrupar para mantener la afinidad.</span><span class="sxs-lookup"><span data-stu-id="1926b-123">Mailboxes that have the same value and use the same Exchange Web Services (EWS) endpoint can be grouped together to maintain affinity.</span></span> <span data-ttu-id="1926b-124">Para obtener más información, vea [mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de Exchange](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1926b-124">For more details, see [Maintain affinity between a group of subscriptions and the Mailbox server in Exchange](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1926b-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1926b-125">Remarks</span></span>

<span data-ttu-id="1926b-126">El elemento **GroupingInformation** solo se aplica a los elementos de **Protocolo** que tienen un elemento secundario [tipo (POX)](type-pox.md) con un valor de "expr".</span><span class="sxs-lookup"><span data-stu-id="1926b-126">The **GroupingInformation** element is only applicable to **Protocol** elements that have a [Type (POX)](type-pox.md) child element with a value of "EXPR".</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1926b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1926b-127">See also</span></span>

- [<span data-ttu-id="1926b-128">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="1926b-128">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)
- [<span data-ttu-id="1926b-129">Mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de correo de Exchange</span><span class="sxs-lookup"><span data-stu-id="1926b-129">Maintain affinity between a group of subscriptions and the Mailbox server in Exchange</span></span>](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)

