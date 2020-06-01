---
title: ItemClasses (ArrayOfItemClassType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 971784d1-6860-4833-bb26-0e930fa11c21
description: El elemento ItemClasses contiene una lista de clases de elementos que representa todas las clases de elementos de la conversación en la carpeta actual.
ms.openlocfilehash: 39118bf845429bb198874ae4e6b424c6339b1964
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467301"
---
# <a name="itemclasses-arrayofitemclasstype"></a><span data-ttu-id="99549-103">ItemClasses (ArrayOfItemClassType)</span><span class="sxs-lookup"><span data-stu-id="99549-103">ItemClasses (ArrayOfItemClassType)</span></span>

<span data-ttu-id="99549-104">El elemento **ItemClasses** contiene una lista de clases de elementos que representa todas las clases de elementos de la conversación en la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="99549-104">The **ItemClasses** element contains a list of item classes that represents all the item classes of the conversation items in the current folder.</span></span> 
  
[<span data-ttu-id="99549-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="99549-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="99549-106">Conversaciones</span><span class="sxs-lookup"><span data-stu-id="99549-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="99549-107">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="99549-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="99549-108">ItemClasses (ArrayOfItemClassType)</span><span class="sxs-lookup"><span data-stu-id="99549-108">ItemClasses (ArrayOfItemClassType)</span></span>](itemclasses-arrayofitemclasstype.md)
  
```XML
<ItemClasses>
    <String/>
</ItemClasses>
```

 <span data-ttu-id="99549-109">**ArrayOfItemClassType**</span><span class="sxs-lookup"><span data-stu-id="99549-109">**ArrayOfItemClassType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="99549-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="99549-110">Attributes and elements</span></span>

<span data-ttu-id="99549-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="99549-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="99549-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="99549-112">Attributes</span></span>

<span data-ttu-id="99549-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="99549-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="99549-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="99549-114">Child elements</span></span>

|<span data-ttu-id="99549-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99549-115">**Element**</span></span>|<span data-ttu-id="99549-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99549-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99549-117">ItemClass</span><span class="sxs-lookup"><span data-stu-id="99549-117">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="99549-118">Representa la clase de mensaje de un elemento.</span><span class="sxs-lookup"><span data-stu-id="99549-118">Represents the message class of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="99549-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="99549-119">Parent elements</span></span>

|<span data-ttu-id="99549-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="99549-120">**Element**</span></span>|<span data-ttu-id="99549-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="99549-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="99549-122">Conversación (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="99549-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="99549-123">Representa una sola conversación.</span><span class="sxs-lookup"><span data-stu-id="99549-123">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="99549-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="99549-124">Text value</span></span>

<span data-ttu-id="99549-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="99549-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="99549-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="99549-126">Remarks</span></span>

<span data-ttu-id="99549-127">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange. este elemento se introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="99549-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="99549-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="99549-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99549-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="99549-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="99549-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="99549-130">Schema name</span></span>  <br/> |<span data-ttu-id="99549-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="99549-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="99549-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="99549-132">Validation file</span></span>  <br/> |<span data-ttu-id="99549-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="99549-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="99549-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="99549-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="99549-135">Falso</span><span class="sxs-lookup"><span data-stu-id="99549-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99549-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="99549-136">See also</span></span>



[<span data-ttu-id="99549-137">Operación FindConversation</span><span class="sxs-lookup"><span data-stu-id="99549-137">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="99549-138">Operación ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="99549-138">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="99549-139">Conversaciones en EWS</span><span class="sxs-lookup"><span data-stu-id="99549-139">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

