---
title: GroupSids
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupSids
api_type:
- schema
ms.assetid: ebb00653-83f0-4080-a902-c38df6719800
description: El elemento GroupSids representa una colección de identificadores de seguridad de objeto de grupo servicio de directorio de Active Directory.
ms.openlocfilehash: c24c8ea3c3b7d37f41986997ed924c951b4a48ef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835790"
---
# <a name="groupsids"></a><span data-ttu-id="635bc-103">GroupSids</span><span class="sxs-lookup"><span data-stu-id="635bc-103">GroupSids</span></span>

<span data-ttu-id="635bc-104">El elemento **GroupSids** representa una colección de identificadores de seguridad de objeto de grupo servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="635bc-104">The **GroupSids** element represents a collection of Active Directory directory service group object security identifiers.</span></span> 
  
```xml
<GroupSids>
   <GroupIdentifier/>
</GroupSids>
```

 <span data-ttu-id="635bc-105">**NonEmptyArrayOfGroupIdentifiersType**</span><span class="sxs-lookup"><span data-stu-id="635bc-105">**NonEmptyArrayOfGroupIdentifiersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="635bc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="635bc-106">Attributes and elements</span></span>

<span data-ttu-id="635bc-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="635bc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="635bc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="635bc-108">Attributes</span></span>

<span data-ttu-id="635bc-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="635bc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="635bc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="635bc-110">Child elements</span></span>

|<span data-ttu-id="635bc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="635bc-111">**Element**</span></span>|<span data-ttu-id="635bc-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="635bc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="635bc-113">GroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="635bc-113">GroupIdentifier</span></span>](groupidentifier.md) <br/> |<span data-ttu-id="635bc-114">Representa un identificador de seguridad único y un atributo para un grupo de objetos de Active Directory de que la cuenta es miembro.</span><span class="sxs-lookup"><span data-stu-id="635bc-114">Represents a single security identifier and attribute for an Active Directory object group of which the account is a member.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="635bc-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="635bc-115">Parent elements</span></span>

|<span data-ttu-id="635bc-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="635bc-116">**Element**</span></span>|<span data-ttu-id="635bc-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="635bc-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="635bc-118">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="635bc-118">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="635bc-119">Se usa en el encabezado de protocolo de acceso de objeto Simple (SOAP) para la serialización de token de autenticación de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="635bc-119">Used in the Simple Object Access Protocol (SOAP) header for token serialization in server-to-server authentication.</span></span> <span data-ttu-id="635bc-120">No se admite la serialización de token.</span><span class="sxs-lookup"><span data-stu-id="635bc-120">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="635bc-121">Notas</span><span class="sxs-lookup"><span data-stu-id="635bc-121">Remarks</span></span>

<span data-ttu-id="635bc-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="635bc-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="635bc-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="635bc-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="635bc-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="635bc-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="635bc-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="635bc-125">Schema Name</span></span>  <br/> |<span data-ttu-id="635bc-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="635bc-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="635bc-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="635bc-127">Validation File</span></span>  <br/> |<span data-ttu-id="635bc-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="635bc-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="635bc-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="635bc-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="635bc-130">False</span><span class="sxs-lookup"><span data-stu-id="635bc-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="635bc-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="635bc-131">See also</span></span>



- [<span data-ttu-id="635bc-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="635bc-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

