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
description: El elemento EnableAlwaysDelete especifica una marca que habilita la eliminación de todos los elementos nuevos en una conversación.
ms.openlocfilehash: f86765c641604afbf13ac962f4b34fbd8de56200
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764394"
---
# <a name="enablealwaysdelete"></a><span data-ttu-id="277db-103">EnableAlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="277db-103">EnableAlwaysDelete</span></span>

<span data-ttu-id="277db-104">El elemento **EnableAlwaysDelete** especifica una marca que habilita la eliminación de todos los elementos nuevos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="277db-104">The **EnableAlwaysDelete** element specifies a flag that enables deletion for all new items in a conversation.</span></span> 
  
[<span data-ttu-id="277db-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="277db-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="277db-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="277db-106">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="277db-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="277db-107">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="277db-108">EnableAlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="277db-108">EnableAlwaysDelete</span></span>](enablealwaysdelete.md)
  
```XML
<EnableAlwaysDelete/>
```

 <span data-ttu-id="277db-109">**xs: Boolean**</span><span class="sxs-lookup"><span data-stu-id="277db-109">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="277db-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="277db-110">Attributes and elements</span></span>

<span data-ttu-id="277db-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="277db-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="277db-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="277db-112">Attributes</span></span>

<span data-ttu-id="277db-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="277db-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="277db-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="277db-114">Child elements</span></span>

<span data-ttu-id="277db-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="277db-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="277db-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="277db-116">Parent elements</span></span>

|<span data-ttu-id="277db-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="277db-117">**Element**</span></span>|<span data-ttu-id="277db-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="277db-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="277db-119">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="277db-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="277db-120">Contiene una única acción que se aplicará a una conversación único.</span><span class="sxs-lookup"><span data-stu-id="277db-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="277db-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="277db-121">Text value</span></span>

<span data-ttu-id="277db-122">El valor de texto del elemento **EnableAlwaysDelete** es **true** para habilitar la eliminación de todos los elementos de conversación; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="277db-122">The text value of the **EnableAlwaysDelete** element is **true** to enable the deletion of all items in conversation; otherwise, **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="277db-123">Notas</span><span class="sxs-lookup"><span data-stu-id="277db-123">Remarks</span></span>

<span data-ttu-id="277db-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="277db-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="277db-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="277db-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="277db-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="277db-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="277db-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="277db-127">Schema Name</span></span>  <br/> |<span data-ttu-id="277db-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="277db-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="277db-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="277db-129">Validation File</span></span>  <br/> |<span data-ttu-id="277db-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="277db-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="277db-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="277db-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="277db-132">False</span><span class="sxs-lookup"><span data-stu-id="277db-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="277db-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="277db-133">See also</span></span>



[<span data-ttu-id="277db-134">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="277db-134">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)

