---
title: GlobalHasIrm
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 425272b2-7a4e-4376-aea9-d9b10c1ad6ee
description: El elemento GlobalHasIrm especifica si al menos un mensaje de la conversación y de todas las carpetas es un mensaje protegido por IRM.
ms.openlocfilehash: 10b99c9a6421a89a549b69e918087f3e542ffa09
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459472"
---
# <a name="globalhasirm"></a><span data-ttu-id="29740-103">GlobalHasIrm</span><span class="sxs-lookup"><span data-stu-id="29740-103">GlobalHasIrm</span></span>

<span data-ttu-id="29740-104">El elemento **GlobalHasIrm** especifica si al menos un mensaje de la conversación y de todas las carpetas es un mensaje protegido por IRM.</span><span class="sxs-lookup"><span data-stu-id="29740-104">The **GlobalHasIrm** element specifies whether at least one message in the conversation and across all folders is an IRM protected message.</span></span> 
  
```XML
<GlobalHasIrm> true | false </GlobalHasIrm>
```

 <span data-ttu-id="29740-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="29740-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="29740-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="29740-106">Attributes and elements</span></span>

<span data-ttu-id="29740-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="29740-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="29740-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="29740-108">Attributes</span></span>

<span data-ttu-id="29740-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="29740-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="29740-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="29740-110">Child elements</span></span>

<span data-ttu-id="29740-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="29740-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="29740-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="29740-112">Parent elements</span></span>

[<span data-ttu-id="29740-113">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="29740-113">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
## <a name="text-value"></a><span data-ttu-id="29740-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="29740-114">Text value</span></span>

<span data-ttu-id="29740-115">El valor de texto del elemento **GlobalHasIrm** es **true** si al menos un mensaje en la conversación y en todas las carpetas es un mensaje protegido por IRM.</span><span class="sxs-lookup"><span data-stu-id="29740-115">The text value of the **GlobalHasIrm** element is **true** if at least one message in the conversation and across all folders is an IRM protected message.</span></span> <span data-ttu-id="29740-116">De lo contrario, el valor es **false**.</span><span class="sxs-lookup"><span data-stu-id="29740-116">Otherwise the value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="29740-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="29740-117">Remarks</span></span>

<span data-ttu-id="29740-118">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="29740-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="29740-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="29740-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="29740-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="29740-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="29740-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="29740-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="29740-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="29740-122">Schema Name</span></span>  <br/> |<span data-ttu-id="29740-123">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="29740-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="29740-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="29740-124">Validation File</span></span>  <br/> |<span data-ttu-id="29740-125">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="29740-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="29740-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="29740-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="29740-127">Verdadero</span><span class="sxs-lookup"><span data-stu-id="29740-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="29740-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="29740-128">See also</span></span>



[<span data-ttu-id="29740-129">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="29740-129">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)


- [<span data-ttu-id="29740-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="29740-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

