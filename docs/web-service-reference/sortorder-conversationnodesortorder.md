---
title: SortOrder (ConversationNodeSortOrder)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9c4295c-8089-4533-b92f-2051eae9afeb
description: El elemento SortOrder especifica el criterio de ordenación usado para el resultado de una solicitud GetConversationItems.
ms.openlocfilehash: 69d362b9f769749bcc9692825b64ff486e8b60a0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530968"
---
# <a name="sortorder-conversationnodesortorder"></a><span data-ttu-id="eadb1-103">SortOrder (ConversationNodeSortOrder)</span><span class="sxs-lookup"><span data-stu-id="eadb1-103">SortOrder (ConversationNodeSortOrder)</span></span>

<span data-ttu-id="eadb1-104">El elemento **SortOrder** especifica el criterio de ordenación usado para el resultado de una solicitud **GetConversationItems** .</span><span class="sxs-lookup"><span data-stu-id="eadb1-104">The **SortOrder** element specifies the sort order used for the result of a **GetConversationItems** request.</span></span> 
  
```XML
<SortOrder>TreeOrderAscending | TreeOrderDescending | DateOrderAscending | DateOrderDescending</SortOrder>
```

 <span data-ttu-id="eadb1-105">**ConversationNodeSortOrder**</span><span class="sxs-lookup"><span data-stu-id="eadb1-105">**ConversationNodeSortOrder**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eadb1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="eadb1-106">Attributes and elements</span></span>

<span data-ttu-id="eadb1-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="eadb1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eadb1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="eadb1-108">Attributes</span></span>

<span data-ttu-id="eadb1-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="eadb1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eadb1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eadb1-110">Child elements</span></span>

<span data-ttu-id="eadb1-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="eadb1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eadb1-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="eadb1-112">Parent elements</span></span>

[<span data-ttu-id="eadb1-113">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="eadb1-113">GetConversationItems</span></span>](getconversationitems.md)
  
## <a name="text-value"></a><span data-ttu-id="eadb1-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="eadb1-114">Text value</span></span>

<span data-ttu-id="eadb1-115">El valor de texto del elemento **SortOrder** es el orden en el que se ordenan las conversaciones.</span><span class="sxs-lookup"><span data-stu-id="eadb1-115">The text value of the **SortOrder** element is the order in which conversations ordered.</span></span> <span data-ttu-id="eadb1-116">Un valor de texto de **TreeOrderAscending** indica que las conversaciones se ordenan de acuerdo con el árbol de conversaciones en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="eadb1-116">A text value of **TreeOrderAscending** indicates that the conversations are ordered according to the conversation tree in ascending order.</span></span> <span data-ttu-id="eadb1-117">Un valor de texto de **TreeOrderDescending** indica que las conversaciones se ordenan de acuerdo con el árbol de conversación en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="eadb1-117">A text value of **TreeOrderDescending** indicates that the conversations are ordered according to the conversation tree in descending order.</span></span> <span data-ttu-id="eadb1-118">Un valor de texto de **DateOrderAscending** indica que las conversaciones se ordenan en función de la fecha de la conversación en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="eadb1-118">A text value of **DateOrderAscending** indicates that the conversations are ordered according to the conversation date in ascending order.</span></span> <span data-ttu-id="eadb1-119">Un valor de texto de **DateOrderDescending** indica que las conversaciones se ordenan según la fecha de la conversación en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="eadb1-119">A text value of **DateOrderDescending** indicates that the conversations are ordered according to the conversation date in descending order.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="eadb1-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eadb1-120">Remarks</span></span>

<span data-ttu-id="eadb1-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="eadb1-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="eadb1-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="eadb1-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eadb1-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="eadb1-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eadb1-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="eadb1-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="eadb1-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="eadb1-125">Schema name</span></span>  <br/> |<span data-ttu-id="eadb1-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="eadb1-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="eadb1-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="eadb1-127">Validation file</span></span>  <br/> |<span data-ttu-id="eadb1-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="eadb1-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eadb1-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="eadb1-129">Can be empty</span></span>  <br/> ||
   

