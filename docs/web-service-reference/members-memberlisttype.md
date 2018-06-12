---
title: Miembros (MemberListType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Members
api_type:
- schema
ms.assetid: cbd38049-2ef7-40bf-9bec-0469af0f58ec
description: El elemento (miembros) proporciona la lista de miembros para una lista de distribución.
ms.openlocfilehash: 8cf9ed7a64a908614ce7be30a9bef631739fcebf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836439"
---
# <a name="members-memberlisttype"></a><span data-ttu-id="b98fc-103">Miembros (MemberListType)</span><span class="sxs-lookup"><span data-stu-id="b98fc-103">Members (MemberListType)</span></span>

<span data-ttu-id="b98fc-104">El elemento **(miembros)** proporciona la lista de miembros para una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="b98fc-104">The **Members** element provides the list of members for a distribution list.</span></span> 
  
```xml
<Members>
   <Member/>
</Members>
```

<span data-ttu-id="b98fc-105">**MemberListType**</span><span class="sxs-lookup"><span data-stu-id="b98fc-105">**MemberListType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b98fc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b98fc-106">Attributes and elements</span></span>

<span data-ttu-id="b98fc-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b98fc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b98fc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b98fc-108">Attributes</span></span>

<span data-ttu-id="b98fc-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b98fc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b98fc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b98fc-110">Child elements</span></span>

|<span data-ttu-id="b98fc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b98fc-111">**Element**</span></span>|<span data-ttu-id="b98fc-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b98fc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b98fc-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="b98fc-113">Member</span></span>](member-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b98fc-114">Proporciona un identificador para una dirección de correo electrónico completa resuelta y el estado de esa dirección en el servidor.</span><span class="sxs-lookup"><span data-stu-id="b98fc-114">Provides an identifier for a fully resolved e-mail address, and the status of that address on the server.</span></span> <span data-ttu-id="b98fc-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="b98fc-115">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b98fc-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b98fc-116">Parent elements</span></span>

|<span data-ttu-id="b98fc-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="b98fc-117">**Element**</span></span>|<span data-ttu-id="b98fc-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b98fc-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b98fc-119">DistributionList</span><span class="sxs-lookup"><span data-stu-id="b98fc-119">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="b98fc-120">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="b98fc-120">Represents a distribution list.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b98fc-121">Notas</span><span class="sxs-lookup"><span data-stu-id="b98fc-121">Remarks</span></span>

<span data-ttu-id="b98fc-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b98fc-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b98fc-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b98fc-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b98fc-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b98fc-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b98fc-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b98fc-125">Schema Name</span></span>  <br/> |<span data-ttu-id="b98fc-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b98fc-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="b98fc-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b98fc-127">Validation File</span></span>  <br/> |<span data-ttu-id="b98fc-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b98fc-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b98fc-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b98fc-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="b98fc-130">False</span><span class="sxs-lookup"><span data-stu-id="b98fc-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b98fc-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="b98fc-131">See also</span></span>

- [<span data-ttu-id="b98fc-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b98fc-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

