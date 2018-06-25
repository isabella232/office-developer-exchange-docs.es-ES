---
title: SeekToConditionPageItemView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b3b86720-d086-47c3-94af-921fdd719edf
description: El elemento SeekToConditionPageItemView identifica la condición que se usa para identificar el final de una búsqueda, el índice de inicio de una búsqueda, las entradas máximas para devolver y las instrucciones de búsqueda para una búsqueda FindItem o FindConversation.
ms.openlocfilehash: e95246079f8c6e7acffac1dabb278895265767d9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837328"
---
# <a name="seektoconditionpageitemview"></a><span data-ttu-id="2dec9-103">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="2dec9-103">SeekToConditionPageItemView</span></span>

<span data-ttu-id="2dec9-104">El elemento **SeekToConditionPageItemView** identifica la condición que se usa para identificar el final de una búsqueda, el índice de inicio de una búsqueda, las entradas máximas para devolver y las instrucciones de búsqueda para un **FindItem** o **FindConversation **búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2dec9-104">The **SeekToConditionPageItemView** element identifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or **FindConversation** search.</span></span> 
  
```XML
<SeekToConditionPageItemView BasePoint="" MaxEntriesReturned="">
   <Condition/>
</SeekToConditionPageItemView>
```

 <span data-ttu-id="2dec9-105">**SeekToConditionPageViewType**</span><span class="sxs-lookup"><span data-stu-id="2dec9-105">**SeekToConditionPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2dec9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2dec9-106">Attributes and elements</span></span>

<span data-ttu-id="2dec9-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2dec9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2dec9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2dec9-108">Attributes</span></span>

|<span data-ttu-id="2dec9-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="2dec9-109">**Attribute**</span></span>|<span data-ttu-id="2dec9-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2dec9-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2dec9-111">Punto base</span><span class="sxs-lookup"><span data-stu-id="2dec9-111">BasePoint</span></span>  <br/> |<span data-ttu-id="2dec9-112">El valor de texto del atributo **punto base** es el punto de partida desde donde se iniciará la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2dec9-112">The text value of the **BasePoint** attribute is the base point from where the search will start.</span></span> <span data-ttu-id="2dec9-113">Un valor de texto de **principio** indica que la búsqueda se iniciará al principio del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="2dec9-113">A text value of **Beginning** indicates that the search will start at the beginning of the result set.</span></span> <span data-ttu-id="2dec9-114">Un valor de texto de **final** indica que la búsqueda se iniciará al final del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="2dec9-114">A text value of **End** indicates that the search will start at the end of the result set.</span></span>  <br/> |
|<span data-ttu-id="2dec9-115">MaxEntriesReturned</span><span class="sxs-lookup"><span data-stu-id="2dec9-115">MaxEntriesReturned</span></span>  <br/> |<span data-ttu-id="2dec9-116">El valor de texto del atributo **MaxEntriesReturned** es el número máximo de elementos que se pueden devolver en un conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="2dec9-116">The text value of the **MaxEntriesReturned** attribute is the maximum number of items that can be returned in a result set.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2dec9-117">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2dec9-117">Child elements</span></span>

[<span data-ttu-id="2dec9-118">Condición (RestrictionType)</span><span class="sxs-lookup"><span data-stu-id="2dec9-118">Condition (RestrictionType)</span></span>](condition-restrictiontype.md)
  
### <a name="parent-elements"></a><span data-ttu-id="2dec9-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2dec9-119">Parent elements</span></span>

<span data-ttu-id="2dec9-120">[FindConversation](findconversation.md) | [FindItem](finditem.md)</span><span class="sxs-lookup"><span data-stu-id="2dec9-120">[FindConversation](findconversation.md) | [FindItem](finditem.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2dec9-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2dec9-121">Remarks</span></span>

<span data-ttu-id="2dec9-122">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2dec9-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2dec9-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2dec9-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2dec9-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2dec9-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2dec9-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2dec9-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2dec9-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2dec9-126">Schema name</span></span>  <br/> |<span data-ttu-id="2dec9-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="2dec9-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2dec9-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2dec9-128">Validation file</span></span>  <br/> |<span data-ttu-id="2dec9-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2dec9-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2dec9-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2dec9-130">Can be empty</span></span>  <br/> |<span data-ttu-id="2dec9-131">falso</span><span class="sxs-lookup"><span data-stu-id="2dec9-131">false</span></span>  <br/> |
   

