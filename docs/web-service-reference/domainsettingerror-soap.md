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
description: El elemento DomainSettingError representa un error que se produjo al recuperar una configuración de dominio. Esto representa un error de una solicitud GetDomainSettings.
ms.openlocfilehash: 189a614e7629033c8db2f60b8fd3679835a696ed
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530715"
---
# <a name="domainsettingerror-soap"></a><span data-ttu-id="90879-104">DomainSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="90879-104">DomainSettingError (SOAP)</span></span>

<span data-ttu-id="90879-105">El elemento **DomainSettingError** representa un error que se produjo al recuperar una configuración de dominio.</span><span class="sxs-lookup"><span data-stu-id="90879-105">The **DomainSettingError** element represents an error that occurred while retrieving a domain setting.</span></span> <span data-ttu-id="90879-106">Esto representa un error de una solicitud **GetDomainSettings** .</span><span class="sxs-lookup"><span data-stu-id="90879-106">This represents an error from a **GetDomainSettings** request.</span></span> 
  
```XML
<DomainSettingError>
   <ErrorCode/>
   <ErrorMessage/>
   <SettingName/>
</DomainSettingError>
```

 <span data-ttu-id="90879-107">**DomainSettingError**</span><span class="sxs-lookup"><span data-stu-id="90879-107">**DomainSettingError**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="90879-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="90879-108">Attributes and elements</span></span>

<span data-ttu-id="90879-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="90879-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="90879-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="90879-110">Attributes</span></span>

<span data-ttu-id="90879-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="90879-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="90879-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="90879-112">Child elements</span></span>

|<span data-ttu-id="90879-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="90879-113">**Element**</span></span>|<span data-ttu-id="90879-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90879-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90879-115">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="90879-115">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="90879-116">Identifica el código de error que está asociado con la solicitud específica.</span><span class="sxs-lookup"><span data-stu-id="90879-116">Identifies the error code that is associated with the specific request.</span></span>  <br/> |
|[<span data-ttu-id="90879-117">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="90879-117">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="90879-118">Contiene el mensaje de error que está asociado con la solicitud específica.</span><span class="sxs-lookup"><span data-stu-id="90879-118">Contains the error message that is associated with the specific request.</span></span>  <br/> |
|[<span data-ttu-id="90879-119">SettingName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="90879-119">SettingName (SOAP)</span></span>](settingname-soap.md) <br/> |<span data-ttu-id="90879-120">Representa el nombre de la configuración.</span><span class="sxs-lookup"><span data-stu-id="90879-120">Represents the name of the setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="90879-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="90879-121">Parent elements</span></span>

|<span data-ttu-id="90879-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="90879-122">**Element**</span></span>|<span data-ttu-id="90879-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90879-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90879-124">DomainSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="90879-124">DomainSettingErrors (SOAP)</span></span>](domainsettingerrors-soap.md) <br/> |<span data-ttu-id="90879-125">Contiene información de error de la configuración que no se pudo devolver.</span><span class="sxs-lookup"><span data-stu-id="90879-125">Contains error information for settings that could not be returned.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="90879-126">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="90879-126">Text value</span></span>

<span data-ttu-id="90879-127">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="90879-127">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="90879-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="90879-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="90879-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="90879-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="90879-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="90879-130">Schema Name</span></span>  <br/> |<span data-ttu-id="90879-131">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="90879-131">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="90879-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="90879-132">Validation File</span></span>  <br/> |<span data-ttu-id="90879-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="90879-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="90879-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="90879-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="90879-135">Verdadero</span><span class="sxs-lookup"><span data-stu-id="90879-135">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="90879-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="90879-136">See also</span></span>

- [<span data-ttu-id="90879-137">Operación GetDomainSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="90879-137">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)

