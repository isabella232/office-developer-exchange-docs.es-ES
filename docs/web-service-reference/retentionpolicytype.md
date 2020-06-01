---
title: RetentionPolicyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: abce5b3e-971d-42fc-aeea-caa7202214de
description: El elemento RetentionPolicyType especifica el tipo de directiva de retención que se aplica a los elementos de una conversación.
ms.openlocfilehash: 3900718f10e1e11d5864ebf7e64a3e1e22aa45c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462874"
---
# <a name="retentionpolicytype"></a><span data-ttu-id="63640-103">RetentionPolicyType</span><span class="sxs-lookup"><span data-stu-id="63640-103">RetentionPolicyType</span></span>

<span data-ttu-id="63640-104">El elemento **RetentionPolicyType** especifica el tipo de directiva de retención que se aplica a los elementos de una conversación.</span><span class="sxs-lookup"><span data-stu-id="63640-104">The **RetentionPolicyType** element specifies the retention policy type applied to items in a conversation.</span></span> 
  
```XML
<RetentionPolicyType> Delete | Archive </RetentionPolicyType>
```

 <span data-ttu-id="63640-105">**RetentionType**</span><span class="sxs-lookup"><span data-stu-id="63640-105">**RetentionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="63640-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="63640-106">Attributes and elements</span></span>

<span data-ttu-id="63640-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="63640-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="63640-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="63640-108">Attributes</span></span>

<span data-ttu-id="63640-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="63640-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="63640-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="63640-110">Child elements</span></span>

<span data-ttu-id="63640-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="63640-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="63640-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="63640-112">Parent elements</span></span>

[<span data-ttu-id="63640-113">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="63640-113">ConversationAction</span></span>](conversationaction.md)
  
## <a name="text-value"></a><span data-ttu-id="63640-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="63640-114">Text value</span></span>

<span data-ttu-id="63640-115">El valor de texto del elemento **RetentionPolicyType** es el tipo de retención que se aplica a los elementos de una conversación.</span><span class="sxs-lookup"><span data-stu-id="63640-115">The text value of the **RetentionPolicyType** element is the retention type applied to items in a conversation.</span></span> <span data-ttu-id="63640-116">El valor de texto de **Delete** indica que los elementos de la conversación se eliminan cuando expira la suspensión de retención.</span><span class="sxs-lookup"><span data-stu-id="63640-116">The text value of **Delete** indicates that the items in the conversation are deleted when the retention hold expires.</span></span> <span data-ttu-id="63640-117">El valor de texto de **archivo** indica que los elementos de la conversación se mueven al buzón de archivo cuando expira la suspensión de retención.</span><span class="sxs-lookup"><span data-stu-id="63640-117">The text value of **Archive** indicates that the items in the conversation are moved to the archive mailbox when the retention hold expires.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="63640-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63640-118">Remarks</span></span>

<span data-ttu-id="63640-119">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="63640-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="63640-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="63640-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="63640-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="63640-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63640-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="63640-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="63640-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="63640-123">Schema name</span></span>  <br/> |<span data-ttu-id="63640-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="63640-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="63640-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="63640-125">Validation file</span></span>  <br/> |<span data-ttu-id="63640-126">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="63640-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="63640-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="63640-127">Can be empty</span></span>  <br/> ||
   

