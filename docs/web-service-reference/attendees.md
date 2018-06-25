---
title: Asistentes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 837bb372-39eb-48ae-9c09-0d2552511f93
description: El elemento de los asistentes especifica a los destinatarios de una invitación a una reunión.
ms.openlocfilehash: 22d88bb092b416c553144496e133680b53f5d30e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763577"
---
# <a name="attendees"></a><span data-ttu-id="dd343-103">Asistentes</span><span class="sxs-lookup"><span data-stu-id="dd343-103">Attendees</span></span>

<span data-ttu-id="dd343-104">El elemento de **los asistentes** especifica a los destinatarios de una invitación a una reunión.</span><span class="sxs-lookup"><span data-stu-id="dd343-104">The **Attendees** element specifies the recipients of an invitation to a meeting.</span></span> 
  
```XML
<Attendees>
    <EmailUser></EmailUser>
</Attendees>
```

 <span data-ttu-id="dd343-105">**ArrayOfEmailUsersType**</span><span class="sxs-lookup"><span data-stu-id="dd343-105">**ArrayOfEmailUsersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dd343-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dd343-106">Attributes and elements</span></span>

<span data-ttu-id="dd343-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dd343-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dd343-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="dd343-108">Attributes</span></span>

<span data-ttu-id="dd343-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dd343-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dd343-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dd343-110">Child elements</span></span>

|<span data-ttu-id="dd343-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd343-111">**Element**</span></span>|<span data-ttu-id="dd343-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dd343-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd343-113">EmailUser</span><span class="sxs-lookup"><span data-stu-id="dd343-113">EmailUser</span></span>](emailuser.md) <br/> |<span data-ttu-id="dd343-114">Especifica un destinatario de correo electrónico o un contacto de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dd343-114">Specifies an email recipient or Active Directory contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dd343-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dd343-115">Parent elements</span></span>

|<span data-ttu-id="dd343-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="dd343-116">**Element**</span></span>|<span data-ttu-id="dd343-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dd343-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd343-118">MeetingSuggestion</span><span class="sxs-lookup"><span data-stu-id="dd343-118">MeetingSuggestion</span></span>](meetingsuggestion.md) <br/> |<span data-ttu-id="dd343-119">Especifica una reunión propuesta.</span><span class="sxs-lookup"><span data-stu-id="dd343-119">Specifies a proposed meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd343-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dd343-120">Remarks</span></span>

<span data-ttu-id="dd343-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dd343-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dd343-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="dd343-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dd343-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dd343-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd343-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dd343-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dd343-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dd343-125">Schema Name</span></span>  <br/> |<span data-ttu-id="dd343-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="dd343-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="dd343-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dd343-127">Validation File</span></span>  <br/> |<span data-ttu-id="dd343-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dd343-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="dd343-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dd343-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="dd343-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd343-130">See also</span></span>

- [<span data-ttu-id="dd343-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="dd343-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

