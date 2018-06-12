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
description: El elemento RestrictedGroupSids representa una colección de grupos restringidos de símbolo (token) de un usuario.
ms.openlocfilehash: fcfee809261c7ed0a4e0d092c091841fec641e46
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837201"
---
# <a name="restrictedgroupsids"></a><span data-ttu-id="759ee-103">RestrictedGroupSids</span><span class="sxs-lookup"><span data-stu-id="759ee-103">RestrictedGroupSids</span></span>

<span data-ttu-id="759ee-104">El elemento **RestrictedGroupSids** representa una colección de grupos restringidos de símbolo (token) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="759ee-104">The **RestrictedGroupSids** element represents a collection of restricted groups from a user's token.</span></span> 
  
```xml
<RestrictedGroupSids>
   <RestrictedGroupIdentifier/>
</RestrictedGroupSids>
```

 <span data-ttu-id="759ee-105">**NonEmptyArrayOfRestrictedGroupIdentifiersType**</span><span class="sxs-lookup"><span data-stu-id="759ee-105">**NonEmptyArrayOfRestrictedGroupIdentifiersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="759ee-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="759ee-106">Attributes and elements</span></span>

<span data-ttu-id="759ee-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="759ee-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="759ee-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="759ee-108">Attributes</span></span>

<span data-ttu-id="759ee-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="759ee-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="759ee-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="759ee-110">Child elements</span></span>

|<span data-ttu-id="759ee-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="759ee-111">**Element**</span></span>|<span data-ttu-id="759ee-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="759ee-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="759ee-113">RestrictedGroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="759ee-113">RestrictedGroupIdentifier</span></span>](restrictedgroupidentifier.md) <br/> |<span data-ttu-id="759ee-114">Representa el identificador del grupo de seguridad (SID) y los atributos de un grupo restringido.</span><span class="sxs-lookup"><span data-stu-id="759ee-114">Represents the group security identifier (SID) and attributes for a restricted group.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="759ee-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="759ee-115">Parent elements</span></span>

|<span data-ttu-id="759ee-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="759ee-116">**Element**</span></span>|<span data-ttu-id="759ee-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="759ee-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="759ee-118">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="759ee-118">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="759ee-119">Se usa en el encabezado SOAP para la serialización de token de autenticación de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="759ee-119">Used in the SOAP header for token serialization in server- to-server authentication.</span></span> <span data-ttu-id="759ee-120">No se admite la serialización de token.</span><span class="sxs-lookup"><span data-stu-id="759ee-120">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="759ee-121">Notas</span><span class="sxs-lookup"><span data-stu-id="759ee-121">Remarks</span></span>

<span data-ttu-id="759ee-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="759ee-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="759ee-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="759ee-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="759ee-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="759ee-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="759ee-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="759ee-125">Schema Name</span></span>  <br/> |<span data-ttu-id="759ee-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="759ee-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="759ee-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="759ee-127">Validation File</span></span>  <br/> |<span data-ttu-id="759ee-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="759ee-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="759ee-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="759ee-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="759ee-130">False</span><span class="sxs-lookup"><span data-stu-id="759ee-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="759ee-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="759ee-131">See also</span></span>



- [<span data-ttu-id="759ee-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="759ee-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

