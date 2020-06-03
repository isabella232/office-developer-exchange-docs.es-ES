---
title: Asigna una
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20ef18c2-daa0-4f65-a515-e84e9993a77f
description: El elemento Assignments especifica las personas a las que se asigna una tarea.
ms.openlocfilehash: 3e98273e859dbe2128b0ad3b4df42c8016fd3bc5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464717"
---
# <a name="assignees"></a><span data-ttu-id="063ae-103">Asigna una</span><span class="sxs-lookup"><span data-stu-id="063ae-103">Assignees</span></span>

<span data-ttu-id="063ae-104">El elemento **Assignments** especifica las personas a las que se asigna una tarea.</span><span class="sxs-lookup"><span data-stu-id="063ae-104">The **Assignees** element specifies the people to whom a task is assigned.</span></span> 
  
```XML
<Assignees>
    <Name></Name>
    <UserID></UserID>
</Assignees>
```

 <span data-ttu-id="063ae-105">**EmailUserType**</span><span class="sxs-lookup"><span data-stu-id="063ae-105">**EmailUserType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="063ae-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="063ae-106">Attributes and elements</span></span>

<span data-ttu-id="063ae-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="063ae-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="063ae-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="063ae-108">Attributes</span></span>

<span data-ttu-id="063ae-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="063ae-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="063ae-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="063ae-110">Child elements</span></span>

|<span data-ttu-id="063ae-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="063ae-111">**Element**</span></span>|<span data-ttu-id="063ae-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="063ae-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="063ae-113">Nombre (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="063ae-113">Name (EmailAddress)</span></span>](name-emailaddress.md) <br/> |<span data-ttu-id="063ae-114">Representa el nombre para mostrar del usuario del buzón.</span><span class="sxs-lookup"><span data-stu-id="063ae-114">Represents the display name of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="063ae-115">UserId (cadena)</span><span class="sxs-lookup"><span data-stu-id="063ae-115">UserId (string)</span></span>](userid-string.md) <br/> |<span data-ttu-id="063ae-116">Especifica el identificador de usuario de un usuario de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="063ae-116">Specifies the user identifier of an email user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="063ae-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="063ae-117">Parent elements</span></span>

|<span data-ttu-id="063ae-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="063ae-118">**Element**</span></span>|<span data-ttu-id="063ae-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="063ae-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="063ae-120">TaskSuggestion</span><span class="sxs-lookup"><span data-stu-id="063ae-120">TaskSuggestion</span></span>](tasksuggestion.md) <br/> |<span data-ttu-id="063ae-121">Especifica una tarea propuesta.</span><span class="sxs-lookup"><span data-stu-id="063ae-121">Specifies a proposed task.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="063ae-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="063ae-122">Remarks</span></span>

<span data-ttu-id="063ae-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="063ae-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="063ae-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="063ae-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="063ae-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="063ae-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="063ae-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="063ae-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="063ae-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="063ae-127">Schema Name</span></span>  <br/> |<span data-ttu-id="063ae-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="063ae-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="063ae-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="063ae-129">Validation File</span></span>  <br/> |<span data-ttu-id="063ae-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="063ae-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="063ae-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="063ae-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="063ae-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="063ae-132">See also</span></span>

- [<span data-ttu-id="063ae-133">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="063ae-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

