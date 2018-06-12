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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837156"
---
# <a name="resolution"></a><span data-ttu-id="54290-103">Solución</span><span class="sxs-lookup"><span data-stu-id="54290-103">Resolution</span></span>

<span data-ttu-id="54290-104">El elemento **resolución** contiene una única entidad resuelta.</span><span class="sxs-lookup"><span data-stu-id="54290-104">The **Resolution** element contains a single resolved entity.</span></span> 
  
[<span data-ttu-id="54290-105">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="54290-105">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="54290-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="54290-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="54290-107">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="54290-107">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
  
[<span data-ttu-id="54290-108">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="54290-108">ResolutionSet</span></span>](resolutionset.md)
  
[<span data-ttu-id="54290-109">Resoluci?n</span><span class="sxs-lookup"><span data-stu-id="54290-109">Resolution</span></span>](resolution.md)
  
```xml
<Resolution>
   <Mailbox/>
   <Contact/>
</Resolution>
```

 <span data-ttu-id="54290-110">**ResolutionType**</span><span class="sxs-lookup"><span data-stu-id="54290-110">**ResolutionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="54290-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="54290-111">Attributes and elements</span></span>

<span data-ttu-id="54290-112">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="54290-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54290-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="54290-113">Attributes</span></span>

<span data-ttu-id="54290-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="54290-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="54290-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="54290-115">Child elements</span></span>

|<span data-ttu-id="54290-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="54290-116">**Element**</span></span>|<span data-ttu-id="54290-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="54290-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54290-118">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="54290-118">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="54290-119">Identifica un objeto de servicio de directorio de Active Directory habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="54290-119">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
|[<span data-ttu-id="54290-120">Contact</span><span class="sxs-lookup"><span data-stu-id="54290-120">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="54290-121">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="54290-121">Represents an Exchange contact item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="54290-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="54290-122">Parent elements</span></span>

|<span data-ttu-id="54290-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="54290-123">**Element**</span></span>|<span data-ttu-id="54290-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="54290-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54290-125">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="54290-125">ResolutionSet</span></span>](resolutionset.md) <br/> |<span data-ttu-id="54290-126">Contiene una matriz de soluciones para un nombre ambiguo.</span><span class="sxs-lookup"><span data-stu-id="54290-126">Contains an array of resolutions for an ambiguous name.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54290-127">Notas</span><span class="sxs-lookup"><span data-stu-id="54290-127">Remarks</span></span>

<span data-ttu-id="54290-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="54290-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="54290-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="54290-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54290-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="54290-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="54290-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="54290-131">Schema name</span></span>  <br/> |<span data-ttu-id="54290-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="54290-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="54290-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="54290-133">Validation file</span></span>  <br/> |<span data-ttu-id="54290-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="54290-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="54290-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="54290-135">Can be empty</span></span>  <br/> |<span data-ttu-id="54290-136">False</span><span class="sxs-lookup"><span data-stu-id="54290-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="54290-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="54290-137">See also</span></span>



[<span data-ttu-id="54290-138">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="54290-138">ResolveNames</span></span>](resolvenames.md)
  
[<span data-ttu-id="54290-139">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="54290-139">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="54290-140">Operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="54290-140">ResolveNames operation</span></span>](resolvenames-operation.md)

