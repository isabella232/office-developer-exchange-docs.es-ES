---
title: EnableAlwaysDelete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EnableAlwaysDelete
api_type:
- schema
ms.assetid: 7753aec5-3f93-4aeb-a28e-8b9b42ca7f9b
description: El elemento EnableAlwaysDelete especifica una marca que permite la eliminación para todos los elementos nuevos de una conversación.
ms.openlocfilehash: 14784d3a6ba52c76b64b81e15c0522d66d125cbf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526210"
---
# <a name="enablealwaysdelete"></a><span data-ttu-id="52d92-103">EnableAlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="52d92-103">EnableAlwaysDelete</span></span>

<span data-ttu-id="52d92-104">El elemento **EnableAlwaysDelete** especifica una marca que permite la eliminación para todos los elementos nuevos de una conversación.</span><span class="sxs-lookup"><span data-stu-id="52d92-104">The **EnableAlwaysDelete** element specifies a flag that enables deletion for all new items in a conversation.</span></span> 
  
[<span data-ttu-id="52d92-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="52d92-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="52d92-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="52d92-106">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="52d92-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="52d92-107">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="52d92-108">EnableAlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="52d92-108">EnableAlwaysDelete</span></span>](enablealwaysdelete.md)
  
```XML
<EnableAlwaysDelete/>
```

 <span data-ttu-id="52d92-109">**XS: Boolean**</span><span class="sxs-lookup"><span data-stu-id="52d92-109">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52d92-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="52d92-110">Attributes and elements</span></span>

<span data-ttu-id="52d92-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="52d92-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52d92-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="52d92-112">Attributes</span></span>

<span data-ttu-id="52d92-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="52d92-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="52d92-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="52d92-114">Child elements</span></span>

<span data-ttu-id="52d92-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="52d92-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="52d92-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="52d92-116">Parent elements</span></span>

|<span data-ttu-id="52d92-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="52d92-117">**Element**</span></span>|<span data-ttu-id="52d92-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="52d92-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52d92-119">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="52d92-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="52d92-120">Contiene una sola acción que se aplicará a una única conversación.</span><span class="sxs-lookup"><span data-stu-id="52d92-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="52d92-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="52d92-121">Text value</span></span>

<span data-ttu-id="52d92-122">El valor de texto del elemento **EnableAlwaysDelete** es **true** para permitir la eliminación de todos los elementos de la conversación; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="52d92-122">The text value of the **EnableAlwaysDelete** element is **true** to enable the deletion of all items in conversation; otherwise, **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52d92-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52d92-123">Remarks</span></span>

<span data-ttu-id="52d92-124">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="52d92-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52d92-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="52d92-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52d92-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="52d92-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="52d92-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="52d92-127">Schema Name</span></span>  <br/> |<span data-ttu-id="52d92-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="52d92-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="52d92-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="52d92-129">Validation File</span></span>  <br/> |<span data-ttu-id="52d92-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="52d92-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="52d92-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="52d92-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="52d92-132">Falso</span><span class="sxs-lookup"><span data-stu-id="52d92-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52d92-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="52d92-133">See also</span></span>



[<span data-ttu-id="52d92-134">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="52d92-134">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)

