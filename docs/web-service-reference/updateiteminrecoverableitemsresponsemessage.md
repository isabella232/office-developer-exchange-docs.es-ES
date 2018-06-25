---
title: UpdateItemInRecoverableItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96259756-322e-4c24-ac76-0cd9c32e0d6d
description: El elemento UpdateItemInRecoverableItemsResponseMessage especifica la respuesta a una solicitud de UpdateItemInRecoverableItems.
ms.openlocfilehash: 598d91a4fbd4d241b75aea4c155caca68f120b3f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840844"
---
# <a name="updateiteminrecoverableitemsresponsemessage"></a><span data-ttu-id="93c90-103">UpdateItemInRecoverableItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="93c90-103">UpdateItemInRecoverableItemsResponseMessage</span></span>

<span data-ttu-id="93c90-104">El elemento **UpdateItemInRecoverableItemsResponseMessage** especifica la respuesta a una solicitud de **UpdateItemInRecoverableItems** .</span><span class="sxs-lookup"><span data-stu-id="93c90-104">The **UpdateItemInRecoverableItemsResponseMessage** element specifies the response to an **UpdateItemInRecoverableItems** request.</span></span> 
  
```XML
<UpdateItemInRecoverableItemsResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKet/>
   <MessageXml/>
   <Items/>
   <Attachments/>
   <ConflictResults/>
</UpdateItemInRecoverableItemsResponseMessage>
```

 <span data-ttu-id="93c90-105">**UpdateItemInRecoverableItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="93c90-105">**UpdateItemInRecoverableItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="93c90-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="93c90-106">Attributes and elements</span></span>

<span data-ttu-id="93c90-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="93c90-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="93c90-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="93c90-108">Attributes</span></span>

<span data-ttu-id="93c90-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="93c90-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="93c90-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="93c90-110">Child elements</span></span>

<span data-ttu-id="93c90-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [elementos](items.md) | [datos adjuntos](attachments-ex15websvcsotherref.md) | [ConflictResults](conflictresults.md)</span><span class="sxs-lookup"><span data-stu-id="93c90-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [Items](items.md) | [Attachments](attachments-ex15websvcsotherref.md) | [ConflictResults](conflictresults.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="93c90-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="93c90-112">Parent elements</span></span>

<span data-ttu-id="93c90-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="93c90-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="93c90-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="93c90-114">Remarks</span></span>

<span data-ttu-id="93c90-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="93c90-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="93c90-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="93c90-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="93c90-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="93c90-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="93c90-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="93c90-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|<span data-ttu-id="93c90-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="93c90-119">Schema name</span></span>  <br/> |<span data-ttu-id="93c90-120">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="93c90-120">Message schema</span></span>  <br/> |
|<span data-ttu-id="93c90-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="93c90-121">Validation file</span></span>  <br/> |<span data-ttu-id="93c90-122">Message.xsd</span><span class="sxs-lookup"><span data-stu-id="93c90-122">Message.xsd</span></span>  <br/> |
|<span data-ttu-id="93c90-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="93c90-123">Can be empty</span></span>  <br/> |<span data-ttu-id="93c90-124">falso</span><span class="sxs-lookup"><span data-stu-id="93c90-124">false</span></span>  <br/> |
   

