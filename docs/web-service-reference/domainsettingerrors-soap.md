---
title: DomainSettingErrors (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a4ce19de-f560-4984-8047-ecbbc86c9b91
description: El elemento DomainSettingsErrors contiene información de error de configuración que no se pudo devolver.
ms.openlocfilehash: 6ecd23bc556ca32d724581a28cc7c117c6853207
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764281"
---
# <a name="domainsettingerrors-soap"></a><span data-ttu-id="bcd52-103">DomainSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bcd52-103">DomainSettingErrors (SOAP)</span></span>

<span data-ttu-id="bcd52-104">El elemento **DomainSettingsErrors** contiene información de error de configuración que no se pudo devolver.</span><span class="sxs-lookup"><span data-stu-id="bcd52-104">The **DomainSettingsErrors** element contains error information for settings that could not be returned.</span></span> 
  
```XML
<DomainSettingsErrors>
   <DomainSettingsError/>
</DomainSettingsErrors>
```

 <span data-ttu-id="bcd52-105">**DomainSettingsErrors**</span><span class="sxs-lookup"><span data-stu-id="bcd52-105">**DomainSettingsErrors**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bcd52-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bcd52-106">Attributes and elements</span></span>

<span data-ttu-id="bcd52-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bcd52-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bcd52-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="bcd52-108">Attributes</span></span>

<span data-ttu-id="bcd52-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bcd52-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bcd52-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bcd52-110">Child elements</span></span>

|<span data-ttu-id="bcd52-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="bcd52-111">**Element**</span></span>|<span data-ttu-id="bcd52-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bcd52-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bcd52-113">DomainSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bcd52-113">DomainSettingError (SOAP)</span></span>](domainsettingerror-soap.md) <br/> |<span data-ttu-id="bcd52-114">Representa un error que se produjo durante la recuperación de una configuración de dominio.</span><span class="sxs-lookup"><span data-stu-id="bcd52-114">Represents an error that occurred while retrieving a domain setting.</span></span> <span data-ttu-id="bcd52-115">Esto representa un error de una solicitud de operación de la [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="bcd52-115">This represents an error from a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) operation request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="bcd52-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bcd52-116">Parent elements</span></span>

|<span data-ttu-id="bcd52-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="bcd52-117">**Element**</span></span>|<span data-ttu-id="bcd52-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bcd52-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bcd52-119">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bcd52-119">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="bcd52-120">Contiene la configuración solicitada para el dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="bcd52-120">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bcd52-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="bcd52-121">Text value</span></span>

<span data-ttu-id="bcd52-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bcd52-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bcd52-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bcd52-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bcd52-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bcd52-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="bcd52-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bcd52-125">Schema Name</span></span>  <br/> |<span data-ttu-id="bcd52-126">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="bcd52-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="bcd52-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bcd52-127">Validation File</span></span>  <br/> |<span data-ttu-id="bcd52-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bcd52-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bcd52-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bcd52-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="bcd52-130">Verdadero</span><span class="sxs-lookup"><span data-stu-id="bcd52-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bcd52-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcd52-131">See also</span></span>

- [<span data-ttu-id="bcd52-132">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="bcd52-132">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

