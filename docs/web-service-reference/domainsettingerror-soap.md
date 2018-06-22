---
title: DomainSettingError (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 48c3f7b5-2ee0-42ce-97a1-a881e2f60327
description: El elemento DomainSettingError representa un error que se produjo durante la recuperación de una configuración de dominio. Esto representa un error de una solicitud de GetDomainSettings.
ms.openlocfilehash: 08b0a47acea8d35ec78efd701168a251771effac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764274"
---
# <a name="domainsettingerror-soap"></a><span data-ttu-id="34623-104">DomainSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="34623-104">DomainSettingError (SOAP)</span></span>

<span data-ttu-id="34623-105">El elemento **DomainSettingError** representa un error que se produjo durante la recuperación de una configuración de dominio.</span><span class="sxs-lookup"><span data-stu-id="34623-105">The **DomainSettingError** element represents an error that occurred while retrieving a domain setting.</span></span> <span data-ttu-id="34623-106">Esto representa un error de una solicitud de **GetDomainSettings** .</span><span class="sxs-lookup"><span data-stu-id="34623-106">This represents an error from a **GetDomainSettings** request.</span></span> 
  
```XML
<DomainSettingError>
   <ErrorCode/>
   <ErrorMessage/>
   <SettingName/>
</DomainSettingError>
```

 <span data-ttu-id="34623-107">**DomainSettingError**</span><span class="sxs-lookup"><span data-stu-id="34623-107">**DomainSettingError**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="34623-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="34623-108">Attributes and elements</span></span>

<span data-ttu-id="34623-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="34623-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="34623-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="34623-110">Attributes</span></span>

<span data-ttu-id="34623-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="34623-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="34623-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="34623-112">Child elements</span></span>

|<span data-ttu-id="34623-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="34623-113">**Element**</span></span>|<span data-ttu-id="34623-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="34623-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="34623-115">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="34623-115">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="34623-116">Identifica el código de error que está asociado a la solicitud específico.</span><span class="sxs-lookup"><span data-stu-id="34623-116">Identifies the error code that is associated with the specific request.</span></span>  <br/> |
|[<span data-ttu-id="34623-117">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="34623-117">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="34623-118">Contiene el mensaje de error que está asociado a la solicitud específico.</span><span class="sxs-lookup"><span data-stu-id="34623-118">Contains the error message that is associated with the specific request.</span></span>  <br/> |
|[<span data-ttu-id="34623-119">NombreDeOpción (SOAP)</span><span class="sxs-lookup"><span data-stu-id="34623-119">SettingName (SOAP)</span></span>](settingname-soap.md) <br/> |<span data-ttu-id="34623-120">Representa el nombre de la configuración.</span><span class="sxs-lookup"><span data-stu-id="34623-120">Represents the name of the setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="34623-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="34623-121">Parent elements</span></span>

|<span data-ttu-id="34623-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="34623-122">**Element**</span></span>|<span data-ttu-id="34623-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="34623-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="34623-124">DomainSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="34623-124">DomainSettingErrors (SOAP)</span></span>](domainsettingerrors-soap.md) <br/> |<span data-ttu-id="34623-125">Contiene información de error de configuración que no se pudo devolver.</span><span class="sxs-lookup"><span data-stu-id="34623-125">Contains error information for settings that could not be returned.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="34623-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="34623-126">Text value</span></span>

<span data-ttu-id="34623-127">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="34623-127">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="34623-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="34623-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34623-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="34623-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="34623-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="34623-130">Schema Name</span></span>  <br/> |<span data-ttu-id="34623-131">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="34623-131">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="34623-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="34623-132">Validation File</span></span>  <br/> |<span data-ttu-id="34623-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="34623-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="34623-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="34623-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="34623-135">Verdadero</span><span class="sxs-lookup"><span data-stu-id="34623-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="34623-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="34623-136">See also</span></span>

- [<span data-ttu-id="34623-137">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="34623-137">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

