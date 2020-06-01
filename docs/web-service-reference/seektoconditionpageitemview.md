---
title: SeekToConditionPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b3b86720-d086-47c3-94af-921fdd719edf
description: El elemento SeekToConditionPageItemView identifica la condición que se usa para identificar el final de una búsqueda, el índice inicial de una búsqueda, las entradas máximas que se devolverán y las direcciones de búsqueda de una búsqueda de FindItem o FindConversation.
ms.openlocfilehash: dbb073263740ccdf75367f85f672b7d5ec78f7a0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466839"
---
# <a name="seektoconditionpageitemview"></a><span data-ttu-id="30209-103">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="30209-103">SeekToConditionPageItemView</span></span>

<span data-ttu-id="30209-104">El elemento **SeekToConditionPageItemView** identifica la condición que se usa para identificar el final de una búsqueda, el índice inicial de una búsqueda, las entradas máximas que se devolverán y las direcciones de búsqueda de una búsqueda de **FindItem** o **FindConversation** .</span><span class="sxs-lookup"><span data-stu-id="30209-104">The **SeekToConditionPageItemView** element identifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or **FindConversation** search.</span></span> 
  
```XML
<SeekToConditionPageItemView BasePoint="" MaxEntriesReturned="">
   <Condition/>
</SeekToConditionPageItemView>
```

 <span data-ttu-id="30209-105">**SeekToConditionPageViewType**</span><span class="sxs-lookup"><span data-stu-id="30209-105">**SeekToConditionPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="30209-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="30209-106">Attributes and elements</span></span>

<span data-ttu-id="30209-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="30209-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="30209-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="30209-108">Attributes</span></span>

|<span data-ttu-id="30209-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="30209-109">**Attribute**</span></span>|<span data-ttu-id="30209-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="30209-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="30209-111">BasePoint</span><span class="sxs-lookup"><span data-stu-id="30209-111">BasePoint</span></span>  <br/> |<span data-ttu-id="30209-112">El valor de texto del atributo **BasePoint** es el punto base desde el que se iniciará la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="30209-112">The text value of the **BasePoint** attribute is the base point from where the search will start.</span></span> <span data-ttu-id="30209-113">Un valor de texto **inicial** indica que la búsqueda se iniciará al principio del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="30209-113">A text value of **Beginning** indicates that the search will start at the beginning of the result set.</span></span> <span data-ttu-id="30209-114">Un valor de texto de **End** indica que la búsqueda comenzará al final del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="30209-114">A text value of **End** indicates that the search will start at the end of the result set.</span></span>  <br/> |
|<span data-ttu-id="30209-115">MaxEntriesReturned</span><span class="sxs-lookup"><span data-stu-id="30209-115">MaxEntriesReturned</span></span>  <br/> |<span data-ttu-id="30209-116">El valor de texto del atributo **MaxEntriesReturned** es el número máximo de elementos que se pueden devolver en un conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="30209-116">The text value of the **MaxEntriesReturned** attribute is the maximum number of items that can be returned in a result set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="30209-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="30209-117">Child elements</span></span>

[<span data-ttu-id="30209-118">Condición (RestrictionType)</span><span class="sxs-lookup"><span data-stu-id="30209-118">Condition (RestrictionType)</span></span>](condition-restrictiontype.md)
  
### <a name="parent-elements"></a><span data-ttu-id="30209-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="30209-119">Parent elements</span></span>

<span data-ttu-id="30209-120">[FindConversation](findconversation.md)  |  [FindItem](finditem.md)</span><span class="sxs-lookup"><span data-stu-id="30209-120">[FindConversation](findconversation.md) | [FindItem](finditem.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="30209-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="30209-121">Remarks</span></span>

<span data-ttu-id="30209-122">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="30209-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="30209-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="30209-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="30209-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="30209-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30209-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="30209-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="30209-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="30209-126">Schema name</span></span>  <br/> |<span data-ttu-id="30209-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="30209-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="30209-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="30209-128">Validation file</span></span>  <br/> |<span data-ttu-id="30209-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="30209-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="30209-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="30209-130">Can be empty</span></span>  <br/> |<span data-ttu-id="30209-131">false</span><span class="sxs-lookup"><span data-stu-id="30209-131">false</span></span>  <br/> |
   

