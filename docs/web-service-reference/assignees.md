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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763559"
---
# <a name="assignees"></a><span data-ttu-id="f855f-103">Usuarios asignados</span><span class="sxs-lookup"><span data-stu-id="f855f-103">Assignees</span></span>

<span data-ttu-id="f855f-104">El elemento **Assignees** especifica las personas a quienes se asigna una tarea.</span><span class="sxs-lookup"><span data-stu-id="f855f-104">The **Assignees** element specifies the people to whom a task is assigned.</span></span> 
  
```XML
<Assignees>
    <Name></Name>
    <UserID></UserID>
</Assignees>
```

 <span data-ttu-id="f855f-105">**EmailUserType**</span><span class="sxs-lookup"><span data-stu-id="f855f-105">**EmailUserType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f855f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f855f-106">Attributes and elements</span></span>

<span data-ttu-id="f855f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f855f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f855f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f855f-108">Attributes</span></span>

<span data-ttu-id="f855f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f855f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f855f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f855f-110">Child elements</span></span>

|<span data-ttu-id="f855f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f855f-111">**Element**</span></span>|<span data-ttu-id="f855f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f855f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f855f-113">Nombre (EmailAddress)</span><span class="sxs-lookup"><span data-stu-id="f855f-113">Name (EmailAddress)</span></span>](name-emailaddress.md) <br/> |<span data-ttu-id="f855f-114">Representa el nombre para mostrar del usuario de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="f855f-114">Represents the display name of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="f855f-115">UserId (cadena)</span><span class="sxs-lookup"><span data-stu-id="f855f-115">UserId (string)</span></span>](userid-string.md) <br/> |<span data-ttu-id="f855f-116">Especifica el identificador de usuario de un usuario de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="f855f-116">Specifies the user identifier of an email user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f855f-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f855f-117">Parent elements</span></span>

|<span data-ttu-id="f855f-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="f855f-118">**Element**</span></span>|<span data-ttu-id="f855f-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f855f-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f855f-120">TaskSuggestion</span><span class="sxs-lookup"><span data-stu-id="f855f-120">TaskSuggestion</span></span>](tasksuggestion.md) <br/> |<span data-ttu-id="f855f-121">Especifica una tarea propuesta.</span><span class="sxs-lookup"><span data-stu-id="f855f-121">Specifies a proposed task.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f855f-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f855f-122">Remarks</span></span>

<span data-ttu-id="f855f-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f855f-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f855f-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="f855f-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f855f-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f855f-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f855f-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f855f-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f855f-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f855f-127">Schema Name</span></span>  <br/> |<span data-ttu-id="f855f-128">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="f855f-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="f855f-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f855f-129">Validation File</span></span>  <br/> |<span data-ttu-id="f855f-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f855f-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f855f-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f855f-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f855f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f855f-132">See also</span></span>

- [<span data-ttu-id="f855f-133">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="f855f-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

