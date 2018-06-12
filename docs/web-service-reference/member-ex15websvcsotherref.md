---
title: Miembro	
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
description: El elemento de miembro representa a un miembro de una lista de distribución.
ms.openlocfilehash: c38e2ed24e78b5199d4d65cce27a00a8e6704037
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836434"
---
# <a name="member"></a><span data-ttu-id="88dfd-103">Miembro	</span><span class="sxs-lookup"><span data-stu-id="88dfd-103">Member</span></span>

<span data-ttu-id="88dfd-104">El elemento de **miembro** representa a un miembro de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="88dfd-104">The **Member** element represents a member of a distribution list.</span></span> 
  
```xml
<Member Key="">
   <Mailbox/>
   <Status/>
</Member>
```

<span data-ttu-id="88dfd-105">**MemberType**</span><span class="sxs-lookup"><span data-stu-id="88dfd-105">**MemberType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="88dfd-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="88dfd-106">Attributes and elements</span></span>

<span data-ttu-id="88dfd-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="88dfd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88dfd-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="88dfd-108">Attributes</span></span>

|<span data-ttu-id="88dfd-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="88dfd-109">**Attribute**</span></span>|<span data-ttu-id="88dfd-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="88dfd-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="88dfd-111">Clave</span><span class="sxs-lookup"><span data-stu-id="88dfd-111">Key</span></span>  <br/> |<span data-ttu-id="88dfd-112">Proporciona un identificador único para el miembro de la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="88dfd-112">Provides a unique identifier for the distribution list member.</span></span> <span data-ttu-id="88dfd-113">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="88dfd-113">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="88dfd-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="88dfd-114">Child elements</span></span>

|<span data-ttu-id="88dfd-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="88dfd-115">**Element**</span></span>|<span data-ttu-id="88dfd-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="88dfd-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88dfd-117">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="88dfd-117">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="88dfd-118">Representa la dirección de correo electrónico del miembro de la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="88dfd-118">Represents the e-mail address of the distribution list member.</span></span> <span data-ttu-id="88dfd-119">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="88dfd-119">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="88dfd-120">Estado (MemberStatusType)</span><span class="sxs-lookup"><span data-stu-id="88dfd-120">Status (MemberStatusType)</span></span>](status-memberstatustype.md) <br/> |<span data-ttu-id="88dfd-121">Proporciona información sobre el estado de un miembro de la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="88dfd-121">Provides information about the status of a distribution list member.</span></span> <span data-ttu-id="88dfd-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="88dfd-122">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="88dfd-123">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="88dfd-123">Parent elements</span></span>

|<span data-ttu-id="88dfd-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="88dfd-124">**Element**</span></span>|<span data-ttu-id="88dfd-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="88dfd-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88dfd-126">Miembros (MemberListType)</span><span class="sxs-lookup"><span data-stu-id="88dfd-126">Members (MemberListType)</span></span>](members-memberlisttype.md) <br/> |<span data-ttu-id="88dfd-127">Contiene una lista de miembros de la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="88dfd-127">Contains a list of distribution list members.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88dfd-128">Notas</span><span class="sxs-lookup"><span data-stu-id="88dfd-128">Remarks</span></span>

<span data-ttu-id="88dfd-129">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="88dfd-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="88dfd-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="88dfd-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88dfd-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="88dfd-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="88dfd-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="88dfd-132">Schema Name</span></span>  <br/> |<span data-ttu-id="88dfd-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="88dfd-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="88dfd-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="88dfd-134">Validation File</span></span>  <br/> |<span data-ttu-id="88dfd-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="88dfd-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="88dfd-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="88dfd-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="88dfd-137">False</span><span class="sxs-lookup"><span data-stu-id="88dfd-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88dfd-138">Ver también</span><span class="sxs-lookup"><span data-stu-id="88dfd-138">See also</span></span>

- [<span data-ttu-id="88dfd-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="88dfd-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

