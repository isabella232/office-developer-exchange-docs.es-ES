---
title: Request (GetOrganizationRelationship) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85dc155c-fad0-4756-b9a8-dedf5040a7c6
description: El elemento request representa una solicitud GetOrganizationRelationshipSettingsRequest (SOAP). El elemento request es solo para uso interno. Los clientes no usan este elemento.
ms.openlocfilehash: 90ccd3579c91c916ea645e6a3b466c9de4706421
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459563"
---
# <a name="request-getorganizationrelationship-soap"></a><span data-ttu-id="13f96-105">Request (GetOrganizationRelationship) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="13f96-105">Request (GetOrganizationRelationship) (SOAP)</span></span>

<span data-ttu-id="13f96-106">El elemento **request** representa una solicitud [GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="13f96-106">The **Request** element represents a [GetOrganizationRelationshipSettingsRequest (SOAP)](getorganizationrelationshipsettingsrequest-soap.md) request.</span></span> <span data-ttu-id="13f96-107">El elemento **request** es solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="13f96-107">The **Request** element is for internal use only.</span></span> <span data-ttu-id="13f96-108">Los clientes no usan este elemento.</span><span class="sxs-lookup"><span data-stu-id="13f96-108">This element is not used by clients.</span></span> 
  
```XML
<Request>
   <Domains/>
</Request>
```

 <span data-ttu-id="13f96-109">**GetOrganizationRelationshipSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="13f96-109">**GetOrganizationRelationshipSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="13f96-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="13f96-110">Attributes and elements</span></span>

<span data-ttu-id="13f96-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="13f96-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13f96-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="13f96-112">Attributes</span></span>

<span data-ttu-id="13f96-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="13f96-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="13f96-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="13f96-114">Child elements</span></span>

|<span data-ttu-id="13f96-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="13f96-115">**Element**</span></span>|<span data-ttu-id="13f96-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13f96-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13f96-117">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="13f96-117">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="13f96-118">Representa los dominios para los que se ejecutará detección automática y que se van a usar en una consulta.</span><span class="sxs-lookup"><span data-stu-id="13f96-118">Represents the domains for which Autodiscover is to be run and that are to be used in a query.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="13f96-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="13f96-119">Parent elements</span></span>

|<span data-ttu-id="13f96-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="13f96-120">**Element**</span></span>|<span data-ttu-id="13f96-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13f96-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13f96-122">GetOrganizationRelationshipSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="13f96-122">GetOrganizationRelationshipSettingsRequestMessage (SOAP)</span></span>](getorganizationrelationshipsettingsrequestmessage-soap.md) <br/> |<span data-ttu-id="13f96-123">Representa una solicitud de operación de [GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="13f96-123">Represents a [GetOrganizationRelationshipSettings operation (SOAP)](getorganizationrelationshipsettings-operation-soap.md) operation request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="13f96-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="13f96-124">Text value</span></span>

<span data-ttu-id="13f96-125">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="13f96-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="13f96-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="13f96-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13f96-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="13f96-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="13f96-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="13f96-128">Schema Name</span></span>  <br/> |<span data-ttu-id="13f96-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="13f96-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="13f96-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="13f96-130">Validation File</span></span>  <br/> |<span data-ttu-id="13f96-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="13f96-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="13f96-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="13f96-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="13f96-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="13f96-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13f96-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="13f96-134">See also</span></span>



[<span data-ttu-id="13f96-135">GetOrganizationRelationshipSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="13f96-135">GetOrganizationRelationshipSettingsRequest (SOAP)</span></span>](getorganizationrelationshipsettingsrequest-soap.md)


[<span data-ttu-id="13f96-136">Trabajar con detección automática</span><span class="sxs-lookup"><span data-stu-id="13f96-136">Working with Autodiscover</span></span>](https://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

