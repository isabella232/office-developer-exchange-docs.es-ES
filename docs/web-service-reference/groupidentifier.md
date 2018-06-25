---
title: GroupIdentifier
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupIdentifier
api_type:
- schema
ms.assetid: bdc6fc1e-4979-42da-a35b-e3017988c7d3
description: El elemento GroupIdentifier representa un identificador de seguridad único y un atributo para un grupo de objetos de servicio de directorio de Active Directory de que la cuenta es miembro.
ms.openlocfilehash: d73d72979762238ca09496cfbd6636b4ff44a969
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835767"
---
# <a name="groupidentifier"></a><span data-ttu-id="3cac4-103">GroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="3cac4-103">GroupIdentifier</span></span>

<span data-ttu-id="3cac4-104">El elemento **GroupIdentifier** representa un identificador de seguridad único y un atributo para un grupo de objetos de servicio de directorio de Active Directory de que la cuenta es miembro.</span><span class="sxs-lookup"><span data-stu-id="3cac4-104">The **GroupIdentifier** element represents a single security identifier and attribute for an Active Directory directory service object group of which the account is a member.</span></span> 
  
```xml
<GroupIdentifier>
   <SecurityIdentifier/>
</GroupIdentifier>
```

 <span data-ttu-id="3cac4-105">**SidAndAttributesType**</span><span class="sxs-lookup"><span data-stu-id="3cac4-105">**SidAndAttributesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3cac4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3cac4-106">Attributes and elements</span></span>

<span data-ttu-id="3cac4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3cac4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3cac4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3cac4-108">Attributes</span></span>

|<span data-ttu-id="3cac4-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="3cac4-109">**Attribute**</span></span>|<span data-ttu-id="3cac4-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3cac4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3cac4-111">**Attributes**</span><span class="sxs-lookup"><span data-stu-id="3cac4-111">**Attributes**</span></span> <br/> |<span data-ttu-id="3cac4-112">Contiene los atributos de grupo.</span><span class="sxs-lookup"><span data-stu-id="3cac4-112">Contains group attributes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3cac4-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3cac4-113">Child elements</span></span>

|<span data-ttu-id="3cac4-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="3cac4-114">**Element**</span></span>|<span data-ttu-id="3cac4-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3cac4-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3cac4-116">SecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="3cac4-116">SecurityIdentifier</span></span>](securityidentifier.md) <br/> |<span data-ttu-id="3cac4-117">Representa el formato de idioma (SDDL) de definición de descriptor de seguridad de un identificador de seguridad ([SID](sid.md)) que representa el grupo.</span><span class="sxs-lookup"><span data-stu-id="3cac4-117">Represents the security descriptor definition language (SDDL) form of a security identifier ([SID](sid.md)) that represents the group.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3cac4-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3cac4-118">Parent elements</span></span>

|<span data-ttu-id="3cac4-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="3cac4-119">**Element**</span></span>|<span data-ttu-id="3cac4-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3cac4-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3cac4-121">GroupSids</span><span class="sxs-lookup"><span data-stu-id="3cac4-121">GroupSids</span></span>](groupsids.md) <br/> |<span data-ttu-id="3cac4-122">Representa una colección de identificadores de seguridad de objeto de grupo de Active Directory que componen un símbolo (token) de cuenta para la serialización de token.</span><span class="sxs-lookup"><span data-stu-id="3cac4-122">Represents a collection of Active Directory group object security identifiers that make up an account token for token serialization.</span></span> <span data-ttu-id="3cac4-123">No se admite la serialización de token.</span><span class="sxs-lookup"><span data-stu-id="3cac4-123">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3cac4-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3cac4-124">Remarks</span></span>

<span data-ttu-id="3cac4-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3cac4-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3cac4-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3cac4-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3cac4-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3cac4-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3cac4-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3cac4-128">Schema Name</span></span>  <br/> |<span data-ttu-id="3cac4-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3cac4-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="3cac4-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3cac4-130">Validation File</span></span>  <br/> |<span data-ttu-id="3cac4-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3cac4-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3cac4-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3cac4-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="3cac4-133">False</span><span class="sxs-lookup"><span data-stu-id="3cac4-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3cac4-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3cac4-134">See also</span></span>



- [<span data-ttu-id="3cac4-135">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3cac4-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

