---
title: RestrictedGroupSids
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RestrictedGroupSids
api_type:
- schema
ms.assetid: 569ab552-5616-444a-a7f5-de366a684a34
description: El elemento RestrictedGroupSids representa una colección de grupos restringidos del token de un usuario.
ms.openlocfilehash: 739a73d2ac4bdbbee03650d035271b5c8d9ea25a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465362"
---
# <a name="restrictedgroupsids"></a><span data-ttu-id="853cb-103">RestrictedGroupSids</span><span class="sxs-lookup"><span data-stu-id="853cb-103">RestrictedGroupSids</span></span>

<span data-ttu-id="853cb-104">El elemento **RestrictedGroupSids** representa una colección de grupos restringidos del token de un usuario.</span><span class="sxs-lookup"><span data-stu-id="853cb-104">The **RestrictedGroupSids** element represents a collection of restricted groups from a user's token.</span></span> 
  
```xml
<RestrictedGroupSids>
   <RestrictedGroupIdentifier/>
</RestrictedGroupSids>
```

 <span data-ttu-id="853cb-105">**NonEmptyArrayOfRestrictedGroupIdentifiersType**</span><span class="sxs-lookup"><span data-stu-id="853cb-105">**NonEmptyArrayOfRestrictedGroupIdentifiersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="853cb-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="853cb-106">Attributes and elements</span></span>

<span data-ttu-id="853cb-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="853cb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="853cb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="853cb-108">Attributes</span></span>

<span data-ttu-id="853cb-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="853cb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="853cb-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="853cb-110">Child elements</span></span>

|<span data-ttu-id="853cb-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="853cb-111">**Element**</span></span>|<span data-ttu-id="853cb-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="853cb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="853cb-113">RestrictedGroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="853cb-113">RestrictedGroupIdentifier</span></span>](restrictedgroupidentifier.md) <br/> |<span data-ttu-id="853cb-114">Representa el identificador de seguridad (SID) de grupo y los atributos de un grupo restringido.</span><span class="sxs-lookup"><span data-stu-id="853cb-114">Represents the group security identifier (SID) and attributes for a restricted group.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="853cb-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="853cb-115">Parent elements</span></span>

|<span data-ttu-id="853cb-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="853cb-116">**Element**</span></span>|<span data-ttu-id="853cb-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="853cb-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="853cb-118">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="853cb-118">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="853cb-119">Se usa en el encabezado SOAP para la serialización de tokens en la autenticación de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="853cb-119">Used in the SOAP header for token serialization in server- to-server authentication.</span></span> <span data-ttu-id="853cb-120">No se admite la serialización de tokens.</span><span class="sxs-lookup"><span data-stu-id="853cb-120">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="853cb-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="853cb-121">Remarks</span></span>

<span data-ttu-id="853cb-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="853cb-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="853cb-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="853cb-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="853cb-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="853cb-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="853cb-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="853cb-125">Schema Name</span></span>  <br/> |<span data-ttu-id="853cb-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="853cb-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="853cb-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="853cb-127">Validation File</span></span>  <br/> |<span data-ttu-id="853cb-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="853cb-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="853cb-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="853cb-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="853cb-130">Falso</span><span class="sxs-lookup"><span data-stu-id="853cb-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="853cb-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="853cb-131">See also</span></span>



- [<span data-ttu-id="853cb-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="853cb-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

