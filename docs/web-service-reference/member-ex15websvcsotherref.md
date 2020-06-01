---
title: Member
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Member
api_type:
- schema
ms.assetid: af9c5ff8-02a4-41fc-876d-14ac05f1ee77
description: El elemento Member representa a un miembro de una lista de distribución.
ms.openlocfilehash: e84223b7c41846ca2f174293bff46a8825777a0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457308"
---
# <a name="member"></a><span data-ttu-id="100be-103">Member</span><span class="sxs-lookup"><span data-stu-id="100be-103">Member</span></span>

<span data-ttu-id="100be-104">El elemento **member** representa a un miembro de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="100be-104">The **Member** element represents a member of a distribution list.</span></span> 
  
```xml
<Member Key="">
   <Mailbox/>
   <Status/>
</Member>
```

<span data-ttu-id="100be-105">**MemberType**</span><span class="sxs-lookup"><span data-stu-id="100be-105">**MemberType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="100be-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="100be-106">Attributes and elements</span></span>

<span data-ttu-id="100be-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="100be-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="100be-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="100be-108">Attributes</span></span>

|<span data-ttu-id="100be-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="100be-109">**Attribute**</span></span>|<span data-ttu-id="100be-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="100be-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="100be-111">Key </span><span class="sxs-lookup"><span data-stu-id="100be-111">Key</span></span>  <br/> |<span data-ttu-id="100be-112">Proporciona un identificador único para el miembro de la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="100be-112">Provides a unique identifier for the distribution list member.</span></span> <span data-ttu-id="100be-113">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="100be-113">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="100be-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="100be-114">Child elements</span></span>

|<span data-ttu-id="100be-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="100be-115">**Element**</span></span>|<span data-ttu-id="100be-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="100be-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="100be-117">Buzón</span><span class="sxs-lookup"><span data-stu-id="100be-117">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="100be-118">Representa la dirección de correo electrónico del miembro de la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="100be-118">Represents the e-mail address of the distribution list member.</span></span> <span data-ttu-id="100be-119">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="100be-119">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="100be-120">Estado (MemberStatusType)</span><span class="sxs-lookup"><span data-stu-id="100be-120">Status (MemberStatusType)</span></span>](status-memberstatustype.md) <br/> |<span data-ttu-id="100be-121">Proporciona información sobre el estado de un miembro de la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="100be-121">Provides information about the status of a distribution list member.</span></span> <span data-ttu-id="100be-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="100be-122">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="100be-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="100be-123">Parent elements</span></span>

|<span data-ttu-id="100be-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="100be-124">**Element**</span></span>|<span data-ttu-id="100be-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="100be-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="100be-126">Miembros (MemberListType)</span><span class="sxs-lookup"><span data-stu-id="100be-126">Members (MemberListType)</span></span>](members-memberlisttype.md) <br/> |<span data-ttu-id="100be-127">Contiene una lista de miembros de la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="100be-127">Contains a list of distribution list members.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="100be-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="100be-128">Remarks</span></span>

<span data-ttu-id="100be-129">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="100be-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="100be-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="100be-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="100be-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="100be-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="100be-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="100be-132">Schema Name</span></span>  <br/> |<span data-ttu-id="100be-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="100be-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="100be-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="100be-134">Validation File</span></span>  <br/> |<span data-ttu-id="100be-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="100be-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="100be-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="100be-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="100be-137">Falso</span><span class="sxs-lookup"><span data-stu-id="100be-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="100be-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="100be-138">See also</span></span>

- [<span data-ttu-id="100be-139">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="100be-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

