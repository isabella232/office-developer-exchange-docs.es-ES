---
title: Tipo (ElcFolderType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6faad98f-1a92-4373-bde5-dd12af61765f
description: El elemento de tipo especifica el tipo de carpeta que se utiliza en una directiva de retención.
ms.openlocfilehash: f679a9237a577d26d4b28e1b25f3e135f7193903
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840732"
---
# <a name="type-elcfoldertype"></a><span data-ttu-id="d5dea-103">Tipo (ElcFolderType)</span><span class="sxs-lookup"><span data-stu-id="d5dea-103">Type (ElcFolderType)</span></span>

<span data-ttu-id="d5dea-104">El elemento de **tipo** especifica el tipo de carpeta que se utiliza en una directiva de retención.</span><span class="sxs-lookup"><span data-stu-id="d5dea-104">The **Type** element specifies the type of folder used in a retention policy.</span></span> 
  
```XML
<Type> Calendar | Contacts | DeletedItems | Drafts | Inbox | JunkEmail | Journal | Notes | Outbox | SentItems | Tasks | All | ManagedCustomFolder | RssSubscriptions | SyncIssues | ConversationHistory | Personal | RecoverableItems | NonIpmRoot <Type>
```

 <span data-ttu-id="d5dea-105">**ElcFolderType**</span><span class="sxs-lookup"><span data-stu-id="d5dea-105">**ElcFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5dea-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d5dea-106">Attributes and elements</span></span>

<span data-ttu-id="d5dea-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d5dea-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5dea-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d5dea-108">Attributes</span></span>

<span data-ttu-id="d5dea-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d5dea-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5dea-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d5dea-110">Child elements</span></span>

<span data-ttu-id="d5dea-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d5dea-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d5dea-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d5dea-112">Parent elements</span></span>

[<span data-ttu-id="d5dea-113">RetentionPolicyTag</span><span class="sxs-lookup"><span data-stu-id="d5dea-113">RetentionPolicyTag</span></span>](retentionpolicytag.md)
  
## <a name="text-value"></a><span data-ttu-id="d5dea-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d5dea-114">Text value</span></span>

<span data-ttu-id="d5dea-115">El valor de texto del **tipo de** elemento es el tipo de carpeta utilizado en una directiva de retención.</span><span class="sxs-lookup"><span data-stu-id="d5dea-115">The text value of the **Type** element is the folder type used in a retention policy.</span></span> <span data-ttu-id="d5dea-116">El valor de texto puede ser uno de los siguientes valores que representan un tipo de carpeta predeterminado: calendario, contactos, DeletedItems, borradores, Bandeja de entrada, JunkEmail, diario, notas, Bandeja de salida, elementos enviados y tareas, All, ManagedCustomFolder, RssSubscriptions, SyncIssues, ConversationHistory, Personal, RecoverableItems o NonIpmRoot</span><span class="sxs-lookup"><span data-stu-id="d5dea-116">The text value can be one of the following values that represent a default folder type: Calendar, Contacts, DeletedItems, Drafts, Inbox, JunkEmail, Journal, Notes, Outbox, SentItems, Tasks, All, ManagedCustomFolder, RssSubscriptions, SyncIssues, ConversationHistory, Personal, RecoverableItems, or NonIpmRoot</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d5dea-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d5dea-117">Remarks</span></span>

<span data-ttu-id="d5dea-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d5dea-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d5dea-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="d5dea-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d5dea-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d5dea-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5dea-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d5dea-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d5dea-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d5dea-122">Schema name</span></span>  <br/> |<span data-ttu-id="d5dea-123">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d5dea-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="d5dea-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d5dea-124">Validation file</span></span>  <br/> |<span data-ttu-id="d5dea-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d5dea-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d5dea-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d5dea-126">Can be empty</span></span>  <br/> |<span data-ttu-id="d5dea-127">falso</span><span class="sxs-lookup"><span data-stu-id="d5dea-127">false</span></span>  <br/> |
   

