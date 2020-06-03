---
title: MailboxHoldResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da03b877-37c6-4ecb-8549-c639f140302e
description: El elemento MailboxHoldResult contiene el resultado de la solicitud GetHoldOnMailboxes.
ms.openlocfilehash: 3895c1351587db45881c661809a19dad1929b4a9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466398"
---
# <a name="mailboxholdresult"></a><span data-ttu-id="06b70-103">MailboxHoldResult</span><span class="sxs-lookup"><span data-stu-id="06b70-103">MailboxHoldResult</span></span>

<span data-ttu-id="06b70-104">El elemento **MailboxHoldResult** contiene el resultado de la solicitud **GetHoldOnMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="06b70-104">The **MailboxHoldResult** element contains the result of the **GetHoldOnMailboxes** request.</span></span> 
  
```XML
<MailboxHoldResult>
   <HoldId/>
   <Query/>
   <MailboxHoldStatuses/>
</MailboxHoldResult>
```

<span data-ttu-id="06b70-105">**MailboxHoldResultType**</span><span class="sxs-lookup"><span data-stu-id="06b70-105">**MailboxHoldResultType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="06b70-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="06b70-106">Attributes and elements</span></span>

<span data-ttu-id="06b70-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="06b70-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="06b70-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="06b70-108">Attributes</span></span>

<span data-ttu-id="06b70-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="06b70-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="06b70-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="06b70-110">Child elements</span></span>

<span data-ttu-id="06b70-111">[HoldId](holdid.md)  |  [Consulta](query.md)  |  [MailboxHoldStatuses](mailboxholdstatuses.md)</span><span class="sxs-lookup"><span data-stu-id="06b70-111">[HoldId](holdid.md) | [Query](query.md) | [MailboxHoldStatuses](mailboxholdstatuses.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="06b70-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="06b70-112">Parent elements</span></span>

<span data-ttu-id="06b70-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="06b70-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="06b70-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="06b70-114">Remarks</span></span>

<span data-ttu-id="06b70-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="06b70-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="06b70-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="06b70-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="06b70-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="06b70-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06b70-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="06b70-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="06b70-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="06b70-119">Schema name</span></span>  <br/> |<span data-ttu-id="06b70-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="06b70-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="06b70-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="06b70-121">Validation file</span></span>  <br/> |<span data-ttu-id="06b70-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="06b70-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="06b70-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="06b70-123">Can be empty</span></span>  <br/> ||
   

