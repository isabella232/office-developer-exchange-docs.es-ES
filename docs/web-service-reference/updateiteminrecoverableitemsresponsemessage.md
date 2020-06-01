---
title: UpdateItemInRecoverableItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96259756-322e-4c24-ac76-0cd9c32e0d6d
description: El elemento UpdateItemInRecoverableItemsResponseMessage especifica la respuesta a una solicitud UpdateItemInRecoverableItems.
ms.openlocfilehash: 021631f5c30eebbf4d7ae0aad35a85b99a23925f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466538"
---
# <a name="updateiteminrecoverableitemsresponsemessage"></a><span data-ttu-id="193d4-103">UpdateItemInRecoverableItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="193d4-103">UpdateItemInRecoverableItemsResponseMessage</span></span>

<span data-ttu-id="193d4-104">El elemento **UpdateItemInRecoverableItemsResponseMessage** especifica la respuesta a una solicitud **UpdateItemInRecoverableItems** .</span><span class="sxs-lookup"><span data-stu-id="193d4-104">The **UpdateItemInRecoverableItemsResponseMessage** element specifies the response to an **UpdateItemInRecoverableItems** request.</span></span> 
  
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

 <span data-ttu-id="193d4-105">**UpdateItemInRecoverableItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="193d4-105">**UpdateItemInRecoverableItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="193d4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="193d4-106">Attributes and elements</span></span>

<span data-ttu-id="193d4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="193d4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="193d4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="193d4-108">Attributes</span></span>

<span data-ttu-id="193d4-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="193d4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="193d4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="193d4-110">Child elements</span></span>

<span data-ttu-id="193d4-111">[MessageText](messagetext.md)  |  [ResponseCode](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [MessageXml](messagexml.md)  |  [Elementos](items.md)  |  [Datos adjuntos](attachments-ex15websvcsotherref.md)  |  [ConflictResults](conflictresults.md)</span><span class="sxs-lookup"><span data-stu-id="193d4-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [Items](items.md) | [Attachments](attachments-ex15websvcsotherref.md) | [ConflictResults](conflictresults.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="193d4-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="193d4-112">Parent elements</span></span>

<span data-ttu-id="193d4-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="193d4-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="193d4-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="193d4-114">Remarks</span></span>

<span data-ttu-id="193d4-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="193d4-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="193d4-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="193d4-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="193d4-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="193d4-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="193d4-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="193d4-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|<span data-ttu-id="193d4-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="193d4-119">Schema name</span></span>  <br/> |<span data-ttu-id="193d4-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="193d4-120">Message schema</span></span>  <br/> |
|<span data-ttu-id="193d4-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="193d4-121">Validation file</span></span>  <br/> |<span data-ttu-id="193d4-122">Mensaje. xsd</span><span class="sxs-lookup"><span data-stu-id="193d4-122">Message.xsd</span></span>  <br/> |
|<span data-ttu-id="193d4-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="193d4-123">Can be empty</span></span>  <br/> |<span data-ttu-id="193d4-124">false</span><span class="sxs-lookup"><span data-stu-id="193d4-124">false</span></span>  <br/> |
   

