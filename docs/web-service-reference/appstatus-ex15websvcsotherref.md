---
title: AppStatus
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f3ab8bf1-abc5-45cf-a2e1-d7602f2c24ec
description: El valor del elemento AppStatus indica el estado de la aplicación de correo.
ms.openlocfilehash: d833947fd62d500418f257829d241a2e0b3bca9c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464780"
---
# <a name="appstatus"></a><span data-ttu-id="a19c1-103">AppStatus</span><span class="sxs-lookup"><span data-stu-id="a19c1-103">AppStatus</span></span>

<span data-ttu-id="a19c1-104">El valor del elemento **AppStatus** indica el estado de la aplicación de correo.</span><span class="sxs-lookup"><span data-stu-id="a19c1-104">The **AppStatus** element value indicates the status of the mail app.</span></span> 
  
```XML
<AppStatus/>
```

 <span data-ttu-id="a19c1-105">**string**</span><span class="sxs-lookup"><span data-stu-id="a19c1-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a19c1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a19c1-106">Attributes and elements</span></span>

<span data-ttu-id="a19c1-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a19c1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a19c1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a19c1-108">Attributes</span></span>

<span data-ttu-id="a19c1-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a19c1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a19c1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a19c1-110">Child elements</span></span>

<span data-ttu-id="a19c1-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a19c1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a19c1-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a19c1-112">Parent elements</span></span>

[<span data-ttu-id="a19c1-113">Metadatos</span><span class="sxs-lookup"><span data-stu-id="a19c1-113">Metadata</span></span>](metadata-ex15websvcsotherref.md)
  
## <a name="text-value"></a><span data-ttu-id="a19c1-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a19c1-114">Text value</span></span>

<span data-ttu-id="a19c1-115">El valor de texto del elemento **AppStatus** indica el estado de la aplicación de correo.</span><span class="sxs-lookup"><span data-stu-id="a19c1-115">The text value of the **AppStatus** element indicates the status of the mail app.</span></span> <span data-ttu-id="a19c1-116">Si el usuario puede corregir un problema relacionado con el estado de la aplicación de correo, el elemento [ActionUrl](actionurl.md) proporciona la dirección URL para realizar la corrección.</span><span class="sxs-lookup"><span data-stu-id="a19c1-116">If the user can fix an issue related to the status of the mail app, the [ActionUrl](actionurl.md) element provides the URL to perform the fix.</span></span> 
  
<span data-ttu-id="a19c1-117">**Tabla 1. Valores de AppStatus**</span><span class="sxs-lookup"><span data-stu-id="a19c1-117">**Table 1. AppStatus values**</span></span>

|<span data-ttu-id="a19c1-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a19c1-118">**Value**</span></span>|<span data-ttu-id="a19c1-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a19c1-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a19c1-120">Null o 0</span><span class="sxs-lookup"><span data-stu-id="a19c1-120">Null or 0</span></span>  <br/> |<span data-ttu-id="a19c1-121">La aplicación de correo tiene un estado correcto.</span><span class="sxs-lookup"><span data-stu-id="a19c1-121">The mail app has a healthy status.</span></span>  <br/> |
|<span data-ttu-id="a19c1-122">1.0</span><span class="sxs-lookup"><span data-stu-id="a19c1-122">1.0</span></span>  <br/> |<span data-ttu-id="a19c1-123">La aplicación de correo no se pudo actualizar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a19c1-123">The mail app could not be automatically updated.</span></span> <span data-ttu-id="a19c1-124">La aplicación de correo debe volver a instalarse desde la tienda Office.</span><span class="sxs-lookup"><span data-stu-id="a19c1-124">The mail app needs to be re-installed from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="a19c1-125">1.1</span><span class="sxs-lookup"><span data-stu-id="a19c1-125">1.1</span></span>  <br/> |<span data-ttu-id="a19c1-126">La aplicación de correo no se pudo actualizar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a19c1-126">The mail app could not be automatically updated.</span></span> <span data-ttu-id="a19c1-127">La aplicación de correo requiere mayor cantidad de permisos y esto requiere la revisión y la confirmación de la instalación.</span><span class="sxs-lookup"><span data-stu-id="a19c1-127">The mail app requires increased permissions, and this requires your review and confirmation to install.</span></span>  <br/> |
|<span data-ttu-id="a19c1-128">1.2</span><span class="sxs-lookup"><span data-stu-id="a19c1-128">1.2</span></span>  <br/> |<span data-ttu-id="a19c1-129">La aplicación de correo no se pudo actualizar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a19c1-129">The mail app couldn't be updated automatically.</span></span> <span data-ttu-id="a19c1-130">La licencia actual ha expirado o no es válida.</span><span class="sxs-lookup"><span data-stu-id="a19c1-130">The current license has expired or is invalid.</span></span> <span data-ttu-id="a19c1-131">Actualice la aplicación de correo desde la tienda Office.</span><span class="sxs-lookup"><span data-stu-id="a19c1-131">Please update the mail app from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="a19c1-132">2.0</span><span class="sxs-lookup"><span data-stu-id="a19c1-132">2.0</span></span>  <br/> |<span data-ttu-id="a19c1-133">La licencia de la aplicación de correo no se pudo actualizar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a19c1-133">The mail app license could not be automatically updated.</span></span> <span data-ttu-id="a19c1-134">La licencia de la aplicación de correo debe recuperarse de la tienda Office.</span><span class="sxs-lookup"><span data-stu-id="a19c1-134">The license for the mail app needs to be recovered from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="a19c1-135">2.1</span><span class="sxs-lookup"><span data-stu-id="a19c1-135">2.1</span></span>  <br/> |<span data-ttu-id="a19c1-136">La licencia de la aplicación de correo no se pudo actualizar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="a19c1-136">The mail app license could not be automatically updated.</span></span> <span data-ttu-id="a19c1-137">La licencia actual ha expirado.</span><span class="sxs-lookup"><span data-stu-id="a19c1-137">The current license has expired.</span></span> <span data-ttu-id="a19c1-138">Se debe instalar una nueva licencia para esta aplicación desde la tienda Office.</span><span class="sxs-lookup"><span data-stu-id="a19c1-138">A new license for this app needs to be installed from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="a19c1-139">3,0</span><span class="sxs-lookup"><span data-stu-id="a19c1-139">3.0</span></span>  <br/> |<span data-ttu-id="a19c1-140">El estado de la tienda Office de la aplicación de correo ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="a19c1-140">The Office Store status for the mail app has changed.</span></span> <span data-ttu-id="a19c1-141">Esto puede indicar que hay un problema con la aplicación de correo.</span><span class="sxs-lookup"><span data-stu-id="a19c1-141">This may indicate that there is a problem with the mail app.</span></span> <span data-ttu-id="a19c1-142">Vaya a la página de la aplicación de correo en la tienda Office para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="a19c1-142">Go to the mail app page in the Office Store for more information.</span></span>  <br/> |
|<span data-ttu-id="a19c1-143">3.1</span><span class="sxs-lookup"><span data-stu-id="a19c1-143">3.1</span></span>  <br/> |<span data-ttu-id="a19c1-144">La aplicación de correo se ha quitado de la tienda Office.</span><span class="sxs-lookup"><span data-stu-id="a19c1-144">The mail app has been removed from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="a19c1-145">3.2</span><span class="sxs-lookup"><span data-stu-id="a19c1-145">3.2</span></span>  <br/> |<span data-ttu-id="a19c1-146">Se ha detectado un problema con la aplicación de correo y se ha retirado temporalmente de la tienda Office.</span><span class="sxs-lookup"><span data-stu-id="a19c1-146">A problem has been discovered with the mail app and it has temporarily been withdrawn from the Office Store.</span></span>  <br/> |
|<span data-ttu-id="a19c1-147">3.3</span><span class="sxs-lookup"><span data-stu-id="a19c1-147">3.3</span></span>  <br/> |<span data-ttu-id="a19c1-148">La aplicación de correo se quitará de la tienda Office en un plazo de 30 días.</span><span class="sxs-lookup"><span data-stu-id="a19c1-148">The mail app will be removed from the Office Store within 30 days.</span></span>  <br/> |
|<span data-ttu-id="a19c1-149">4,0</span><span class="sxs-lookup"><span data-stu-id="a19c1-149">4.0</span></span>  <br/> |<span data-ttu-id="a19c1-150">El cliente de correo ha deshabilitado automáticamente la aplicación de correo.</span><span class="sxs-lookup"><span data-stu-id="a19c1-150">The mail app has been automatically disabled by your mail client.</span></span>  <br/> |
|<span data-ttu-id="a19c1-151">4.1</span><span class="sxs-lookup"><span data-stu-id="a19c1-151">4.1</span></span>  <br/> |<span data-ttu-id="a19c1-152">Outlook ha deshabilitado la aplicación de correo por motivos de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="a19c1-152">The mail app has been disabled by Outlook for performance reasons.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a19c1-153">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a19c1-153">Remarks</span></span>

<span data-ttu-id="a19c1-154">Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a19c1-154">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="a19c1-155">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="a19c1-155">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a19c1-156">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a19c1-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a19c1-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="a19c1-157">Namespace</span></span>  <br/> | https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a19c1-158">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a19c1-158">Schema Name</span></span>  <br/> |<span data-ttu-id="a19c1-159">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a19c1-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="a19c1-160">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a19c1-160">Validation File</span></span>  <br/> |<span data-ttu-id="a19c1-161">No aplicable</span><span class="sxs-lookup"><span data-stu-id="a19c1-161">Not applicable</span></span>  <br/> |
|<span data-ttu-id="a19c1-162">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a19c1-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="a19c1-163">Falso</span><span class="sxs-lookup"><span data-stu-id="a19c1-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a19c1-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="a19c1-164">See also</span></span>

- [<span data-ttu-id="a19c1-165">Metadatos</span><span class="sxs-lookup"><span data-stu-id="a19c1-165">Metadata</span></span>](metadata-ex15websvcsotherref.md)
- [<span data-ttu-id="a19c1-166">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a19c1-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

