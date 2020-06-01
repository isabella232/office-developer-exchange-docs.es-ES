---
title: Asistentes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 837bb372-39eb-48ae-9c09-0d2552511f93
description: El elemento attendees especifica los destinatarios de una invitación a una reunión.
ms.openlocfilehash: 3a63bdf7e49309697ac503be5f4c95eb805b9635
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460333"
---
# <a name="attendees"></a><span data-ttu-id="88cfe-103">Asistentes</span><span class="sxs-lookup"><span data-stu-id="88cfe-103">Attendees</span></span>

<span data-ttu-id="88cfe-104">El elemento **attendees** especifica los destinatarios de una invitación a una reunión.</span><span class="sxs-lookup"><span data-stu-id="88cfe-104">The **Attendees** element specifies the recipients of an invitation to a meeting.</span></span> 
  
```XML
<Attendees>
    <EmailUser></EmailUser>
</Attendees>
```

 <span data-ttu-id="88cfe-105">**ArrayOfEmailUsersType**</span><span class="sxs-lookup"><span data-stu-id="88cfe-105">**ArrayOfEmailUsersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="88cfe-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="88cfe-106">Attributes and elements</span></span>

<span data-ttu-id="88cfe-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="88cfe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88cfe-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="88cfe-108">Attributes</span></span>

<span data-ttu-id="88cfe-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="88cfe-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="88cfe-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="88cfe-110">Child elements</span></span>

|<span data-ttu-id="88cfe-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="88cfe-111">**Element**</span></span>|<span data-ttu-id="88cfe-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="88cfe-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88cfe-113">EmailUser</span><span class="sxs-lookup"><span data-stu-id="88cfe-113">EmailUser</span></span>](emailuser.md) <br/> |<span data-ttu-id="88cfe-114">Especifica un destinatario de correo electrónico o un contacto de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="88cfe-114">Specifies an email recipient or Active Directory contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="88cfe-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="88cfe-115">Parent elements</span></span>

|<span data-ttu-id="88cfe-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="88cfe-116">**Element**</span></span>|<span data-ttu-id="88cfe-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="88cfe-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88cfe-118">MeetingSuggestion</span><span class="sxs-lookup"><span data-stu-id="88cfe-118">MeetingSuggestion</span></span>](meetingsuggestion.md) <br/> |<span data-ttu-id="88cfe-119">Especifica una reunión propuesta.</span><span class="sxs-lookup"><span data-stu-id="88cfe-119">Specifies a proposed meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88cfe-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="88cfe-120">Remarks</span></span>

<span data-ttu-id="88cfe-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="88cfe-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="88cfe-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="88cfe-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="88cfe-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="88cfe-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88cfe-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="88cfe-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="88cfe-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="88cfe-125">Schema Name</span></span>  <br/> |<span data-ttu-id="88cfe-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="88cfe-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="88cfe-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="88cfe-127">Validation File</span></span>  <br/> |<span data-ttu-id="88cfe-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="88cfe-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="88cfe-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="88cfe-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="88cfe-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="88cfe-130">See also</span></span>

- [<span data-ttu-id="88cfe-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="88cfe-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

