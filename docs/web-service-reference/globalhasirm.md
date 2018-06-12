---
title: GlobalHasIrm
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 425272b2-7a4e-4376-aea9-d9b10c1ad6ee
description: El elemento GlobalHasIrm especifica si al menos un mensaje en la conversación y en todas las carpetas es un mensaje protegido de IRM.
ms.openlocfilehash: ad3eafcb38829e7ea57cbc7535b0f5411ad595d2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835717"
---
# <a name="globalhasirm"></a><span data-ttu-id="0fc7e-103">GlobalHasIrm</span><span class="sxs-lookup"><span data-stu-id="0fc7e-103">GlobalHasIrm</span></span>

<span data-ttu-id="0fc7e-104">El elemento **GlobalHasIrm** especifica si al menos un mensaje en la conversación y en todas las carpetas es un mensaje protegido de IRM.</span><span class="sxs-lookup"><span data-stu-id="0fc7e-104">The **GlobalHasIrm** element specifies whether at least one message in the conversation and across all folders is an IRM protected message.</span></span> 
  
```XML
<GlobalHasIrm> true | false </GlobalHasIrm>
```

 <span data-ttu-id="0fc7e-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0fc7e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0fc7e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0fc7e-106">Attributes and elements</span></span>

<span data-ttu-id="0fc7e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0fc7e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0fc7e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0fc7e-108">Attributes</span></span>

<span data-ttu-id="0fc7e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0fc7e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0fc7e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0fc7e-110">Child elements</span></span>

<span data-ttu-id="0fc7e-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0fc7e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0fc7e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0fc7e-112">Parent elements</span></span>

[<span data-ttu-id="0fc7e-113">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="0fc7e-113">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
## <a name="text-value"></a><span data-ttu-id="0fc7e-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0fc7e-114">Text value</span></span>

<span data-ttu-id="0fc7e-115">El valor de texto del elemento **GlobalHasIrm** es **true** si al menos un mensaje en la conversación y en todas las carpetas es un mensaje protegido de IRM.</span><span class="sxs-lookup"><span data-stu-id="0fc7e-115">The text value of the **GlobalHasIrm** element is **true** if at least one message in the conversation and across all folders is an IRM protected message.</span></span> <span data-ttu-id="0fc7e-116">En caso contrario, el valor es **false**.</span><span class="sxs-lookup"><span data-stu-id="0fc7e-116">Otherwise the value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0fc7e-117">Notas</span><span class="sxs-lookup"><span data-stu-id="0fc7e-117">Remarks</span></span>

<span data-ttu-id="0fc7e-118">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="0fc7e-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="0fc7e-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0fc7e-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0fc7e-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0fc7e-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0fc7e-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0fc7e-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0fc7e-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0fc7e-122">Schema Name</span></span>  <br/> |<span data-ttu-id="0fc7e-123">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0fc7e-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="0fc7e-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0fc7e-124">Validation File</span></span>  <br/> |<span data-ttu-id="0fc7e-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0fc7e-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0fc7e-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0fc7e-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="0fc7e-127">Verdadero</span><span class="sxs-lookup"><span data-stu-id="0fc7e-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0fc7e-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="0fc7e-128">See also</span></span>



[<span data-ttu-id="0fc7e-129">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="0fc7e-129">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)


- [<span data-ttu-id="0fc7e-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="0fc7e-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

