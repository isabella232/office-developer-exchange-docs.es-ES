---
title: Solicitud (SOAP) (GetOrganizationRelationship)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85dc155c-fad0-4756-b9a8-dedf5040a7c6
description: El elemento de solicitud representa una solicitud de GetOrganizationRelationshipSettingsRequest (SOAP). El elemento de solicitud es sólo para uso interno. Este elemento no se usa en los clientes.
ms.openlocfilehash: d3ae48ca403398288b8399ede82b98322a1b3260
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837122"
---
# <a name="request-getorganizationrelationship-soap"></a><span data-ttu-id="44ffc-105">Solicitud (SOAP) (GetOrganizationRelationship)</span><span class="sxs-lookup"><span data-stu-id="44ffc-105">Request (GetOrganizationRelationship) (SOAP)</span></span>

<span data-ttu-id="44ffc-106">El elemento de **solicitud** representa una solicitud de [GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="44ffc-106">The **Request** element represents a [GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md) request.</span></span> <span data-ttu-id="44ffc-107">El elemento de **solicitud** es sólo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="44ffc-107">The **Request** element is for internal use only.</span></span> <span data-ttu-id="44ffc-108">Este elemento no se usa en los clientes.</span><span class="sxs-lookup"><span data-stu-id="44ffc-108">This element is not used by clients.</span></span> 
  
```XML
<Request>
   <Domains/>
</Request>
```

 <span data-ttu-id="44ffc-109">**GetOrganizationRelationshipSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="44ffc-109">**GetOrganizationRelationshipSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="44ffc-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="44ffc-110">Attributes and elements</span></span>

<span data-ttu-id="44ffc-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="44ffc-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44ffc-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="44ffc-112">Attributes</span></span>

<span data-ttu-id="44ffc-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="44ffc-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="44ffc-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="44ffc-114">Child elements</span></span>

|<span data-ttu-id="44ffc-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="44ffc-115">**Element**</span></span>|<span data-ttu-id="44ffc-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="44ffc-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44ffc-117">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="44ffc-117">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="44ffc-118">Representa los dominios para la detección automática es para ejecutarse y que van a utilizarse en una consulta.</span><span class="sxs-lookup"><span data-stu-id="44ffc-118">Represents the domains for which Autodiscover is to be run and that are to be used in a query.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="44ffc-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="44ffc-119">Parent elements</span></span>

|<span data-ttu-id="44ffc-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="44ffc-120">**Element**</span></span>|<span data-ttu-id="44ffc-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="44ffc-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44ffc-122">GetOrganizationRelationshipSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="44ffc-122">GetOrganizationRelationshipSettingsRequestMessage (SOAP)</span></span>](getorganizationrelationshipsettingsrequestmessage-soap.md) <br/> |<span data-ttu-id="44ffc-123">Representa una solicitud de operación de la [operación de GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="44ffc-123">Represents a [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) operation request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="44ffc-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="44ffc-124">Text value</span></span>

<span data-ttu-id="44ffc-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="44ffc-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="44ffc-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="44ffc-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44ffc-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="44ffc-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="44ffc-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="44ffc-128">Schema Name</span></span>  <br/> |<span data-ttu-id="44ffc-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="44ffc-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="44ffc-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="44ffc-130">Validation File</span></span>  <br/> |<span data-ttu-id="44ffc-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="44ffc-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="44ffc-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="44ffc-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="44ffc-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="44ffc-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44ffc-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="44ffc-134">See also</span></span>



[<span data-ttu-id="44ffc-135">GetOrganizationRelationshipSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="44ffc-135">GetOrganizationRelationshipSettingsRequest (SOAP)</span></span>](getorganizationrelationshipsettingsrequest-soap.md)


[<span data-ttu-id="44ffc-136">Trabajar con detección automática</span><span class="sxs-lookup"><span data-stu-id="44ffc-136">Working with Autodiscover</span></span>](http://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

