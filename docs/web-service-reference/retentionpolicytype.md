---
title: RetentionPolicyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: abce5b3e-971d-42fc-aeea-caa7202214de
description: El elemento RetentionPolicyType especifica el tipo de directiva de retención aplicado a los elementos en una conversación.
ms.openlocfilehash: dacb3fa75611cbd6e6e29eab7c791dfd8964c9ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837229"
---
# <a name="retentionpolicytype"></a><span data-ttu-id="b8523-103">RetentionPolicyType</span><span class="sxs-lookup"><span data-stu-id="b8523-103">RetentionPolicyType</span></span>

<span data-ttu-id="b8523-104">El elemento **RetentionPolicyType** especifica el tipo de directiva de retención aplicado a los elementos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="b8523-104">The **RetentionPolicyType** element specifies the retention policy type applied to items in a conversation.</span></span> 
  
```XML
<RetentionPolicyType> Delete | Archive </RetentionPolicyType>
```

 <span data-ttu-id="b8523-105">**RetentionType**</span><span class="sxs-lookup"><span data-stu-id="b8523-105">**RetentionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b8523-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b8523-106">Attributes and elements</span></span>

<span data-ttu-id="b8523-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b8523-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b8523-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b8523-108">Attributes</span></span>

<span data-ttu-id="b8523-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b8523-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b8523-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b8523-110">Child elements</span></span>

<span data-ttu-id="b8523-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b8523-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b8523-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b8523-112">Parent elements</span></span>

[<span data-ttu-id="b8523-113">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="b8523-113">ConversationAction</span></span>](conversationaction.md)
  
## <a name="text-value"></a><span data-ttu-id="b8523-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b8523-114">Text value</span></span>

<span data-ttu-id="b8523-115">El valor de texto del elemento **RetentionPolicyType** es el tipo de retención aplicado a los elementos en una conversación.</span><span class="sxs-lookup"><span data-stu-id="b8523-115">The text value of the **RetentionPolicyType** element is the retention type applied to items in a conversation.</span></span> <span data-ttu-id="b8523-116">El valor de texto de **Eliminar** indica que los elementos de la conversación se eliminan cuando expire la suspensión de retención.</span><span class="sxs-lookup"><span data-stu-id="b8523-116">The text value of **Delete** indicates that the items in the conversation are deleted when the retention hold expires.</span></span> <span data-ttu-id="b8523-117">El valor de texto del **archivo** indica que los elementos de la conversación se mueven al buzón de archivo cuando expire la suspensión de retención.</span><span class="sxs-lookup"><span data-stu-id="b8523-117">The text value of **Archive** indicates that the items in the conversation are moved to the archive mailbox when the retention hold expires.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b8523-118">Notas</span><span class="sxs-lookup"><span data-stu-id="b8523-118">Remarks</span></span>

<span data-ttu-id="b8523-119">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b8523-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b8523-120">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b8523-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8523-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b8523-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8523-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b8523-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b8523-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b8523-123">Schema name</span></span>  <br/> |<span data-ttu-id="b8523-124">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b8523-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="b8523-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b8523-125">Validation file</span></span>  <br/> |<span data-ttu-id="b8523-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b8523-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b8523-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b8523-127">Can be empty</span></span>  <br/> ||
   

