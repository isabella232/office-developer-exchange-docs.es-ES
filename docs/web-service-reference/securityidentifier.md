---
title: SecurityIdentifier
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SecurityIdentifier
api_type:
- schema
ms.assetid: f7656729-f2c9-41cc-b1ec-60f480fc4dab
description: El elemento SecurityIdentifier representa el formato de lenguaje de definición de descriptores de seguridad (SDDL) de un identificador de seguridad (SID).
ms.openlocfilehash: c55e4a7f7f0b8f8a40e6fcaf8d18e253a6da2679
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468806"
---
# <a name="securityidentifier"></a><span data-ttu-id="2e673-103">SecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="2e673-103">SecurityIdentifier</span></span>

<span data-ttu-id="2e673-104">El elemento **SecurityIdentifier** representa el formato de lenguaje de definición de descriptores de seguridad (SDDL) de un identificador de seguridad ( [SID](sid.md)).</span><span class="sxs-lookup"><span data-stu-id="2e673-104">The **SecurityIdentifier** element represents the security descriptor definition language (SDDL) form of a security identifier ( [SID](sid.md)).</span></span>
  
```xml
<SecurityIdentifier/>
```

 <span data-ttu-id="2e673-105">**string**</span><span class="sxs-lookup"><span data-stu-id="2e673-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2e673-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2e673-106">Attributes and elements</span></span>

<span data-ttu-id="2e673-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2e673-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e673-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2e673-108">Attributes</span></span>

<span data-ttu-id="2e673-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2e673-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2e673-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2e673-110">Child elements</span></span>

<span data-ttu-id="2e673-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2e673-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2e673-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2e673-112">Parent elements</span></span>

|<span data-ttu-id="2e673-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2e673-113">**Element**</span></span>|<span data-ttu-id="2e673-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e673-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e673-115">GroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="2e673-115">GroupIdentifier</span></span>](groupidentifier.md) <br/> |<span data-ttu-id="2e673-116">Representa un único identificador de seguridad y un atributo para un grupo de objetos de Active Directory del que es miembro la cuenta.</span><span class="sxs-lookup"><span data-stu-id="2e673-116">Represents a single security identifier and attribute for an Active Directory object group of which the account is a member.</span></span>  <br/> <span data-ttu-id="2e673-117">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="2e673-117">The following is the XPath expression to this element:</span></span>  <br/>  `/SerializedSecurityContext/GroupSids/GroupIdentifier[i]` <br/> |
|[<span data-ttu-id="2e673-118">RestrictedGroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="2e673-118">RestrictedGroupIdentifier</span></span>](restrictedgroupidentifier.md) <br/> |<span data-ttu-id="2e673-119">Representa el identificador de seguridad de grupo y los atributos de un grupo restringido dentro de un token de usuario.</span><span class="sxs-lookup"><span data-stu-id="2e673-119">Represents the group security identifier and attributes for a restricted group within a user token.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e673-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2e673-120">Remarks</span></span>

<span data-ttu-id="2e673-121">Este elemento se usa en el encabezado del Protocolo simple de acceso a objetos (SOAP).</span><span class="sxs-lookup"><span data-stu-id="2e673-121">This element is used in the Simple Object Access Protocol (SOAP) header.</span></span>
  
<span data-ttu-id="2e673-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="2e673-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2e673-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2e673-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e673-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e673-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2e673-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2e673-125">Schema Name</span></span>  <br/> |<span data-ttu-id="2e673-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2e673-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="2e673-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2e673-127">Validation File</span></span>  <br/> |<span data-ttu-id="2e673-128">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="2e673-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2e673-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2e673-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="2e673-130">Falso</span><span class="sxs-lookup"><span data-stu-id="2e673-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e673-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e673-131">See also</span></span>



- [<span data-ttu-id="2e673-132">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2e673-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

