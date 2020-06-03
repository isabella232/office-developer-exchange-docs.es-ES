---
title: Acciones (RuleActionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2afba70c-65f7-458c-a4e6-a2cd9bccc0f9
description: El elemento Actions contiene una lista de acciones asociadas con las reglas de la bandeja de entrada.
ms.openlocfilehash: fbef3b69b1688d7c612af018d6a19f9ec1728066
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529682"
---
# <a name="actions-ruleactionstype"></a><span data-ttu-id="57045-103">Acciones (RuleActionsType)</span><span class="sxs-lookup"><span data-stu-id="57045-103">Actions (RuleActionsType)</span></span>

<span data-ttu-id="57045-104">El elemento **Actions** contiene una lista de acciones asociadas con las reglas de la bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="57045-104">The **Actions** element contains a list of actions associated with Inbox rules.</span></span> 
  
```XML
<Actions>
   <AssignCategories/>
   <CopyToFolder/>
   <Delete/>
   <ForwardAsAttachmentToRecipients/>
   <ForwardToRecipients/>
   <MarkImportance/>
   <MarkAsRead/>
   <MoveToFolder/>
   <PermanentDelete/>
   <RedirectToRecipients/>
   <SendSMSAlertToRecipients/>
   <ServerReplyWithMessage/>
   <StopProcessingRules/>
</Actions>
```

 <span data-ttu-id="57045-105">**RuleActionsType**</span><span class="sxs-lookup"><span data-stu-id="57045-105">**RuleActionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="57045-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="57045-106">Attributes and elements</span></span>

<span data-ttu-id="57045-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="57045-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="57045-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="57045-108">Attributes</span></span>

<span data-ttu-id="57045-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="57045-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="57045-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="57045-110">Child elements</span></span>

<span data-ttu-id="57045-111">[AssignCategories](assigncategories.md)  |  [CopyToFolder](copytofolder.md)  |  [Eliminar](delete.md)  |  [ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md)  |  [ForwardToRecipients](forwardtorecipients.md)  |  [MarkImportance](markimportance.md)  |  [MarkAsRead](markasread.md)  |  [MoveToFolder](movetofolder.md)  |  [PermanentDelete](permanentdelete.md)  |  [RedirectToRecipients](redirecttorecipients.md)  |  [SendSMSAlertToRecipients](sendsmsalerttorecipients.md)  |  [ServerReplyWithMessage](serverreplywithmessage.md)  |  [StopProcessingRules](stopprocessingrules.md)</span><span class="sxs-lookup"><span data-stu-id="57045-111">[AssignCategories](assigncategories.md) | [CopyToFolder](copytofolder.md) | [Delete](delete.md) | [ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md) | [ForwardToRecipients](forwardtorecipients.md) | [MarkImportance](markimportance.md) | [MarkAsRead](markasread.md) | [MoveToFolder](movetofolder.md) | [PermanentDelete](permanentdelete.md) | [RedirectToRecipients](redirecttorecipients.md) | [SendSMSAlertToRecipients](sendsmsalerttorecipients.md) | [ServerReplyWithMessage](serverreplywithmessage.md) | [StopProcessingRules](stopprocessingrules.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="57045-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="57045-112">Parent elements</span></span>

[<span data-ttu-id="57045-113">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="57045-113">Rule (RuleType)</span></span>](rule-ruletype.md)
  
## <a name="remarks"></a><span data-ttu-id="57045-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="57045-114">Remarks</span></span>

<span data-ttu-id="57045-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="57045-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="57045-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="57045-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="57045-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="57045-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="57045-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="57045-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="57045-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="57045-119">Schema name</span></span>  <br/> |<span data-ttu-id="57045-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="57045-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="57045-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="57045-121">Validation file</span></span>  <br/> |<span data-ttu-id="57045-122">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="57045-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="57045-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="57045-123">Can be empty</span></span>  <br/> |<span data-ttu-id="57045-124">false</span><span class="sxs-lookup"><span data-stu-id="57045-124">false</span></span>  <br/> |
   

