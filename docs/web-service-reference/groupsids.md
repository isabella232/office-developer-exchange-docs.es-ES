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
description: El elemento GroupSids representa una colección de identificadores de seguridad de objetos de grupo del servicio de directorio de Active Directory.
ms.openlocfilehash: 40f36176fcaa3e2160237f269fb2dc3b12bf8af2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530067"
---
# <a name="groupsids"></a><span data-ttu-id="2e714-103">GroupSids</span><span class="sxs-lookup"><span data-stu-id="2e714-103">GroupSids</span></span>

<span data-ttu-id="2e714-104">El elemento **GroupSids** representa una colección de identificadores de seguridad de objetos de grupo del servicio de directorio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2e714-104">The **GroupSids** element represents a collection of Active Directory directory service group object security identifiers.</span></span> 
  
```xml
<GroupSids>
   <GroupIdentifier/>
</GroupSids>
```

 <span data-ttu-id="2e714-105">**NonEmptyArrayOfGroupIdentifiersType**</span><span class="sxs-lookup"><span data-stu-id="2e714-105">**NonEmptyArrayOfGroupIdentifiersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2e714-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2e714-106">Attributes and elements</span></span>

<span data-ttu-id="2e714-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2e714-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e714-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2e714-108">Attributes</span></span>

<span data-ttu-id="2e714-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2e714-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2e714-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2e714-110">Child elements</span></span>

|<span data-ttu-id="2e714-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2e714-111">**Element**</span></span>|<span data-ttu-id="2e714-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e714-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e714-113">GroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="2e714-113">GroupIdentifier</span></span>](groupidentifier.md) <br/> |<span data-ttu-id="2e714-114">Representa un único identificador de seguridad y un atributo para un grupo de objetos de Active Directory del que es miembro la cuenta.</span><span class="sxs-lookup"><span data-stu-id="2e714-114">Represents a single security identifier and attribute for an Active Directory object group of which the account is a member.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2e714-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2e714-115">Parent elements</span></span>

|<span data-ttu-id="2e714-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2e714-116">**Element**</span></span>|<span data-ttu-id="2e714-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e714-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e714-118">SerializedSecurityContext</span><span class="sxs-lookup"><span data-stu-id="2e714-118">SerializedSecurityContext</span></span>](serializedsecuritycontext.md) <br/> |<span data-ttu-id="2e714-119">Se usa en el encabezado del Protocolo simple de acceso a objetos (SOAP) para la serialización de tokens en la autenticación de servidor a servidor.</span><span class="sxs-lookup"><span data-stu-id="2e714-119">Used in the Simple Object Access Protocol (SOAP) header for token serialization in server-to-server authentication.</span></span> <span data-ttu-id="2e714-120">No se admite la serialización de tokens.</span><span class="sxs-lookup"><span data-stu-id="2e714-120">Token serialization is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e714-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2e714-121">Remarks</span></span>

<span data-ttu-id="2e714-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="2e714-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2e714-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2e714-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e714-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e714-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2e714-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2e714-125">Schema Name</span></span>  <br/> |<span data-ttu-id="2e714-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2e714-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="2e714-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2e714-127">Validation File</span></span>  <br/> |<span data-ttu-id="2e714-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="2e714-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2e714-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2e714-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="2e714-130">Falso</span><span class="sxs-lookup"><span data-stu-id="2e714-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e714-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e714-131">See also</span></span>



- [<span data-ttu-id="2e714-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2e714-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

