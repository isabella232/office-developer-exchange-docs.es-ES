---
title: Request (GetFederationInformation) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: beeb5371-f57b-4346-9753-035dd42c6bee
description: El elemento request representa una solicitud GetFederationInformationRequest (SOAP).
ms.openlocfilehash: dbd88537d03f6325cf0025d08c63ae486544d705
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459584"
---
# <a name="request-getfederationinformation-soap"></a><span data-ttu-id="dabdf-103">Request (GetFederationInformation) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dabdf-103">Request (GetFederationInformation) (SOAP)</span></span>

<span data-ttu-id="dabdf-104">El elemento **request** representa una solicitud [GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="dabdf-104">The **Request** element represents a [GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md) request.</span></span> 
  
```XML
<Request>
   <Domain/>
</Request>
```

 <span data-ttu-id="dabdf-105">**GetFederationInformationRequest**</span><span class="sxs-lookup"><span data-stu-id="dabdf-105">**GetFederationInformationRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dabdf-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dabdf-106">Attributes and elements</span></span>

<span data-ttu-id="dabdf-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dabdf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dabdf-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="dabdf-108">Attributes</span></span>

<span data-ttu-id="dabdf-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="dabdf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dabdf-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dabdf-110">Child elements</span></span>

|<span data-ttu-id="dabdf-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dabdf-111">**Element**</span></span>|<span data-ttu-id="dabdf-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dabdf-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dabdf-113">Dominio (GetFederationInformation) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dabdf-113">Domain (GetFederationInformation) (SOAP)</span></span>](domain-getfederationinformationsoap.md) <br/> |<span data-ttu-id="dabdf-114">Identifica el dominio que tiene una confianza de Federación.</span><span class="sxs-lookup"><span data-stu-id="dabdf-114">Identifies the domain that has a federation trust.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dabdf-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dabdf-115">Parent elements</span></span>

|<span data-ttu-id="dabdf-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dabdf-116">**Element**</span></span>|<span data-ttu-id="dabdf-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dabdf-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dabdf-118">GetFederationInformationRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dabdf-118">GetFederationInformationRequestMessage (SOAP)</span></span>](getfederationinformationrequestmessage-soap.md) <br/> |<span data-ttu-id="dabdf-119">Prepara una llamada al servidor para solicitar datos de configuración para el servicio de token de seguridad (STS).</span><span class="sxs-lookup"><span data-stu-id="dabdf-119">Prepares a call to the server to request configuration data for the security token service (STS).</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="dabdf-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dabdf-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dabdf-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="dabdf-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="dabdf-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dabdf-122">Schema Name</span></span>  <br/> |<span data-ttu-id="dabdf-123">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="dabdf-123">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="dabdf-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dabdf-124">Validation File</span></span>  <br/> |<span data-ttu-id="dabdf-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="dabdf-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dabdf-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dabdf-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="dabdf-127">Verdadero</span><span class="sxs-lookup"><span data-stu-id="dabdf-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dabdf-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="dabdf-128">See also</span></span>



[<span data-ttu-id="dabdf-129">Trabajar con detección automática</span><span class="sxs-lookup"><span data-stu-id="dabdf-129">Working with Autodiscover</span></span>](https://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

