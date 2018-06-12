---
title: GetDomainSettingsRequest (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5ac0ff6d-9e02-4e4c-973d-cd9e076661d5
description: El elemento GetDomainSettingsRequest representa una solicitud de operación GetDomainSettings operación (SOAP).
ms.openlocfilehash: 4de525a9ba47a0d9afb0d6db9200fe32845f31d0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764813"
---
# <a name="getdomainsettingsrequest-soap"></a><span data-ttu-id="4c386-103">GetDomainSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4c386-103">GetDomainSettingsRequest (SOAP)</span></span>

<span data-ttu-id="4c386-104">El elemento **GetDomainSettingsRequest** representa una solicitud de operación de la [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="4c386-104">The **GetDomainSettingsRequest** element represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) operation request.</span></span> 
  
```XML
<GetDomainSettingsRequest>
   <Domains/>
   <RequestedSettings/>
   <RequestedVersion/>
</GetDomainSettingsRequest>
```

 <span data-ttu-id="4c386-105">**GetDomainSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="4c386-105">**GetDomainSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4c386-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4c386-106">Attributes and elements</span></span>

<span data-ttu-id="4c386-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4c386-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c386-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4c386-108">Attributes</span></span>

<span data-ttu-id="4c386-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4c386-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4c386-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4c386-110">Child elements</span></span>

|<span data-ttu-id="4c386-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4c386-111">**Element**</span></span>|<span data-ttu-id="4c386-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4c386-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4c386-113">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4c386-113">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="4c386-114">Representa una colección de identificadores de dominio.</span><span class="sxs-lookup"><span data-stu-id="4c386-114">Represents a collection of domain identifiers.</span></span>  <br/> |
|[<span data-ttu-id="4c386-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4c386-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="4c386-116">Contiene los nombres de las opciones de configuración de dominio solicitado.</span><span class="sxs-lookup"><span data-stu-id="4c386-116">Contains the names of the requested domain configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="4c386-117">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4c386-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="4c386-118">Especifica la versión del servidor que va a usar el proveedor.</span><span class="sxs-lookup"><span data-stu-id="4c386-118">Specifies the server version that the provider will use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4c386-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4c386-119">Parent elements</span></span>

<span data-ttu-id="4c386-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4c386-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="4c386-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4c386-121">Text value</span></span>

<span data-ttu-id="4c386-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4c386-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4c386-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4c386-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c386-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4c386-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="4c386-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4c386-125">Schema Name</span></span>  <br/> |<span data-ttu-id="4c386-126">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="4c386-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="4c386-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4c386-127">Validation File</span></span>  <br/> |<span data-ttu-id="4c386-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4c386-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4c386-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4c386-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="4c386-130">Verdadero</span><span class="sxs-lookup"><span data-stu-id="4c386-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4c386-131">Ver también</span><span class="sxs-lookup"><span data-stu-id="4c386-131">See also</span></span>



[<span data-ttu-id="4c386-132">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4c386-132">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

