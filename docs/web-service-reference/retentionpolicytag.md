---
title: RetentionPolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f46679d0-9236-41e2-8624-72300079c67c
description: El elemento RetentionPolicyTag especifica la directiva de retención para un elemento de buzón de correo.
ms.openlocfilehash: 2525f6d7a0ca583342d28dd9f4857a69b3a8c05a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837226"
---
# <a name="retentionpolicytag"></a><span data-ttu-id="83927-103">RetentionPolicyTag</span><span class="sxs-lookup"><span data-stu-id="83927-103">RetentionPolicyTag</span></span>

<span data-ttu-id="83927-104">El elemento **RetentionPolicyTag** especifica la directiva de retención para un elemento de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="83927-104">The **RetentionPolicyTag** element specifies the retention policy for a mailbox item.</span></span> 
  
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

 <span data-ttu-id="83927-105">**RetentionPolicyTagType**</span><span class="sxs-lookup"><span data-stu-id="83927-105">**RetentionPolicyTagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83927-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="83927-106">Attributes and elements</span></span>

<span data-ttu-id="83927-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="83927-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83927-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="83927-108">Attributes</span></span>

<span data-ttu-id="83927-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="83927-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83927-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="83927-110">Child elements</span></span>

<span data-ttu-id="83927-111">[DisplayName (string)](displayname-string.md) | [RetentionId](retentionid.md) | [RetentionPeriod](retentionperiod.md) | [tipo (ElcFolderType)](type-elcfoldertype.md) | [RetentionAction](retentionaction.md) | [Descripción](description.md) | [IsVisible](isvisible.md)  |  [OptedInto](optedinto.md) | [IsArchive](isarchive.md)</span><span class="sxs-lookup"><span data-stu-id="83927-111">[DisplayName (string)](displayname-string.md) | [RetentionId](retentionid.md) | [RetentionPeriod](retentionperiod.md) | [Type (ElcFolderType)](type-elcfoldertype.md) | [RetentionAction](retentionaction.md) | [Description](description.md) | [IsVisible](isvisible.md) | [OptedInto](optedinto.md) | [IsArchive](isarchive.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="83927-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="83927-112">Parent elements</span></span>

[<span data-ttu-id="83927-113">RetentionPolicyTags</span><span class="sxs-lookup"><span data-stu-id="83927-113">RetentionPolicyTags</span></span>](retentionpolicytags.md)
  
## <a name="remarks"></a><span data-ttu-id="83927-114">Notas</span><span class="sxs-lookup"><span data-stu-id="83927-114">Remarks</span></span>

<span data-ttu-id="83927-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="83927-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="83927-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="83927-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83927-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="83927-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83927-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="83927-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="83927-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="83927-119">Schema name</span></span>  <br/> |<span data-ttu-id="83927-120">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="83927-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="83927-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="83927-121">Validation file</span></span>  <br/> |<span data-ttu-id="83927-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="83927-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="83927-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="83927-123">Can be empty</span></span>  <br/> ||
   

