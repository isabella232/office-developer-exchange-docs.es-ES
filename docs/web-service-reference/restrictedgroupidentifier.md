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
description: El elemento RestrictGroupIdentifier representa el identificador de seguridad (SID) de grupo y los atributos de un grupo restringido dentro de un token de usuario.
ms.openlocfilehash: c95af4e09324e96f4551a05490dc200aec0cbd46
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465369"
---
# <a name="restrictedgroupidentifier"></a><span data-ttu-id="016f4-103">RestrictedGroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="016f4-103">RestrictedGroupIdentifier</span></span>

<span data-ttu-id="016f4-104">El elemento **RestrictGroupIdentifier** representa el identificador de seguridad (SID) de grupo y los atributos de un grupo restringido dentro de un token de usuario.</span><span class="sxs-lookup"><span data-stu-id="016f4-104">The **RestrictGroupIdentifier** element represents the group security identifier (SID) and attributes for a restricted group within a user token.</span></span> 
  
```xml
<RestrictedGroupIdentifier Attributes="">
   <SecurityIdentifier/>
</RestrictedGroupIdentifier>
```

 <span data-ttu-id="016f4-105">**SidAndAttributesType**</span><span class="sxs-lookup"><span data-stu-id="016f4-105">**SidAndAttributesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="016f4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="016f4-106">Attributes and elements</span></span>

<span data-ttu-id="016f4-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="016f4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="016f4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="016f4-108">Attributes</span></span>

|<span data-ttu-id="016f4-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="016f4-109">**Attribute**</span></span>|<span data-ttu-id="016f4-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="016f4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="016f4-111">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="016f4-111">**Attributes**</span></span> <br/> |<span data-ttu-id="016f4-112">Contiene los atributos de grupo.</span><span class="sxs-lookup"><span data-stu-id="016f4-112">Contains group attributes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="016f4-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="016f4-113">Child elements</span></span>

|<span data-ttu-id="016f4-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="016f4-114">**Element**</span></span>|<span data-ttu-id="016f4-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="016f4-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="016f4-116">SecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="016f4-116">SecurityIdentifier</span></span>](securityidentifier.md) <br/> |<span data-ttu-id="016f4-117">Representa el formato de lenguaje de definición de descriptores de seguridad (SDDL) de un identificador de seguridad.</span><span class="sxs-lookup"><span data-stu-id="016f4-117">Represents the security descriptor definition language (SDDL) form of a security identifier.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="016f4-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="016f4-118">Parent elements</span></span>

|<span data-ttu-id="016f4-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="016f4-119">**Element**</span></span>|<span data-ttu-id="016f4-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="016f4-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="016f4-121">RestrictedGroupSids</span><span class="sxs-lookup"><span data-stu-id="016f4-121">RestrictedGroupSids</span></span>](restrictedgroupsids.md) <br/> |<span data-ttu-id="016f4-122">Representa una colección de grupos restringidos dentro de un token de usuario.</span><span class="sxs-lookup"><span data-stu-id="016f4-122">Represents a collection of restricted groups within a user token.</span></span> <span data-ttu-id="016f4-123">No se admite la serialización de tokens.</span><span class="sxs-lookup"><span data-stu-id="016f4-123">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="016f4-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="016f4-124">Remarks</span></span>

<span data-ttu-id="016f4-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="016f4-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="016f4-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="016f4-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="016f4-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="016f4-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="016f4-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="016f4-128">Schema Name</span></span>  <br/> |<span data-ttu-id="016f4-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="016f4-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="016f4-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="016f4-130">Validation File</span></span>  <br/> |<span data-ttu-id="016f4-131">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="016f4-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="016f4-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="016f4-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="016f4-133">Falso</span><span class="sxs-lookup"><span data-stu-id="016f4-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="016f4-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="016f4-134">See also</span></span>



- [<span data-ttu-id="016f4-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="016f4-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

