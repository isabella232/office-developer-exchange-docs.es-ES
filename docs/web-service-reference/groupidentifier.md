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
description: El elemento GroupIdentifier representa un único identificador de seguridad y un atributo para un grupo de objetos de servicio de directorio de Active Directory del que es miembro la cuenta.
ms.openlocfilehash: 8b427b9228cc5e66f46f70389acf2fa4bcd283b3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530806"
---
# <a name="groupidentifier"></a><span data-ttu-id="d51fb-103">GroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="d51fb-103">GroupIdentifier</span></span>

<span data-ttu-id="d51fb-104">El elemento **GroupIdentifier** representa un único identificador de seguridad y un atributo para un grupo de objetos de servicio de directorio de Active Directory del que es miembro la cuenta.</span><span class="sxs-lookup"><span data-stu-id="d51fb-104">The **GroupIdentifier** element represents a single security identifier and attribute for an Active Directory directory service object group of which the account is a member.</span></span> 
  
```xml
<GroupIdentifier>
   <SecurityIdentifier/>
</GroupIdentifier>
```

 <span data-ttu-id="d51fb-105">**SidAndAttributesType**</span><span class="sxs-lookup"><span data-stu-id="d51fb-105">**SidAndAttributesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d51fb-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d51fb-106">Attributes and elements</span></span>

<span data-ttu-id="d51fb-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d51fb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d51fb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d51fb-108">Attributes</span></span>

|<span data-ttu-id="d51fb-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="d51fb-109">**Attribute**</span></span>|<span data-ttu-id="d51fb-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d51fb-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d51fb-111">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="d51fb-111">**Attributes**</span></span> <br/> |<span data-ttu-id="d51fb-112">Contiene los atributos de grupo.</span><span class="sxs-lookup"><span data-stu-id="d51fb-112">Contains group attributes.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d51fb-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d51fb-113">Child elements</span></span>

|<span data-ttu-id="d51fb-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d51fb-114">**Element**</span></span>|<span data-ttu-id="d51fb-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d51fb-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d51fb-116">SecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="d51fb-116">SecurityIdentifier</span></span>](securityidentifier.md) <br/> |<span data-ttu-id="d51fb-117">Representa el formato de lenguaje de definición de descriptores de seguridad (SDDL) de un identificador de seguridad ([SID](sid.md)) que representa el grupo.</span><span class="sxs-lookup"><span data-stu-id="d51fb-117">Represents the security descriptor definition language (SDDL) form of a security identifier ([SID](sid.md)) that represents the group.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d51fb-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d51fb-118">Parent elements</span></span>

|<span data-ttu-id="d51fb-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d51fb-119">**Element**</span></span>|<span data-ttu-id="d51fb-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d51fb-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d51fb-121">GroupSids</span><span class="sxs-lookup"><span data-stu-id="d51fb-121">GroupSids</span></span>](groupsids.md) <br/> |<span data-ttu-id="d51fb-122">Representa una colección de identificadores de seguridad de objetos de grupo de Active Directory que componen un token de cuenta para la serialización de tokens.</span><span class="sxs-lookup"><span data-stu-id="d51fb-122">Represents a collection of Active Directory group object security identifiers that make up an account token for token serialization.</span></span> <span data-ttu-id="d51fb-123">No se admite la serialización de tokens.</span><span class="sxs-lookup"><span data-stu-id="d51fb-123">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d51fb-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d51fb-124">Remarks</span></span>

<span data-ttu-id="d51fb-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="d51fb-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d51fb-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d51fb-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d51fb-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="d51fb-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d51fb-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d51fb-128">Schema Name</span></span>  <br/> |<span data-ttu-id="d51fb-129">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="d51fb-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="d51fb-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d51fb-130">Validation File</span></span>  <br/> |<span data-ttu-id="d51fb-131">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d51fb-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d51fb-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d51fb-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="d51fb-133">Falso</span><span class="sxs-lookup"><span data-stu-id="d51fb-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d51fb-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="d51fb-134">See also</span></span>



- [<span data-ttu-id="d51fb-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="d51fb-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

