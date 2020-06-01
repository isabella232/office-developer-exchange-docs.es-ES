---
title: RetentionPolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f46679d0-9236-41e2-8624-72300079c67c
description: El elemento RetentionPolicyTag especifica la Directiva de retención de un elemento de buzón.
ms.openlocfilehash: 3ece841e14e6cf11ab15e4a4d8b83a778ae32e46
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465180"
---
# <a name="retentionpolicytag"></a><span data-ttu-id="7ff76-103">RetentionPolicyTag</span><span class="sxs-lookup"><span data-stu-id="7ff76-103">RetentionPolicyTag</span></span>

<span data-ttu-id="7ff76-104">El elemento **RetentionPolicyTag** especifica la Directiva de retención de un elemento de buzón.</span><span class="sxs-lookup"><span data-stu-id="7ff76-104">The **RetentionPolicyTag** element specifies the retention policy for a mailbox item.</span></span> 
  
```XML
<RetentionPolicyTag>
   <DisplayName/>
   <RetentionId/>
   <RetentionPeriod/>
   <Type/>
   <RetentionAction/>
   <Description/>
   <IsVisible/>
   <OptedInto/>
   <IsArchive/>
</RetentionPolicyTag>
```

 <span data-ttu-id="7ff76-105">**RetentionPolicyTagType**</span><span class="sxs-lookup"><span data-stu-id="7ff76-105">**RetentionPolicyTagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7ff76-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7ff76-106">Attributes and elements</span></span>

<span data-ttu-id="7ff76-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7ff76-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7ff76-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7ff76-108">Attributes</span></span>

<span data-ttu-id="7ff76-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7ff76-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7ff76-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7ff76-110">Child elements</span></span>

<span data-ttu-id="7ff76-111">[DisplayName (cadena)](displayname-string.md)  |  [RetentionId](retentionid.md)  |  [RetentionPeriod](retentionperiod.md)  |  [Tipo (ElcFolderType)](type-elcfoldertype.md)  |  [RetentionAction](retentionaction.md)  |  [Descripción](description.md)  |  [IsVisible](isvisible.md)  |  [OptedInto](optedinto.md)  |  [IsArchive](isarchive.md)</span><span class="sxs-lookup"><span data-stu-id="7ff76-111">[DisplayName (string)](displayname-string.md) | [RetentionId](retentionid.md) | [RetentionPeriod](retentionperiod.md) | [Type (ElcFolderType)](type-elcfoldertype.md) | [RetentionAction](retentionaction.md) | [Description](description.md) | [IsVisible](isvisible.md) | [OptedInto](optedinto.md) | [IsArchive](isarchive.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7ff76-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7ff76-112">Parent elements</span></span>

[<span data-ttu-id="7ff76-113">RetentionPolicyTags</span><span class="sxs-lookup"><span data-stu-id="7ff76-113">RetentionPolicyTags</span></span>](retentionpolicytags.md)
  
## <a name="remarks"></a><span data-ttu-id="7ff76-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7ff76-114">Remarks</span></span>

<span data-ttu-id="7ff76-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="7ff76-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7ff76-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="7ff76-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7ff76-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7ff76-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ff76-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="7ff76-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7ff76-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7ff76-119">Schema name</span></span>  <br/> |<span data-ttu-id="7ff76-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="7ff76-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="7ff76-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7ff76-121">Validation file</span></span>  <br/> |<span data-ttu-id="7ff76-122">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="7ff76-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7ff76-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7ff76-123">Can be empty</span></span>  <br/> ||
   

