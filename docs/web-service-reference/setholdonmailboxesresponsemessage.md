---
title: SetHoldOnMailboxesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61de0f3-24e0-434a-946a-c53d393b7d04
description: El elemento SetHoldOnMailboxesResponseMessage especifica el mensaje de respuesta de una solicitud de SetHoldOnMailboxes.
ms.openlocfilehash: b7cb890a71d27340e328e39c1c463fefa080b8cb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837420"
---
# <a name="setholdonmailboxesresponsemessage"></a><span data-ttu-id="b4112-103">SetHoldOnMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b4112-103">SetHoldOnMailboxesResponseMessage</span></span>

<span data-ttu-id="b4112-104">El elemento **SetHoldOnMailboxesResponseMessage** especifica el mensaje de respuesta de una solicitud de **SetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="b4112-104">The **SetHoldOnMailboxesResponseMessage** element specifies the response message for a **SetHoldOnMailboxes** request.</span></span> 
  
```XML
<SetHoldOnMailboxesResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MailboxHoldResult/>
</SetHoldOnMailboxesResponseMessage>
```

 <span data-ttu-id="b4112-105">**SetHoldOnMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="b4112-105">**SetHoldOnMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b4112-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b4112-106">Attributes and elements</span></span>

<span data-ttu-id="b4112-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b4112-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b4112-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b4112-108">Attributes</span></span>

<span data-ttu-id="b4112-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b4112-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b4112-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b4112-110">Child elements</span></span>

<span data-ttu-id="b4112-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [MailboxHoldResult](mailboxholdresult.md)</span><span class="sxs-lookup"><span data-stu-id="b4112-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [MailboxHoldResult](mailboxholdresult.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b4112-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b4112-112">Parent elements</span></span>

[<span data-ttu-id="b4112-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b4112-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="b4112-114">Notas</span><span class="sxs-lookup"><span data-stu-id="b4112-114">Remarks</span></span>

<span data-ttu-id="b4112-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b4112-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b4112-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b4112-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b4112-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b4112-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4112-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b4112-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b4112-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b4112-119">Schema name</span></span>  <br/> |<span data-ttu-id="b4112-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b4112-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b4112-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b4112-121">Validation file</span></span>  <br/> |<span data-ttu-id="b4112-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b4112-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b4112-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b4112-123">Can be empty</span></span>  <br/> ||
   

