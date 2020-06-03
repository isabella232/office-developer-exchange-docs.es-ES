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
description: El elemento DomainSettingsErrors contiene información de error para las opciones de configuración que no se pudieron devolver.
ms.openlocfilehash: 4e7ee29c2bc680a1938b75189c2ac3c214f7d2b5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530708"
---
# <a name="domainsettingerrors-soap"></a><span data-ttu-id="9df33-103">DomainSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9df33-103">DomainSettingErrors (SOAP)</span></span>

<span data-ttu-id="9df33-104">El elemento **DomainSettingsErrors** contiene información de error para las opciones de configuración que no se pudieron devolver.</span><span class="sxs-lookup"><span data-stu-id="9df33-104">The **DomainSettingsErrors** element contains error information for settings that could not be returned.</span></span> 
  
```XML
<DomainSettingsErrors>
   <DomainSettingsError/>
</DomainSettingsErrors>
```

 <span data-ttu-id="9df33-105">**DomainSettingsErrors**</span><span class="sxs-lookup"><span data-stu-id="9df33-105">**DomainSettingsErrors**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9df33-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9df33-106">Attributes and elements</span></span>

<span data-ttu-id="9df33-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9df33-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9df33-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9df33-108">Attributes</span></span>

<span data-ttu-id="9df33-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9df33-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9df33-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9df33-110">Child elements</span></span>

|<span data-ttu-id="9df33-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9df33-111">**Element**</span></span>|<span data-ttu-id="9df33-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9df33-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9df33-113">DomainSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9df33-113">DomainSettingError (SOAP)</span></span>](domainsettingerror-soap.md) <br/> |<span data-ttu-id="9df33-114">Representa un error que se produjo al recuperar una configuración de dominio.</span><span class="sxs-lookup"><span data-stu-id="9df33-114">Represents an error that occurred while retrieving a domain setting.</span></span> <span data-ttu-id="9df33-115">Esto representa un error de una solicitud de operación de [GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="9df33-115">This represents an error from a [GetDomainSettings operation (SOAP)](getdomainsettings-operation-soap.md) operation request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9df33-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9df33-116">Parent elements</span></span>

|<span data-ttu-id="9df33-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9df33-117">**Element**</span></span>|<span data-ttu-id="9df33-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9df33-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9df33-119">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9df33-119">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="9df33-120">Contiene la configuración solicitada para el dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="9df33-120">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9df33-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9df33-121">Text value</span></span>

<span data-ttu-id="9df33-122">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9df33-122">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9df33-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9df33-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9df33-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="9df33-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="9df33-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9df33-125">Schema Name</span></span>  <br/> |<span data-ttu-id="9df33-126">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="9df33-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="9df33-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9df33-127">Validation File</span></span>  <br/> |<span data-ttu-id="9df33-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="9df33-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9df33-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9df33-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="9df33-130">Verdadero</span><span class="sxs-lookup"><span data-stu-id="9df33-130">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9df33-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="9df33-131">See also</span></span>

- [<span data-ttu-id="9df33-132">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9df33-132">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

