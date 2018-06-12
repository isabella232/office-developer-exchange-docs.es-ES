---
title: RestrictedGroupIdentifier
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RestrictedGroupIdentifier
api_type:
- schema
ms.assetid: a3ea3c81-9f99-4836-8cb4-2384ea63f093
description: El elemento RestrictGroupIdentifier representa los atributos de un grupo restringido dentro de un símbolo (token) de usuario y el identificador del grupo de seguridad (SID).
ms.openlocfilehash: c6db8672b2afa855e83f2e9a2bf84c9ff33bdc7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837206"
---
# <a name="restrictedgroupidentifier"></a><span data-ttu-id="9d0a9-103">RestrictedGroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="9d0a9-103">RestrictedGroupIdentifier</span></span>

<span data-ttu-id="9d0a9-104">El elemento **RestrictGroupIdentifier** representa los atributos de un grupo restringido dentro de un símbolo (token) de usuario y el identificador del grupo de seguridad (SID).</span><span class="sxs-lookup"><span data-stu-id="9d0a9-104">The **RestrictGroupIdentifier** element represents the group security identifier (SID) and attributes for a restricted group within a user token.</span></span> 
  
```xml
<RestrictedGroupIdentifier Attributes="">
   <SecurityIdentifier/>
</RestrictedGroupIdentifier>
```

 <span data-ttu-id="9d0a9-105">**SidAndAttributesType**</span><span class="sxs-lookup"><span data-stu-id="9d0a9-105">**SidAndAttributesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9d0a9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9d0a9-106">Attributes and elements</span></span>

<span data-ttu-id="9d0a9-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d0a9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9d0a9-108">Attributes</span></span>

|<span data-ttu-id="9d0a9-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="9d0a9-109">**Attribute**</span></span>|<span data-ttu-id="9d0a9-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d0a9-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9d0a9-111">**Attributes**</span><span class="sxs-lookup"><span data-stu-id="9d0a9-111">**Attributes**</span></span> <br/> |<span data-ttu-id="9d0a9-112">Contiene los atributos de grupo.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-112">Contains group attributes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9d0a9-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9d0a9-113">Child elements</span></span>

|<span data-ttu-id="9d0a9-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d0a9-114">**Element**</span></span>|<span data-ttu-id="9d0a9-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d0a9-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d0a9-116">SecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="9d0a9-116">SecurityIdentifier</span></span>](securityidentifier.md) <br/> |<span data-ttu-id="9d0a9-117">Representa el formato de idioma (SDDL) de definición de descriptor de seguridad de un identificador de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-117">Represents the security descriptor definition language (SDDL) form of a security identifier.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9d0a9-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9d0a9-118">Parent elements</span></span>

|<span data-ttu-id="9d0a9-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d0a9-119">**Element**</span></span>|<span data-ttu-id="9d0a9-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d0a9-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d0a9-121">RestrictedGroupSids</span><span class="sxs-lookup"><span data-stu-id="9d0a9-121">RestrictedGroupSids</span></span>](restrictedgroupsids.md) <br/> |<span data-ttu-id="9d0a9-122">Representa una colección de grupos restringidos dentro de un símbolo (token) de usuario.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-122">Represents a collection of restricted groups within a user token.</span></span> <span data-ttu-id="9d0a9-123">No se admite la serialización de token.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-123">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d0a9-124">Notas</span><span class="sxs-lookup"><span data-stu-id="9d0a9-124">Remarks</span></span>

<span data-ttu-id="9d0a9-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="9d0a9-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d0a9-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9d0a9-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d0a9-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9d0a9-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9d0a9-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9d0a9-128">Schema Name</span></span>  <br/> |<span data-ttu-id="9d0a9-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="9d0a9-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="9d0a9-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9d0a9-130">Validation File</span></span>  <br/> |<span data-ttu-id="9d0a9-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9d0a9-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9d0a9-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9d0a9-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="9d0a9-133">False</span><span class="sxs-lookup"><span data-stu-id="9d0a9-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d0a9-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="9d0a9-134">See also</span></span>



- [<span data-ttu-id="9d0a9-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="9d0a9-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

