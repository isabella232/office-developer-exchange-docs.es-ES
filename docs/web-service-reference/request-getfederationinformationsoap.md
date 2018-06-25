---
title: Solicitud (SOAP) (GetFederationInformation)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: beeb5371-f57b-4346-9753-035dd42c6bee
description: El elemento de solicitud representa una solicitud de GetFederationInformationRequest (SOAP).
ms.openlocfilehash: 0fb9301c2f318aa2c27155675dd3c43b41aabecd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837119"
---
# <a name="request-getfederationinformation-soap"></a><span data-ttu-id="f28dc-103">Solicitud (SOAP) (GetFederationInformation)</span><span class="sxs-lookup"><span data-stu-id="f28dc-103">Request (GetFederationInformation) (SOAP)</span></span>

<span data-ttu-id="f28dc-104">El elemento de **solicitud** representa una solicitud de [GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="f28dc-104">The **Request** element represents a [GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md) request.</span></span> 
  
```XML
<Request>
   <Domain/>
</Request>
```

 <span data-ttu-id="f28dc-105">**GetFederationInformationRequest**</span><span class="sxs-lookup"><span data-stu-id="f28dc-105">**GetFederationInformationRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f28dc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f28dc-106">Attributes and elements</span></span>

<span data-ttu-id="f28dc-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f28dc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f28dc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f28dc-108">Attributes</span></span>

<span data-ttu-id="f28dc-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f28dc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f28dc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f28dc-110">Child elements</span></span>

|<span data-ttu-id="f28dc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f28dc-111">**Element**</span></span>|<span data-ttu-id="f28dc-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f28dc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f28dc-113">Dominio (GetFederationInformation) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f28dc-113">Domain (GetFederationInformation) (SOAP)</span></span>](domain-getfederationinformationsoap.md) <br/> |<span data-ttu-id="f28dc-114">Identifica el dominio que tiene una confianza de federación.</span><span class="sxs-lookup"><span data-stu-id="f28dc-114">Identifies the domain that has a federation trust.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f28dc-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f28dc-115">Parent elements</span></span>

|<span data-ttu-id="f28dc-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="f28dc-116">**Element**</span></span>|<span data-ttu-id="f28dc-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f28dc-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f28dc-118">GetFederationInformationRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="f28dc-118">GetFederationInformationRequestMessage (SOAP)</span></span>](getfederationinformationrequestmessage-soap.md) <br/> |<span data-ttu-id="f28dc-119">Prepara una llamada al servidor para solicitar los datos de configuración para el servicio de token de seguridad (STS).</span><span class="sxs-lookup"><span data-stu-id="f28dc-119">Prepares a call to the server to request configuration data for the security token service (STS).</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="f28dc-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f28dc-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f28dc-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f28dc-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="f28dc-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f28dc-122">Schema Name</span></span>  <br/> |<span data-ttu-id="f28dc-123">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="f28dc-123">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="f28dc-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f28dc-124">Validation File</span></span>  <br/> |<span data-ttu-id="f28dc-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f28dc-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f28dc-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f28dc-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="f28dc-127">Verdadero</span><span class="sxs-lookup"><span data-stu-id="f28dc-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f28dc-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f28dc-128">See also</span></span>



[<span data-ttu-id="f28dc-129">Trabajar con detección automática</span><span class="sxs-lookup"><span data-stu-id="f28dc-129">Working with Autodiscover</span></span>](http://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

