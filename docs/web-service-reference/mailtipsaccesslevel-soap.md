---
title: MailTipsAccessLevel (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 730e349e-8250-4236-af53-cd9039c74d8f
description: El elemento MailTipsAccessLevel representa la propiedad MailTipsAccessLevel. El elemento MailTipsAccessLevel es sólo para uso interno. Este elemento no se usa en los clientes.
ms.openlocfilehash: 35fb4aa56bbfa42ac4be196a379dc48aff5ec101
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836313"
---
# <a name="mailtipsaccesslevel-soap"></a><span data-ttu-id="543b1-105">MailTipsAccessLevel (SOAP)</span><span class="sxs-lookup"><span data-stu-id="543b1-105">MailTipsAccessLevel (SOAP)</span></span>

<span data-ttu-id="543b1-106">El elemento **MailTipsAccessLevel** representa la propiedad **MailTipsAccessLevel** .</span><span class="sxs-lookup"><span data-stu-id="543b1-106">The **MailTipsAccessLevel** element represents the **MailTipsAccessLevel** property.</span></span> <span data-ttu-id="543b1-107">El elemento **MailTipsAccessLevel** es sólo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="543b1-107">The **MailTipsAccessLevel** element is for internal use only.</span></span> <span data-ttu-id="543b1-108">Este elemento no se usa en los clientes.</span><span class="sxs-lookup"><span data-stu-id="543b1-108">This element is not used by clients.</span></span> 
  
```XML
<MailTipsAccessLevel/>
```

 <span data-ttu-id="543b1-109">**string**</span><span class="sxs-lookup"><span data-stu-id="543b1-109">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="543b1-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="543b1-110">Attributes and elements</span></span>

<span data-ttu-id="543b1-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="543b1-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="543b1-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="543b1-112">Attributes</span></span>

<span data-ttu-id="543b1-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="543b1-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="543b1-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="543b1-114">Child elements</span></span>

<span data-ttu-id="543b1-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="543b1-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="543b1-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="543b1-116">Parent elements</span></span>

|<span data-ttu-id="543b1-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="543b1-117">**Element**</span></span>|<span data-ttu-id="543b1-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="543b1-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="543b1-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="543b1-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="543b1-120">Representa una lista de relaciones de organización para una sola organización.</span><span class="sxs-lookup"><span data-stu-id="543b1-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="543b1-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="543b1-121">Remarks</span></span>

<span data-ttu-id="543b1-122">Este elemento especifica la cantidad máxima de detalle de sugerencias de correo que se devuelve en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="543b1-122">This element specifies the maximum amount of mail tips detail that will be returned in the response.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="543b1-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="543b1-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="543b1-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="543b1-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="543b1-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="543b1-125">Schema Name</span></span>  <br/> |<span data-ttu-id="543b1-126">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="543b1-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="543b1-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="543b1-127">Validation File</span></span>  <br/> |<span data-ttu-id="543b1-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="543b1-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="543b1-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="543b1-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="543b1-130">Verdadero</span><span class="sxs-lookup"><span data-stu-id="543b1-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="543b1-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="543b1-131">See also</span></span>



[<span data-ttu-id="543b1-132">Operación GetOrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="543b1-132">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

