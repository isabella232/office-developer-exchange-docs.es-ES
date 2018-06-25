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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764394"
---
# <a name="enablealwaysdelete"></a><span data-ttu-id="ca486-103">EnableAlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="ca486-103">EnableAlwaysDelete</span></span>

<span data-ttu-id="ca486-104">El elemento **EnableAlwaysDelete** especifica una marca que habilita la eliminación de todos los elementos nuevos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="ca486-104">The **EnableAlwaysDelete** element specifies a flag that enables deletion for all new items in a conversation.</span></span> 
  
[<span data-ttu-id="ca486-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="ca486-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="ca486-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="ca486-106">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="ca486-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="ca486-107">ConversationAction</span></span>](conversationaction.md)
  
[<span data-ttu-id="ca486-108">EnableAlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="ca486-108">EnableAlwaysDelete</span></span>](enablealwaysdelete.md)
  
```XML
<EnableAlwaysDelete/>
```

 <span data-ttu-id="ca486-109">**xs: Boolean**</span><span class="sxs-lookup"><span data-stu-id="ca486-109">**xs:boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ca486-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ca486-110">Attributes and elements</span></span>

<span data-ttu-id="ca486-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ca486-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ca486-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="ca486-112">Attributes</span></span>

<span data-ttu-id="ca486-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ca486-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ca486-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ca486-114">Child elements</span></span>

<span data-ttu-id="ca486-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ca486-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ca486-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ca486-116">Parent elements</span></span>

|<span data-ttu-id="ca486-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="ca486-117">**Element**</span></span>|<span data-ttu-id="ca486-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ca486-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ca486-119">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="ca486-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="ca486-120">Contiene una única acción que se aplicará a una conversación único.</span><span class="sxs-lookup"><span data-stu-id="ca486-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ca486-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ca486-121">Text value</span></span>

<span data-ttu-id="ca486-122">El valor de texto del elemento **EnableAlwaysDelete** es **true** para habilitar la eliminación de todos los elementos de conversación; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="ca486-122">The text value of the **EnableAlwaysDelete** element is **true** to enable the deletion of all items in conversation; otherwise, **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ca486-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ca486-123">Remarks</span></span>

<span data-ttu-id="ca486-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ca486-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ca486-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ca486-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca486-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ca486-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ca486-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ca486-127">Schema Name</span></span>  <br/> |<span data-ttu-id="ca486-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="ca486-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="ca486-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ca486-129">Validation File</span></span>  <br/> |<span data-ttu-id="ca486-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ca486-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ca486-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ca486-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="ca486-132">False</span><span class="sxs-lookup"><span data-stu-id="ca486-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca486-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca486-133">See also</span></span>



[<span data-ttu-id="ca486-134">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="ca486-134">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)

