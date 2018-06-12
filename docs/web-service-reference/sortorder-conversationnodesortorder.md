---
title: SortOrder (ConversationNodeSortOrder)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9c4295c-8089-4533-b92f-2051eae9afeb
description: El elemento SortOrder especifica el criterio de ordenación que se usan en el resultado de una solicitud de GetConversationItems.
ms.openlocfilehash: 397aead62d32e72f991af783bff02e79a6e4b0fb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837520"
---
# <a name="sortorder-conversationnodesortorder"></a><span data-ttu-id="25b32-103">SortOrder (ConversationNodeSortOrder)</span><span class="sxs-lookup"><span data-stu-id="25b32-103">SortOrder (ConversationNodeSortOrder)</span></span>

<span data-ttu-id="25b32-104">El elemento **SortOrder** especifica el criterio de ordenación que se usan en el resultado de una solicitud de **GetConversationItems** .</span><span class="sxs-lookup"><span data-stu-id="25b32-104">The **SortOrder** element specifies the sort order used for the result of a **GetConversationItems** request.</span></span> 
  
```XML
<SortOrder>TreeOrderAscending | TreeOrderDescending | DateOrderAscending | DateOrderDescending</SortOrder>
```

 <span data-ttu-id="25b32-105">**ConversationNodeSortOrder**</span><span class="sxs-lookup"><span data-stu-id="25b32-105">**ConversationNodeSortOrder**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="25b32-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="25b32-106">Attributes and elements</span></span>

<span data-ttu-id="25b32-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="25b32-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25b32-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="25b32-108">Attributes</span></span>

<span data-ttu-id="25b32-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="25b32-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="25b32-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="25b32-110">Child elements</span></span>

<span data-ttu-id="25b32-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="25b32-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="25b32-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="25b32-112">Parent elements</span></span>

[<span data-ttu-id="25b32-113">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="25b32-113">GetConversationItems</span></span>](getconversationitems.md)
  
## <a name="text-value"></a><span data-ttu-id="25b32-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="25b32-114">Text value</span></span>

<span data-ttu-id="25b32-115">El valor de texto del elemento **SortOrder** es el orden en que se ordenan las conversaciones.</span><span class="sxs-lookup"><span data-stu-id="25b32-115">The text value of the **SortOrder** element is the order in which conversations ordered.</span></span> <span data-ttu-id="25b32-116">Un valor de texto de **TreeOrderAscending** indica que las conversaciones se ordenan según el árbol de la conversación en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="25b32-116">A text value of **TreeOrderAscending** indicates that the conversations are ordered according to the conversation tree in ascending order.</span></span> <span data-ttu-id="25b32-117">Un valor de texto de **TreeOrderDescending** indica que las conversaciones se ordenan según el árbol de la conversación en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="25b32-117">A text value of **TreeOrderDescending** indicates that the conversations are ordered according to the conversation tree in descending order.</span></span> <span data-ttu-id="25b32-118">Un valor de texto de **DateOrderAscending** indica que las conversaciones se ordenan según la fecha de conversación en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="25b32-118">A text value of **DateOrderAscending** indicates that the conversations are ordered according to the conversation date in ascending order.</span></span> <span data-ttu-id="25b32-119">Un valor de texto de **DateOrderDescending** indica que las conversaciones se ordenan según la fecha de conversación en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="25b32-119">A text value of **DateOrderDescending** indicates that the conversations are ordered according to the conversation date in descending order.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="25b32-120">Notas</span><span class="sxs-lookup"><span data-stu-id="25b32-120">Remarks</span></span>

<span data-ttu-id="25b32-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="25b32-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="25b32-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="25b32-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="25b32-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="25b32-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25b32-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="25b32-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="25b32-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="25b32-125">Schema name</span></span>  <br/> |<span data-ttu-id="25b32-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="25b32-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="25b32-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="25b32-127">Validation file</span></span>  <br/> |<span data-ttu-id="25b32-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="25b32-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="25b32-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="25b32-129">Can be empty</span></span>  <br/> ||
   

