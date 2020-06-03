---
title: GetSearchableMailboxesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0fcc2f53-742b-46ae-bbab-c3295a3d69e7
description: El elemento GetSearchableMailboxesResponse contiene la respuesta a una solicitud GetSearchableMailboxes.
ms.openlocfilehash: 680fde9d9ad34dd0384e00da023796d004b66b1b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458267"
---
# <a name="getsearchablemailboxesresponse"></a><span data-ttu-id="19b26-103">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="19b26-103">GetSearchableMailboxesResponse</span></span>

<span data-ttu-id="19b26-104">El elemento **GetSearchableMailboxesResponse** contiene la respuesta a una solicitud **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="19b26-104">The **GetSearchableMailboxesResponse** element contains the response to a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<GetSearchableMailboxesResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <SearchableMailboxes/>
   <FailedMailboxes/>
</GetSearchableMailboxesResponse>
```

 <span data-ttu-id="19b26-105">**GetSearchableMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="19b26-105">**GetSearchableMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="19b26-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="19b26-106">Attributes and elements</span></span>

<span data-ttu-id="19b26-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="19b26-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19b26-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="19b26-108">Attributes</span></span>

<span data-ttu-id="19b26-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="19b26-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19b26-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="19b26-110">Child elements</span></span>

<span data-ttu-id="19b26-111">[MessageText](messagetext.md)  |  [ResponseCode](responsecode.md)  |  [DescriptiveLinkKey](descriptivelinkkey.md)  |  [MessageXml](messagexml.md)  |  [SearchableMailboxes](searchablemailboxes.md)  |  [FailedMailboxes](failedmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="19b26-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [SearchableMailboxes](searchablemailboxes.md) | [FailedMailboxes](failedmailboxes.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="19b26-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="19b26-112">Parent elements</span></span>

<span data-ttu-id="19b26-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="19b26-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="19b26-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="19b26-114">Remarks</span></span>

<span data-ttu-id="19b26-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="19b26-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="19b26-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="19b26-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="19b26-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="19b26-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19b26-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="19b26-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="19b26-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="19b26-119">Schema name</span></span>  <br/> |<span data-ttu-id="19b26-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="19b26-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="19b26-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="19b26-121">Validation file</span></span>  <br/> |<span data-ttu-id="19b26-122">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="19b26-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="19b26-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="19b26-123">Can be empty</span></span>  <br/> |<span data-ttu-id="19b26-124">false</span><span class="sxs-lookup"><span data-stu-id="19b26-124">false</span></span>  <br/> |
   

