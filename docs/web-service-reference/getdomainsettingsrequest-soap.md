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
description: El elemento GetDomainSettingsRequest representa una solicitud de operación de GetDomainSettings (SOAP).
ms.openlocfilehash: 400016d0817131fb70ec7ff3db7fbfdc1b51f8f9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460963"
---
# <a name="getdomainsettingsrequest-soap"></a><span data-ttu-id="7177a-103">GetDomainSettingsRequest (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7177a-103">GetDomainSettingsRequest (SOAP)</span></span>

<span data-ttu-id="7177a-104">El elemento **GetDomainSettingsRequest** representa una solicitud de operación de [GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="7177a-104">The **GetDomainSettingsRequest** element represents a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) operation request.</span></span> 
  
```XML
<GetDomainSettingsRequest>
   <Domains/>
   <RequestedSettings/>
   <RequestedVersion/>
</GetDomainSettingsRequest>
```

 <span data-ttu-id="7177a-105">**GetDomainSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="7177a-105">**GetDomainSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7177a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7177a-106">Attributes and elements</span></span>

<span data-ttu-id="7177a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7177a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7177a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7177a-108">Attributes</span></span>

<span data-ttu-id="7177a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7177a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7177a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7177a-110">Child elements</span></span>

|<span data-ttu-id="7177a-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7177a-111">**Element**</span></span>|<span data-ttu-id="7177a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7177a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7177a-113">Dominios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7177a-113">Domains (SOAP)</span></span>](domains-soap.md) <br/> |<span data-ttu-id="7177a-114">Representa una colección de identificadores de dominio.</span><span class="sxs-lookup"><span data-stu-id="7177a-114">Represents a collection of domain identifiers.</span></span>  <br/> |
|[<span data-ttu-id="7177a-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7177a-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="7177a-116">Contiene los nombres de las opciones de configuración de dominio solicitadas.</span><span class="sxs-lookup"><span data-stu-id="7177a-116">Contains the names of the requested domain configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="7177a-117">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7177a-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="7177a-118">Especifica la versión del servidor que usará el proveedor.</span><span class="sxs-lookup"><span data-stu-id="7177a-118">Specifies the server version that the provider will use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7177a-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7177a-119">Parent elements</span></span>

<span data-ttu-id="7177a-120">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7177a-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="7177a-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7177a-121">Text value</span></span>

<span data-ttu-id="7177a-122">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7177a-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7177a-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7177a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7177a-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="7177a-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="7177a-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7177a-125">Schema Name</span></span>  <br/> |<span data-ttu-id="7177a-126">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="7177a-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="7177a-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7177a-127">Validation File</span></span>  <br/> |<span data-ttu-id="7177a-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="7177a-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7177a-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7177a-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="7177a-130">Verdadero</span><span class="sxs-lookup"><span data-stu-id="7177a-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7177a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="7177a-131">See also</span></span>



[<span data-ttu-id="7177a-132">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7177a-132">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

