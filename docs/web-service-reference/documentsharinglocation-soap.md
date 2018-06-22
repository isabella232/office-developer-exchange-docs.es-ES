---
title: DocumentSharingLocation (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21bc388c-33be-422b-a89d-30ade0fae8f1
description: El elemento DocumentSharingLocation contiene la ubicación y la información de metadatos de un documento de ubicación de uso compartido.
ms.openlocfilehash: d258efecb46d570138c7c2c78ed9d2fa9a275103
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764256"
---
# <a name="documentsharinglocation-soap"></a><span data-ttu-id="081a4-103">DocumentSharingLocation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="081a4-103">DocumentSharingLocation (SOAP)</span></span>

<span data-ttu-id="081a4-104">El elemento **DocumentSharingLocation** contiene la ubicación y la información de metadatos de un documento de ubicación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="081a4-104">The **DocumentSharingLocation** element contains location and metadata information for a document sharing location.</span></span> 
  
```XML
<DocumentSharingLocation>
   <ServiceUrl />
   <LocationUrl />
   <DisplayName />
   <SupportedFileExtensions />
   <ExternalAccessAllowed />
   <AnonymousAccessAllowed />
   <CanModifyPermissions />
   <IsDefault />
</DocumentSharingLocation>
```

 <span data-ttu-id="081a4-105">**DocumentSharingLocation**</span><span class="sxs-lookup"><span data-stu-id="081a4-105">**DocumentSharingLocation**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="081a4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="081a4-106">Attributes and elements</span></span>

<span data-ttu-id="081a4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="081a4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="081a4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="081a4-108">Attributes</span></span>

<span data-ttu-id="081a4-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="081a4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="081a4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="081a4-110">Child elements</span></span>

|<span data-ttu-id="081a4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="081a4-111">**Element**</span></span>|<span data-ttu-id="081a4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="081a4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="081a4-113">ServiceUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="081a4-113">ServiceUrl (SOAP)</span></span>](serviceurl-soap.md) <br/> |<span data-ttu-id="081a4-114">Representa la dirección URL del servicio web de uso compartido de documento.</span><span class="sxs-lookup"><span data-stu-id="081a4-114">Represents the URL of the document sharing web service.</span></span>  <br/> |
|[<span data-ttu-id="081a4-115">LocationUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="081a4-115">LocationUrl (SOAP)</span></span>](locationurl-soap.md) <br/> |<span data-ttu-id="081a4-116">Representa la dirección URL de la ubicación de uso compartido de documentos.</span><span class="sxs-lookup"><span data-stu-id="081a4-116">Represents the URL of the document sharing location.</span></span>  <br/> |
|[<span data-ttu-id="081a4-117">DisplayName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="081a4-117">DisplayName (SOAP)</span></span>](displayname-soap.md) <br/> |<span data-ttu-id="081a4-118">Representa el nombre del documento de ubicación que se usará en la interfaz de usuario de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="081a4-118">Represents the name of the document sharing location to use in the UI.</span></span>  <br/> |
|[<span data-ttu-id="081a4-119">SupportedFileExtensions (SOAP)</span><span class="sxs-lookup"><span data-stu-id="081a4-119">SupportedFileExtensions (SOAP)</span></span>](supportedfileextensions-soap.md) <br/> |<span data-ttu-id="081a4-120">Representa las extensiones de archivo que se pueden almacenar en la ubicación de uso compartido de documentos.</span><span class="sxs-lookup"><span data-stu-id="081a4-120">Represents the file extensions that can be stored in the document sharing location.</span></span>  <br/> |
|[<span data-ttu-id="081a4-121">ExternalAccessAllowed (SOAP)</span><span class="sxs-lookup"><span data-stu-id="081a4-121">ExternalAccessAllowed (SOAP)</span></span>](externalaccessallowed-soap.md) <br/> |<span data-ttu-id="081a4-122">Indica si el documento en la ubicación de uso compartido está disponible a fuera de las conexiones.</span><span class="sxs-lookup"><span data-stu-id="081a4-122">Indicates whether the document sharing location is available to outside connections.</span></span>  <br/> |
|[<span data-ttu-id="081a4-123">AnonymousAccessAllowed (SOAP)</span><span class="sxs-lookup"><span data-stu-id="081a4-123">AnonymousAccessAllowed (SOAP)</span></span>](anonymousaccessallowed-soap.md) <br/> |<span data-ttu-id="081a4-124">Indica si el acceso a la ubicación de uso compartido requiere un usuario autenticado.</span><span class="sxs-lookup"><span data-stu-id="081a4-124">Indicates whether access to the sharing location requires an authenticated user.</span></span>  <br/> |
|[<span data-ttu-id="081a4-125">CanModifyPermissions (SOAP)</span><span class="sxs-lookup"><span data-stu-id="081a4-125">CanModifyPermissions (SOAP)</span></span>](canmodifypermissions-soap.md) <br/> |<span data-ttu-id="081a4-126">Indica si el usuario puede modificar los permisos de acceso a la ubicación de uso compartido de documentos.</span><span class="sxs-lookup"><span data-stu-id="081a4-126">Indicates whether the user can modify access permissions to the document sharing location.</span></span>  <br/> |
|[<span data-ttu-id="081a4-127">IsDefault (SOAP)</span><span class="sxs-lookup"><span data-stu-id="081a4-127">IsDefault (SOAP)</span></span>](isdefault-soap.md) <br/> |<span data-ttu-id="081a4-128">Indica si el documento en la ubicación de uso compartido es la predeterminada del usuario ubicación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="081a4-128">Indicates whether the document sharing location is the user's default sharing location.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="081a4-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="081a4-129">Parent elements</span></span>

|<span data-ttu-id="081a4-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="081a4-130">**Element**</span></span>|<span data-ttu-id="081a4-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="081a4-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="081a4-132">DocumentSharingLocations (SOAP)</span><span class="sxs-lookup"><span data-stu-id="081a4-132">DocumentSharingLocations (SOAP)</span></span>](documentsharinglocations-soap.md) <br/> |<span data-ttu-id="081a4-133">Contiene una lista de uso compartido de las ubicaciones y los metadatos del documento.</span><span class="sxs-lookup"><span data-stu-id="081a4-133">Contains a list of document sharing locations and metadata.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="081a4-134">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="081a4-134">Text value</span></span>

<span data-ttu-id="081a4-135">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="081a4-135">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="081a4-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="081a4-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="081a4-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="081a4-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="081a4-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="081a4-138">Schema Name</span></span>  <br/> |<span data-ttu-id="081a4-139">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="081a4-139">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="081a4-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="081a4-140">Validation File</span></span>  <br/> |<span data-ttu-id="081a4-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="081a4-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="081a4-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="081a4-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="081a4-143">Verdadero</span><span class="sxs-lookup"><span data-stu-id="081a4-143">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="081a4-144">Ver también</span><span class="sxs-lookup"><span data-stu-id="081a4-144">See also</span></span>

- [<span data-ttu-id="081a4-145">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="081a4-145">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="081a4-146">Referencia de servicio web de detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="081a4-146">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="081a4-147">Elementos de Autodiscover XML SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="081a4-147">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

