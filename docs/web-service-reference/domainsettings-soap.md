---
title: DomainSettings (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f3d37f5a-c9ea-4ed9-a011-94d33bda64d1
description: El elemento DomainSettings representa la configuración de dominio que se ha enviado en una solicitud de detección automática o devuelta por una respuesta de detección automática.
ms.openlocfilehash: 67e3753b0cf5c7c653664ff087f697ce7ae2b7a4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530701"
---
# <a name="domainsettings-soap"></a><span data-ttu-id="3a5bb-103">DomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3a5bb-103">DomainSettings (SOAP)</span></span>

<span data-ttu-id="3a5bb-104">El elemento **DomainSettings** representa la configuración de dominio que se ha enviado en una solicitud de detección automática o devuelta por una respuesta de detección automática.</span><span class="sxs-lookup"><span data-stu-id="3a5bb-104">The **DomainSettings** element represents the domain settings that were submitted in an Autodiscover request or returned by an Autodiscover response.</span></span> 
  
```XML
<DomainSettings>
   <DomainSetting/>
</DomainSettings>
```

 <span data-ttu-id="3a5bb-105">**DomainSettings**</span><span class="sxs-lookup"><span data-stu-id="3a5bb-105">**DomainSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3a5bb-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3a5bb-106">Attributes and elements</span></span>

<span data-ttu-id="3a5bb-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3a5bb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a5bb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3a5bb-108">Attributes</span></span>

<span data-ttu-id="3a5bb-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3a5bb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3a5bb-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3a5bb-110">Child elements</span></span>

|<span data-ttu-id="3a5bb-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3a5bb-111">**Element**</span></span>|<span data-ttu-id="3a5bb-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a5bb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a5bb-113">DomainSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3a5bb-113">DomainSetting (SOAP)</span></span>](domainsetting-soap.md) <br/> |<span data-ttu-id="3a5bb-114">Contiene la configuración de dominio devuelta por una solicitud de [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="3a5bb-114">Contains domain settings that are returned by a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3a5bb-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3a5bb-115">Parent elements</span></span>

|<span data-ttu-id="3a5bb-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3a5bb-116">**Element**</span></span>|<span data-ttu-id="3a5bb-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a5bb-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a5bb-118">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3a5bb-118">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="3a5bb-119">Contiene la configuración solicitada para el dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="3a5bb-119">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3a5bb-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="3a5bb-120">Text value</span></span>

<span data-ttu-id="3a5bb-121">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3a5bb-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a5bb-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3a5bb-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a5bb-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a5bb-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="3a5bb-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3a5bb-124">Schema Name</span></span>  <br/> |<span data-ttu-id="3a5bb-125">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="3a5bb-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="3a5bb-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3a5bb-126">Validation File</span></span>  <br/> |<span data-ttu-id="3a5bb-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="3a5bb-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3a5bb-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3a5bb-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="3a5bb-129">Verdadero</span><span class="sxs-lookup"><span data-stu-id="3a5bb-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a5bb-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a5bb-130">See also</span></span>

- [<span data-ttu-id="3a5bb-131">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="3a5bb-131">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

