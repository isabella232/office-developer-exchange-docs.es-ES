---
title: Acciones (RuleActionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2afba70c-65f7-458c-a4e6-a2cd9bccc0f9
description: El elemento de acciones contiene una lista de acciones asociadas con las reglas de bandeja de entrada.
ms.openlocfilehash: 8ed8095ca8b41e037c2c0dad319c9c4ab99ed2bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763477"
---
# <a name="actions-ruleactionstype"></a><span data-ttu-id="eda8f-103">Acciones (RuleActionsType)</span><span class="sxs-lookup"><span data-stu-id="eda8f-103">Actions (RuleActionsType)</span></span>

<span data-ttu-id="eda8f-104">El elemento de **acciones** contiene una lista de acciones asociadas con las reglas de bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="eda8f-104">The **Actions** element contains a list of actions associated with Inbox rules.</span></span> 
  
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

 <span data-ttu-id="eda8f-105">**RuleActionsType**</span><span class="sxs-lookup"><span data-stu-id="eda8f-105">**RuleActionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eda8f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="eda8f-106">Attributes and elements</span></span>

<span data-ttu-id="eda8f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="eda8f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eda8f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="eda8f-108">Attributes</span></span>

<span data-ttu-id="eda8f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eda8f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eda8f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eda8f-110">Child elements</span></span>

<span data-ttu-id="eda8f-111">[AssignCategories](assigncategories.md) | [CopyToFolder](copytofolder.md) | [Eliminar](delete.md) | [ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md) | [ForwardToRecipients](forwardtorecipients.md) | [MarkImportance](markimportance.md) | [MarkAsRead ](markasread.md)  |  [MoveToFolder](movetofolder.md) | [PermanentDelete](permanentdelete.md) | [RedirectToRecipients](redirecttorecipients.md) | [SendSMSAlertToRecipients](sendsmsalerttorecipients.md) | [ServerReplyWithMessage](serverreplywithmessage.md)  |  [ StopProcessingRules](stopprocessingrules.md)</span><span class="sxs-lookup"><span data-stu-id="eda8f-111">[AssignCategories](assigncategories.md) | [CopyToFolder](copytofolder.md) | [Delete](delete.md) | [ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md) | [ForwardToRecipients](forwardtorecipients.md) | [MarkImportance](markimportance.md) | [MarkAsRead](markasread.md) | [MoveToFolder](movetofolder.md) | [PermanentDelete](permanentdelete.md) | [RedirectToRecipients](redirecttorecipients.md) | [SendSMSAlertToRecipients](sendsmsalerttorecipients.md) | [ServerReplyWithMessage](serverreplywithmessage.md) | [StopProcessingRules](stopprocessingrules.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eda8f-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="eda8f-112">Parent elements</span></span>

[<span data-ttu-id="eda8f-113">Regla (RuleType)</span><span class="sxs-lookup"><span data-stu-id="eda8f-113">Rule (RuleType)</span></span>](rule-ruletype.md)
  
## <a name="remarks"></a><span data-ttu-id="eda8f-114">Notas</span><span class="sxs-lookup"><span data-stu-id="eda8f-114">Remarks</span></span>

<span data-ttu-id="eda8f-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="eda8f-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="eda8f-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="eda8f-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eda8f-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="eda8f-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eda8f-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eda8f-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="eda8f-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="eda8f-119">Schema name</span></span>  <br/> |<span data-ttu-id="eda8f-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="eda8f-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="eda8f-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="eda8f-121">Validation file</span></span>  <br/> |<span data-ttu-id="eda8f-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="eda8f-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="eda8f-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="eda8f-123">Can be empty</span></span>  <br/> |<span data-ttu-id="eda8f-124">falso</span><span class="sxs-lookup"><span data-stu-id="eda8f-124">false</span></span>  <br/> |
   

