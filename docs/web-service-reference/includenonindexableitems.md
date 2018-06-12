---
title: IncludeNonIndexableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: af7f202b-2889-447e-bdeb-aaad18ce6b46
description: El elemento IncludeNonIndexableItems contiene un valor booleano para indicar si se incluyen los elementos que no se pueden indizar.
ms.openlocfilehash: ae91a3c6db82aea1d45940603d0ff2064d29f43f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835904"
---
# <a name="includenonindexableitems"></a><span data-ttu-id="0d968-103">IncludeNonIndexableItems</span><span class="sxs-lookup"><span data-stu-id="0d968-103">IncludeNonIndexableItems</span></span>

<span data-ttu-id="0d968-104">El elemento **IncludeNonIndexableItems** contiene un valor **booleano** para indicar si se incluyen los elementos que no se pueden indizar.</span><span class="sxs-lookup"><span data-stu-id="0d968-104">The **IncludeNonIndexableItems** element contains a **Boolean** value to indicate whether to include items that cannot be indexed.</span></span> 
  
```XML
<IncludeNonIndexableItems>true | false</IncludeNonIndexableItems>
```

 <span data-ttu-id="0d968-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0d968-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0d968-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0d968-106">Attributes and elements</span></span>

<span data-ttu-id="0d968-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0d968-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d968-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0d968-108">Attributes</span></span>

<span data-ttu-id="0d968-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0d968-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0d968-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0d968-110">Child elements</span></span>

<span data-ttu-id="0d968-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0d968-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0d968-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0d968-112">Parent elements</span></span>

[<span data-ttu-id="0d968-113">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="0d968-113">SetHoldOnMailboxes</span></span>](setholdonmailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="0d968-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0d968-114">Text value</span></span>

<span data-ttu-id="0d968-115">Un valor de texto de **true** para el elemento **IncludeNonIndexableItems** indica que los elementos que no se pueden indizar se incluyen con suspensiones de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0d968-115">A text value of **true** for the **IncludeNonIndexableItems** element indicates that items that cannot be indexed are included with mailbox holds.</span></span> <span data-ttu-id="0d968-116">Un valor de **false** indica que no se incluyen los elementos que no se pueden indizar en suspensiones de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="0d968-116">A value of **false** indicates that the items that cannot be indexed are not included in mailbox holds.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0d968-117">Notas</span><span class="sxs-lookup"><span data-stu-id="0d968-117">Remarks</span></span>

<span data-ttu-id="0d968-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0d968-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0d968-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0d968-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0d968-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0d968-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d968-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0d968-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0d968-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0d968-122">Schema name</span></span>  <br/> |<span data-ttu-id="0d968-123">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0d968-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0d968-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0d968-124">Validation file</span></span>  <br/> |<span data-ttu-id="0d968-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0d968-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0d968-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0d968-126">Can be empty</span></span>  <br/> |<span data-ttu-id="0d968-127">falso</span><span class="sxs-lookup"><span data-stu-id="0d968-127">false</span></span>  <br/> |
   

