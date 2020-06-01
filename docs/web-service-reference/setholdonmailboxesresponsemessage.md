---
title: SetHoldOnMailboxesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61de0f3-24e0-434a-946a-c53d393b7d04
description: El elemento SetHoldOnMailboxesResponseMessage especifica el mensaje de respuesta para una solicitud de SetHoldOnMailboxes.
ms.openlocfilehash: a6af4181218391bc9d3c177467295d771cce4c89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456412"
---
# <a name="setholdonmailboxesresponsemessage"></a><span data-ttu-id="dc94c-103">SetHoldOnMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="dc94c-103">SetHoldOnMailboxesResponseMessage</span></span>

<span data-ttu-id="dc94c-104">El elemento **SetHoldOnMailboxesResponseMessage** especifica el mensaje de respuesta para una solicitud de **SetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="dc94c-104">The **SetHoldOnMailboxesResponseMessage** element specifies the response message for a **SetHoldOnMailboxes** request.</span></span> 
  
```XML
<SetHoldOnMailboxesResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MailboxHoldResult/>
</SetHoldOnMailboxesResponseMessage>
```

 <span data-ttu-id="dc94c-105">**SetHoldOnMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="dc94c-105">**SetHoldOnMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc94c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dc94c-106">Attributes and elements</span></span>

<span data-ttu-id="dc94c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dc94c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc94c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="dc94c-108">Attributes</span></span>

<span data-ttu-id="dc94c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="dc94c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc94c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dc94c-110">Child elements</span></span>

<span data-ttu-id="dc94c-111">[MessageText](messagetext.md)  |  [ResponseCode](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [MessageXml](messagexml.md)  |  [MailboxHoldResult](mailboxholdresult.md)</span><span class="sxs-lookup"><span data-stu-id="dc94c-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [MailboxHoldResult](mailboxholdresult.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dc94c-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dc94c-112">Parent elements</span></span>

[<span data-ttu-id="dc94c-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="dc94c-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="dc94c-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dc94c-114">Remarks</span></span>

<span data-ttu-id="dc94c-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dc94c-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dc94c-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="dc94c-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc94c-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dc94c-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc94c-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc94c-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dc94c-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dc94c-119">Schema name</span></span>  <br/> |<span data-ttu-id="dc94c-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="dc94c-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dc94c-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dc94c-121">Validation file</span></span>  <br/> |<span data-ttu-id="dc94c-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="dc94c-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dc94c-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dc94c-123">Can be empty</span></span>  <br/> ||
   

