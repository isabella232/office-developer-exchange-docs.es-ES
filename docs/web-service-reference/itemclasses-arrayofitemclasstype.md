---
title: ItemClasses (ArrayOfItemClassType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 971784d1-6860-4833-bb26-0e930fa11c21
description: El elemento ItemClasses contiene una lista de las clases de elementos que representa todas las clases de elemento de los elementos de conversación en la carpeta actual.
ms.openlocfilehash: 62ea5b624025b3f012249afd1763e2b393ef5caa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836150"
---
# <a name="itemclasses-arrayofitemclasstype"></a><span data-ttu-id="a66a1-103">ItemClasses (ArrayOfItemClassType)</span><span class="sxs-lookup"><span data-stu-id="a66a1-103">ItemClasses (ArrayOfItemClassType)</span></span>

<span data-ttu-id="a66a1-104">El elemento **ItemClasses** contiene una lista de las clases de elementos que representa todas las clases de elemento de los elementos de conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="a66a1-104">The **ItemClasses** element contains a list of item classes that represents all the item classes of the conversation items in the current folder.</span></span> 
  
[<span data-ttu-id="a66a1-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="a66a1-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="a66a1-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="a66a1-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="a66a1-107">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="a66a1-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="a66a1-108">ItemClasses (ArrayOfItemClassType)</span><span class="sxs-lookup"><span data-stu-id="a66a1-108">ItemClasses (ArrayOfItemClassType)</span></span>](itemclasses-arrayofitemclasstype.md)
  
```XML
<ItemClasses>
    <String/>
</ItemClasses>
```

 <span data-ttu-id="a66a1-109">**ArrayOfItemClassType**</span><span class="sxs-lookup"><span data-stu-id="a66a1-109">**ArrayOfItemClassType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a66a1-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a66a1-110">Attributes and elements</span></span>

<span data-ttu-id="a66a1-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a66a1-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a66a1-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="a66a1-112">Attributes</span></span>

<span data-ttu-id="a66a1-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a66a1-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a66a1-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a66a1-114">Child elements</span></span>

|<span data-ttu-id="a66a1-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="a66a1-115">**Element**</span></span>|<span data-ttu-id="a66a1-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a66a1-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a66a1-117">ItemClass</span><span class="sxs-lookup"><span data-stu-id="a66a1-117">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="a66a1-118">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="a66a1-118">Represents the message class of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a66a1-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a66a1-119">Parent elements</span></span>

|<span data-ttu-id="a66a1-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="a66a1-120">**Element**</span></span>|<span data-ttu-id="a66a1-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a66a1-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a66a1-122">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="a66a1-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="a66a1-123">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="a66a1-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a66a1-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a66a1-124">Text value</span></span>

<span data-ttu-id="a66a1-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a66a1-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a66a1-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a66a1-126">Remarks</span></span>

<span data-ttu-id="a66a1-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a66a1-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a66a1-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a66a1-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a66a1-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a66a1-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a66a1-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a66a1-130">Schema name</span></span>  <br/> |<span data-ttu-id="a66a1-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a66a1-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="a66a1-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a66a1-132">Validation file</span></span>  <br/> |<span data-ttu-id="a66a1-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a66a1-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a66a1-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a66a1-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="a66a1-135">False</span><span class="sxs-lookup"><span data-stu-id="a66a1-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a66a1-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a66a1-136">See also</span></span>



[<span data-ttu-id="a66a1-137">Operación de FindConversation</span><span class="sxs-lookup"><span data-stu-id="a66a1-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="a66a1-138">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="a66a1-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="a66a1-139">Conversaciones de EWS</span><span class="sxs-lookup"><span data-stu-id="a66a1-139">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

