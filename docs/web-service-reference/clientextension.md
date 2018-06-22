---
title: ClientExtension
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3445ef2b-1bb1-43ea-bc93-85c72401e5b6
description: El elemento ClientExtension contiene información de usuario y de configuración sobre una aplicación.
ms.openlocfilehash: 5051248a2c8e664d82666bd7b42ee3c3046f43fe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763742"
---
# <a name="clientextension"></a><span data-ttu-id="e2ef1-103">ClientExtension</span><span class="sxs-lookup"><span data-stu-id="e2ef1-103">ClientExtension</span></span>

<span data-ttu-id="e2ef1-104">El elemento **ClientExtension** contiene información de usuario y de configuración sobre una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-104">The **ClientExtension** element contains user and configuration information about an app.</span></span> 
  
```XML
<ClientExtension IsAvailable=" true | false " IsMandatory=" true | false " IsEnabledByDefault=" true | false " Type="" Scope="" MarketplaceAssetId="" MarketplaceContentMarket="" AppStatus="" Etoken="">
    <SpecificUsers></SpecificUsers>
    <Manifest></Manifest>
</ClientExtension>
```

 <span data-ttu-id="e2ef1-105">**ClientExtensionType**</span><span class="sxs-lookup"><span data-stu-id="e2ef1-105">**ClientExtensionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e2ef1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e2ef1-106">Attributes and elements</span></span>

<span data-ttu-id="e2ef1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2ef1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e2ef1-108">Attributes</span></span>

|<span data-ttu-id="e2ef1-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="e2ef1-109">**Attribute**</span></span>|<span data-ttu-id="e2ef1-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e2ef1-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e2ef1-111">IsAvailable</span><span class="sxs-lookup"><span data-stu-id="e2ef1-111">IsAvailable</span></span>  <br/> |<span data-ttu-id="e2ef1-112">Especifica si la aplicación está disponible.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-112">Specifies whether the app is available.</span></span> <span data-ttu-id="e2ef1-113">Un valor de texto de **true** para el atributo **IsAvailable** indica que la aplicación está disponible.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-113">A text value of **true** for the **IsAvailable** attribute indicates that the app is available.</span></span> <span data-ttu-id="e2ef1-114">Un valor de **false** indica que la aplicación no está disponible.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-114">A value of **false** indicates that the app is not available.</span></span> <span data-ttu-id="e2ef1-115">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-115">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="e2ef1-116">IsMandatory</span><span class="sxs-lookup"><span data-stu-id="e2ef1-116">IsMandatory</span></span>  <br/> |<span data-ttu-id="e2ef1-117">Especifica si la aplicación es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-117">Specifies whether the app is mandatory.</span></span> <span data-ttu-id="e2ef1-118">Un valor de texto de **true** para el atributo **IsMandatory** indica que la aplicación es obligatoria para el buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-118">A text value of **true** for the **IsMandatory** attribute indicates that the app is mandatory for the mailbox.</span></span> <span data-ttu-id="e2ef1-119">Un valor de **false** indica que la aplicación no es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-119">A value of **false** indicates that the app is not mandatory.</span></span> <span data-ttu-id="e2ef1-120">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-120">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="e2ef1-121">IsEnabledByDefault</span><span class="sxs-lookup"><span data-stu-id="e2ef1-121">IsEnabledByDefault</span></span>  <br/> |<span data-ttu-id="e2ef1-122">Especifica si la aplicación está habilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-122">Specifies whether the app is enabled by default.</span></span> <span data-ttu-id="e2ef1-123">Un valor de texto de **true** para el atributo **IsEnabledByDefault** indica que la aplicación está habilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-123">A text value of **true** for the **IsEnabledByDefault** attribute indicates that the app is enabled by default.</span></span> <span data-ttu-id="e2ef1-124">Un valor de **false** indica que la aplicación no está habilitada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-124">A value of **false** indicates that the app is not enabled by default.</span></span> <span data-ttu-id="e2ef1-125">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-125">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="e2ef1-126">ProvidedTo</span><span class="sxs-lookup"><span data-stu-id="e2ef1-126">ProvidedTo</span></span>  <br/> |<span data-ttu-id="e2ef1-127">Especifica a quien se proporciona la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-127">Specifies to whom the app is provided.</span></span> <span data-ttu-id="e2ef1-128">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-128">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="e2ef1-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2ef1-129">Type</span></span>  <br/> |<span data-ttu-id="e2ef1-130">Especifica el tipo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-130">Specifies the type of the app.</span></span>  <br/> |
|<span data-ttu-id="e2ef1-131">Ámbito</span><span class="sxs-lookup"><span data-stu-id="e2ef1-131">Scope</span></span>  <br/> |<span data-ttu-id="e2ef1-132">Especifica el ámbito de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-132">Specifies the scope of the app.</span></span>  <br/> |
|<span data-ttu-id="e2ef1-133">MarketplaceAssetId</span><span class="sxs-lookup"><span data-stu-id="e2ef1-133">MarketplaceAssetId</span></span>  <br/> |<span data-ttu-id="e2ef1-134">Especifica el identificador de activo del catálogo de soluciones de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-134">Specifies the marketplace asset identifier of the app.</span></span>  <br/> |
|<span data-ttu-id="e2ef1-135">MarketplaceContentMarket</span><span class="sxs-lookup"><span data-stu-id="e2ef1-135">MarketplaceContentMarket</span></span>  <br/> |<span data-ttu-id="e2ef1-136">Especifica el contenido del catálogo de soluciones que un usuario ve para obtener información detallada y revisa acerca de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-136">Specifies the marketplace content that a user sees for details and reviews about an app.</span></span>  <br/> |
|<span data-ttu-id="e2ef1-137">AppStatus</span><span class="sxs-lookup"><span data-stu-id="e2ef1-137">AppStatus</span></span>  <br/> |<span data-ttu-id="e2ef1-138">Especifica el código de estado de una aplicación de correo en un estado inesperado.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-138">Specifies the status code of a mail app in an unexpected state.</span></span>  <br/> |
|<span data-ttu-id="e2ef1-139">Etoken</span><span class="sxs-lookup"><span data-stu-id="e2ef1-139">Etoken</span></span>  <br/> |<span data-ttu-id="e2ef1-140">Especifica el token de licencia para las aplicaciones de correo de pago o de prueba.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-140">Specifies the license token for paid or trial mail apps.</span></span>  <br/> |
   
#### <a name="type"></a><span data-ttu-id="e2ef1-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2ef1-141">Type</span></span>

|<span data-ttu-id="e2ef1-142">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e2ef1-142">**Value**</span></span>|<span data-ttu-id="e2ef1-143">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e2ef1-143">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e2ef1-144">Default</span><span class="sxs-lookup"><span data-stu-id="e2ef1-144">Default</span></span>  <br/> |<span data-ttu-id="e2ef1-145">Indica que la aplicación está disponible de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-145">Indicates that the app is available by default.</span></span>  <br/> |
|<span data-ttu-id="e2ef1-146">Privado</span><span class="sxs-lookup"><span data-stu-id="e2ef1-146">Private</span></span>  <br/> |<span data-ttu-id="e2ef1-147">Indica que la aplicación es privada.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-147">Indicates that the app is private.</span></span>  <br/> |
|<span data-ttu-id="e2ef1-148">Catálogo de soluciones</span><span class="sxs-lookup"><span data-stu-id="e2ef1-148">MarketPlace</span></span>  <br/> |<span data-ttu-id="e2ef1-149">Indica que la aplicación es una aplicación de catálogo de soluciones.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-149">Indicates that the app is a marketplace app.</span></span>  <br/> |
   
#### <a name="scope"></a><span data-ttu-id="e2ef1-150">Ámbito</span><span class="sxs-lookup"><span data-stu-id="e2ef1-150">Scope</span></span>

|<span data-ttu-id="e2ef1-151">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e2ef1-151">**Value**</span></span>|<span data-ttu-id="e2ef1-152">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e2ef1-152">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e2ef1-153">None</span><span class="sxs-lookup"><span data-stu-id="e2ef1-153">None</span></span>  <br/> |<span data-ttu-id="e2ef1-154">Indica que la aplicación no tiene ningún ámbito.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-154">Indicates that the app has no scope.</span></span>  <br/> |
|<span data-ttu-id="e2ef1-155">User</span><span class="sxs-lookup"><span data-stu-id="e2ef1-155">User</span></span>  <br/> |<span data-ttu-id="e2ef1-156">Indica que la aplicación es por usuario.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-156">Indicates that the app is per user.</span></span>  <br/> |
|<span data-ttu-id="e2ef1-157">Organización</span><span class="sxs-lookup"><span data-stu-id="e2ef1-157">Organization</span></span>  <br/> |<span data-ttu-id="e2ef1-158">Indica que la aplicación es para una organización.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-158">Indicates that the app is for an organization.</span></span>  <br/> |
|<span data-ttu-id="e2ef1-159">Default</span><span class="sxs-lookup"><span data-stu-id="e2ef1-159">Default</span></span>  <br/> |<span data-ttu-id="e2ef1-160">Indica que la aplicación es una aplicación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-160">Indicates that the app is a default app.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e2ef1-161">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e2ef1-161">Child elements</span></span>

|<span data-ttu-id="e2ef1-162">**Element**</span><span class="sxs-lookup"><span data-stu-id="e2ef1-162">**Element**</span></span>|<span data-ttu-id="e2ef1-163">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e2ef1-163">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2ef1-164">SpecificUsers</span><span class="sxs-lookup"><span data-stu-id="e2ef1-164">SpecificUsers</span></span>](specificusers.md) <br/> |<span data-ttu-id="e2ef1-165">Especifica las cuentas de correo electrónico que pueden tener acceso a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-165">Specifies the email accounts that can access the app.</span></span>  <br/> |
|[<span data-ttu-id="e2ef1-166">Manifest</span><span class="sxs-lookup"><span data-stu-id="e2ef1-166">Manifest</span></span>](manifest.md) <br/> |<span data-ttu-id="e2ef1-167">Contiene el archivo de manifiesto de aplicación de base-64 codificada.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-167">Contains the base-64 encoded app manifest file.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e2ef1-168">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e2ef1-168">Parent elements</span></span>

|<span data-ttu-id="e2ef1-169">**Element**</span><span class="sxs-lookup"><span data-stu-id="e2ef1-169">**Element**</span></span>|<span data-ttu-id="e2ef1-170">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e2ef1-170">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2ef1-171">ClientExtensions</span><span class="sxs-lookup"><span data-stu-id="e2ef1-171">ClientExtensions</span></span>](clientextensions.md) <br/> |<span data-ttu-id="e2ef1-172">Especifica una matriz de elementos de **ClientExtension** .</span><span class="sxs-lookup"><span data-stu-id="e2ef1-172">Specifies an array of **ClientExtension** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2ef1-173">Notas</span><span class="sxs-lookup"><span data-stu-id="e2ef1-173">Remarks</span></span>

<span data-ttu-id="e2ef1-174">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-174">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e2ef1-175">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e2ef1-175">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e2ef1-176">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e2ef1-176">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2ef1-177">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e2ef1-177">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e2ef1-178">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e2ef1-178">Schema Name</span></span>  <br/> |<span data-ttu-id="e2ef1-179">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="e2ef1-179">Type schema</span></span>  <br/> |
|<span data-ttu-id="e2ef1-180">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e2ef1-180">Validation File</span></span>  <br/> |<span data-ttu-id="e2ef1-181">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e2ef1-181">types.xsd</span></span>  <br/> |
|<span data-ttu-id="e2ef1-182">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e2ef1-182">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e2ef1-183">Ver también</span><span class="sxs-lookup"><span data-stu-id="e2ef1-183">See also</span></span>



- [<span data-ttu-id="e2ef1-184">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e2ef1-184">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

