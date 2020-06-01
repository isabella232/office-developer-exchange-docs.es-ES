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
description: El elemento Members proporciona la lista de miembros para una lista de distribución.
ms.openlocfilehash: 2cdfb81dfbc223db365d49ed44d4893339eb4653
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462433"
---
# <a name="members-memberlisttype"></a><span data-ttu-id="08305-103">Miembros (MemberListType)</span><span class="sxs-lookup"><span data-stu-id="08305-103">Members (MemberListType)</span></span>

<span data-ttu-id="08305-104">El elemento **Members** proporciona la lista de miembros para una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="08305-104">The **Members** element provides the list of members for a distribution list.</span></span> 
  
```xml
<Members>
   <Member/>
</Members>
```

<span data-ttu-id="08305-105">**MemberListType**</span><span class="sxs-lookup"><span data-stu-id="08305-105">**MemberListType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="08305-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="08305-106">Attributes and elements</span></span>

<span data-ttu-id="08305-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="08305-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="08305-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="08305-108">Attributes</span></span>

<span data-ttu-id="08305-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="08305-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="08305-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="08305-110">Child elements</span></span>

|<span data-ttu-id="08305-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="08305-111">**Element**</span></span>|<span data-ttu-id="08305-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="08305-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="08305-113">Miembro</span><span class="sxs-lookup"><span data-stu-id="08305-113">Member</span></span>](member-ex15websvcsotherref.md) <br/> |<span data-ttu-id="08305-114">Proporciona un identificador para una dirección de correo electrónico completamente resuelta y el estado de esa dirección en el servidor.</span><span class="sxs-lookup"><span data-stu-id="08305-114">Provides an identifier for a fully resolved e-mail address, and the status of that address on the server.</span></span> <span data-ttu-id="08305-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="08305-115">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="08305-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="08305-116">Parent elements</span></span>

|<span data-ttu-id="08305-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="08305-117">**Element**</span></span>|<span data-ttu-id="08305-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="08305-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="08305-119">DistributionList</span><span class="sxs-lookup"><span data-stu-id="08305-119">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="08305-120">Representa una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="08305-120">Represents a distribution list.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08305-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="08305-121">Remarks</span></span>

<span data-ttu-id="08305-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="08305-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="08305-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="08305-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08305-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="08305-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="08305-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="08305-125">Schema Name</span></span>  <br/> |<span data-ttu-id="08305-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="08305-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="08305-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="08305-127">Validation File</span></span>  <br/> |<span data-ttu-id="08305-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="08305-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="08305-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="08305-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="08305-130">Falso</span><span class="sxs-lookup"><span data-stu-id="08305-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="08305-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="08305-131">See also</span></span>

- [<span data-ttu-id="08305-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="08305-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

