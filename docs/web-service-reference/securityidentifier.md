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
description: El elemento SecurityIdentifier representa el formulario de idioma (SDDL) de definición de descriptor de seguridad de un identificador de seguridad (SID).
ms.openlocfilehash: c18d7d4505c618792497c32c7499eab9ac82989e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837314"
---
# <a name="securityidentifier"></a><span data-ttu-id="73943-103">SecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="73943-103">SecurityIdentifier</span></span>

<span data-ttu-id="73943-104">El elemento **SecurityIdentifier** representa el formulario de idioma (SDDL) de definición de descriptor de seguridad de un identificador de seguridad ( [SID](sid.md)).</span><span class="sxs-lookup"><span data-stu-id="73943-104">The **SecurityIdentifier** element represents the security descriptor definition language (SDDL) form of a security identifier ( [SID](sid.md)).</span></span>
  
```xml
<SecurityIdentifier/>
```

 <span data-ttu-id="73943-105">**string**</span><span class="sxs-lookup"><span data-stu-id="73943-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="73943-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="73943-106">Attributes and elements</span></span>

<span data-ttu-id="73943-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="73943-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73943-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="73943-108">Attributes</span></span>

<span data-ttu-id="73943-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="73943-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="73943-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="73943-110">Child elements</span></span>

<span data-ttu-id="73943-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="73943-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="73943-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="73943-112">Parent elements</span></span>

|<span data-ttu-id="73943-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="73943-113">**Element**</span></span>|<span data-ttu-id="73943-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="73943-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73943-115">GroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="73943-115">GroupIdentifier</span></span>](groupidentifier.md) <br/> |<span data-ttu-id="73943-116">Representa un identificador de seguridad único y un atributo para un grupo de objetos de Active Directory de que la cuenta es miembro.</span><span class="sxs-lookup"><span data-stu-id="73943-116">Represents a single security identifier and attribute for an Active Directory object group of which the account is a member.</span></span>  <br/> <span data-ttu-id="73943-117">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="73943-117">The following is the XPath expression to this element:</span></span>  <br/>  `/SerializedSecurityContext/GroupSids/GroupIdentifier[i]` <br/> |
|[<span data-ttu-id="73943-118">RestrictedGroupIdentifier</span><span class="sxs-lookup"><span data-stu-id="73943-118">RestrictedGroupIdentifier</span></span>](restrictedgroupidentifier.md) <br/> |<span data-ttu-id="73943-119">Representa el identificador del grupo de seguridad y los atributos de un grupo dentro de un token de usuario restringido.</span><span class="sxs-lookup"><span data-stu-id="73943-119">Represents the group security identifier and attributes for a restricted group within a user token.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73943-120">Notas</span><span class="sxs-lookup"><span data-stu-id="73943-120">Remarks</span></span>

<span data-ttu-id="73943-121">Este elemento se usa en el encabezado SOAP Simple Object Access Protocol ().</span><span class="sxs-lookup"><span data-stu-id="73943-121">This element is used in the Simple Object Access Protocol (SOAP) header.</span></span>
  
<span data-ttu-id="73943-122">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="73943-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="73943-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="73943-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73943-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="73943-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="73943-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="73943-125">Schema Name</span></span>  <br/> |<span data-ttu-id="73943-126">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="73943-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="73943-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="73943-127">Validation File</span></span>  <br/> |<span data-ttu-id="73943-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="73943-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="73943-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="73943-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="73943-130">False</span><span class="sxs-lookup"><span data-stu-id="73943-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="73943-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="73943-131">See also</span></span>



- [<span data-ttu-id="73943-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="73943-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

