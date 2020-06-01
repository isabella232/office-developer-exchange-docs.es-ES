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
description: El elemento Resolution contiene una única entidad resuelta.
ms.openlocfilehash: 63c80f3c8d7dabf7e6dc1494df04c0be821b28bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468288"
---
# <a name="resolution"></a><span data-ttu-id="2a26b-103">Solución</span><span class="sxs-lookup"><span data-stu-id="2a26b-103">Resolution</span></span>

<span data-ttu-id="2a26b-104">El elemento **Resolution** contiene una única entidad resuelta.</span><span class="sxs-lookup"><span data-stu-id="2a26b-104">The **Resolution** element contains a single resolved entity.</span></span> 
  
[<span data-ttu-id="2a26b-105">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="2a26b-105">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="2a26b-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2a26b-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="2a26b-107">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2a26b-107">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
  
[<span data-ttu-id="2a26b-108">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="2a26b-108">ResolutionSet</span></span>](resolutionset.md)
  
[<span data-ttu-id="2a26b-109">Resolución</span><span class="sxs-lookup"><span data-stu-id="2a26b-109">Resolution</span></span>](resolution.md)
  
```xml
<Resolution>
   <Mailbox/>
   <Contact/>
</Resolution>
```

 <span data-ttu-id="2a26b-110">**ResolutionType**</span><span class="sxs-lookup"><span data-stu-id="2a26b-110">**ResolutionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2a26b-111">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2a26b-111">Attributes and elements</span></span>

<span data-ttu-id="2a26b-112">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2a26b-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2a26b-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="2a26b-113">Attributes</span></span>

<span data-ttu-id="2a26b-114">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2a26b-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2a26b-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2a26b-115">Child elements</span></span>

|<span data-ttu-id="2a26b-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2a26b-116">**Element**</span></span>|<span data-ttu-id="2a26b-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a26b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a26b-118">Buzón</span><span class="sxs-lookup"><span data-stu-id="2a26b-118">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="2a26b-119">Identifica un objeto de servicio de directorio de Active Directory habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="2a26b-119">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
|[<span data-ttu-id="2a26b-120">Contacto</span><span class="sxs-lookup"><span data-stu-id="2a26b-120">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="2a26b-121">Representa un elemento de contacto de Exchange.</span><span class="sxs-lookup"><span data-stu-id="2a26b-121">Represents an Exchange contact item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2a26b-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2a26b-122">Parent elements</span></span>

|<span data-ttu-id="2a26b-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2a26b-123">**Element**</span></span>|<span data-ttu-id="2a26b-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2a26b-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2a26b-125">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="2a26b-125">ResolutionSet</span></span>](resolutionset.md) <br/> |<span data-ttu-id="2a26b-126">Contiene una matriz de resoluciones para un nombre ambiguo.</span><span class="sxs-lookup"><span data-stu-id="2a26b-126">Contains an array of resolutions for an ambiguous name.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a26b-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2a26b-127">Remarks</span></span>

<span data-ttu-id="2a26b-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="2a26b-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2a26b-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2a26b-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a26b-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a26b-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2a26b-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2a26b-131">Schema name</span></span>  <br/> |<span data-ttu-id="2a26b-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="2a26b-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="2a26b-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2a26b-133">Validation file</span></span>  <br/> |<span data-ttu-id="2a26b-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="2a26b-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2a26b-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2a26b-135">Can be empty</span></span>  <br/> |<span data-ttu-id="2a26b-136">Falso</span><span class="sxs-lookup"><span data-stu-id="2a26b-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2a26b-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a26b-137">See also</span></span>



[<span data-ttu-id="2a26b-138">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="2a26b-138">ResolveNames</span></span>](resolvenames.md)
  
[<span data-ttu-id="2a26b-139">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="2a26b-139">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="2a26b-140">Operación ResolveNames</span><span class="sxs-lookup"><span data-stu-id="2a26b-140">ResolveNames operation</span></span>](resolvenames-operation.md)

