---
title: Usuarios asignados
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20ef18c2-daa0-4f65-a515-e84e9993a77f
description: El elemento Assignees especifica las personas a quienes se asigna una tarea.
ms.openlocfilehash: 5fc301cd77268213e95fd33a2a2f36dbe218b512
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763559"
---
# <a name="assignees"></a><span data-ttu-id="e7e3d-103">Usuarios asignados</span><span class="sxs-lookup"><span data-stu-id="e7e3d-103">Assignees</span></span>

<span data-ttu-id="e7e3d-104">El elemento **Assignees** especifica las personas a quienes se asigna una tarea.</span><span class="sxs-lookup"><span data-stu-id="e7e3d-104">The **Assignees** element specifies the people to whom a task is assigned.</span></span> 
  
```XML
<Assignees>
    <Name></Name>
    <UserID></UserID>
</Assignees>
```

 <span data-ttu-id="e7e3d-105">**EmailUserType**</span><span class="sxs-lookup"><span data-stu-id="e7e3d-105">**EmailUserType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e7e3d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e7e3d-106">Attributes and elements</span></span>

<span data-ttu-id="e7e3d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e7e3d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e7e3d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e7e3d-108">Attributes</span></span>

<span data-ttu-id="e7e3d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e7e3d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e7e3d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e7e3d-110">Child elements</span></span>

|<span data-ttu-id="e7e3d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e7e3d-111">**Element**</span></span>|<span data-ttu-id="e7e3d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e7e3d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7e3d-113">Nombre (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="e7e3d-113">Name (EmailAddress)</span></span>](name-emailaddress.md) <br/> |<span data-ttu-id="e7e3d-114">Representa el nombre para mostrar del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e7e3d-114">Represents the display name of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="e7e3d-115">UserId (cadena)</span><span class="sxs-lookup"><span data-stu-id="e7e3d-115">UserId (string)</span></span>](userid-string.md) <br/> |<span data-ttu-id="e7e3d-116">Especifica el identificador de usuario de un usuario de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="e7e3d-116">Specifies the user identifier of an email user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e7e3d-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e7e3d-117">Parent elements</span></span>

|<span data-ttu-id="e7e3d-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="e7e3d-118">**Element**</span></span>|<span data-ttu-id="e7e3d-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e7e3d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7e3d-120">TaskSuggestion</span><span class="sxs-lookup"><span data-stu-id="e7e3d-120">TaskSuggestion</span></span>](tasksuggestion.md) <br/> |<span data-ttu-id="e7e3d-121">Especifica una tarea propuesta.</span><span class="sxs-lookup"><span data-stu-id="e7e3d-121">Specifies a proposed task.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7e3d-122">Notas</span><span class="sxs-lookup"><span data-stu-id="e7e3d-122">Remarks</span></span>

<span data-ttu-id="e7e3d-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e7e3d-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e7e3d-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e7e3d-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e7e3d-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e7e3d-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7e3d-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e7e3d-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e7e3d-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e7e3d-127">Schema Name</span></span>  <br/> |<span data-ttu-id="e7e3d-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="e7e3d-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="e7e3d-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e7e3d-129">Validation File</span></span>  <br/> |<span data-ttu-id="e7e3d-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e7e3d-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="e7e3d-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e7e3d-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e7e3d-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="e7e3d-132">See also</span></span>

- [<span data-ttu-id="e7e3d-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e7e3d-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

