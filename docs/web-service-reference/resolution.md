---
title: Solución
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Resolution
api_type:
- schema
ms.assetid: 573bed4b-d7b1-4baf-b16f-0795cdebf1a7
description: El elemento resolución contiene una única entidad resuelta.
ms.openlocfilehash: d65f6401e54a4397cad1bfcc85384f644fbae405
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837156"
---
# <a name="resolution"></a><span data-ttu-id="e5389-103">Solución</span><span class="sxs-lookup"><span data-stu-id="e5389-103">Resolution</span></span>

<span data-ttu-id="e5389-104">El elemento **resolución** contiene una única entidad resuelta.</span><span class="sxs-lookup"><span data-stu-id="e5389-104">The **Resolution** element contains a single resolved entity.</span></span> 
  
[<span data-ttu-id="e5389-105">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="e5389-105">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="e5389-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e5389-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="e5389-107">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e5389-107">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
  
[<span data-ttu-id="e5389-108">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="e5389-108">ResolutionSet</span></span>](resolutionset.md)
  
[<span data-ttu-id="e5389-109">Resoluci?n</span><span class="sxs-lookup"><span data-stu-id="e5389-109">Resolution</span></span>](resolution.md)
  
```xml
<Resolution>
   <Mailbox/>
   <Contact/>
</Resolution>
```

 <span data-ttu-id="e5389-110">**ResolutionType**</span><span class="sxs-lookup"><span data-stu-id="e5389-110">**ResolutionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e5389-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e5389-111">Attributes and elements</span></span>

<span data-ttu-id="e5389-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e5389-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e5389-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="e5389-113">Attributes</span></span>

<span data-ttu-id="e5389-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e5389-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e5389-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e5389-115">Child elements</span></span>

|<span data-ttu-id="e5389-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="e5389-116">**Element**</span></span>|<span data-ttu-id="e5389-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e5389-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e5389-118">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="e5389-118">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="e5389-119">Identifica un objeto de servicio de directorio de Active Directory habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="e5389-119">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
|[<span data-ttu-id="e5389-120">Contact</span><span class="sxs-lookup"><span data-stu-id="e5389-120">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="e5389-121">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="e5389-121">Represents an Exchange contact item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e5389-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e5389-122">Parent elements</span></span>

|<span data-ttu-id="e5389-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="e5389-123">**Element**</span></span>|<span data-ttu-id="e5389-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e5389-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e5389-125">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="e5389-125">ResolutionSet</span></span>](resolutionset.md) <br/> |<span data-ttu-id="e5389-126">Contiene una matriz de soluciones para un nombre ambiguo.</span><span class="sxs-lookup"><span data-stu-id="e5389-126">Contains an array of resolutions for an ambiguous name.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5389-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e5389-127">Remarks</span></span>

<span data-ttu-id="e5389-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="e5389-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e5389-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e5389-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5389-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e5389-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e5389-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e5389-131">Schema name</span></span>  <br/> |<span data-ttu-id="e5389-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="e5389-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="e5389-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e5389-133">Validation file</span></span>  <br/> |<span data-ttu-id="e5389-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e5389-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e5389-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e5389-135">Can be empty</span></span>  <br/> |<span data-ttu-id="e5389-136">False</span><span class="sxs-lookup"><span data-stu-id="e5389-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e5389-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5389-137">See also</span></span>



[<span data-ttu-id="e5389-138">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="e5389-138">ResolveNames</span></span>](resolvenames.md)
  
[<span data-ttu-id="e5389-139">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="e5389-139">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="e5389-140">Operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="e5389-140">ResolveNames operation</span></span>](resolvenames-operation.md)

