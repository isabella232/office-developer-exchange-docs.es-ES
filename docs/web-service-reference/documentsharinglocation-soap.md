---
title: DocumentSharingLocation (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21bc388c-33be-422b-a89d-30ade0fae8f1
description: El elemento DocumentSharingLocation contiene información de ubicación y metadatos de una ubicación de uso compartido de documentos.
ms.openlocfilehash: 6fed933da979ab3e3fca51ba606127b7f0a4e3f8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457063"
---
# <a name="documentsharinglocation-soap"></a><span data-ttu-id="a208a-103">DocumentSharingLocation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a208a-103">DocumentSharingLocation (SOAP)</span></span>

<span data-ttu-id="a208a-104">El elemento **DocumentSharingLocation** contiene información de ubicación y metadatos de una ubicación de uso compartido de documentos.</span><span class="sxs-lookup"><span data-stu-id="a208a-104">The **DocumentSharingLocation** element contains location and metadata information for a document sharing location.</span></span> 
  
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

 <span data-ttu-id="a208a-105">**DocumentSharingLocation**</span><span class="sxs-lookup"><span data-stu-id="a208a-105">**DocumentSharingLocation**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a208a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a208a-106">Attributes and elements</span></span>

<span data-ttu-id="a208a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a208a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a208a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a208a-108">Attributes</span></span>

<span data-ttu-id="a208a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a208a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a208a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a208a-110">Child elements</span></span>

|<span data-ttu-id="a208a-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a208a-111">**Element**</span></span>|<span data-ttu-id="a208a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a208a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a208a-113">ServiceUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a208a-113">ServiceUrl (SOAP)</span></span>](serviceurl-soap.md) <br/> |<span data-ttu-id="a208a-114">Representa la dirección URL del servicio Web de uso compartido de documentos.</span><span class="sxs-lookup"><span data-stu-id="a208a-114">Represents the URL of the document sharing web service.</span></span>  <br/> |
|[<span data-ttu-id="a208a-115">LocationUrl (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a208a-115">LocationUrl (SOAP)</span></span>](locationurl-soap.md) <br/> |<span data-ttu-id="a208a-116">Representa la dirección URL de la ubicación de uso compartido de documentos.</span><span class="sxs-lookup"><span data-stu-id="a208a-116">Represents the URL of the document sharing location.</span></span>  <br/> |
|[<span data-ttu-id="a208a-117">DisplayName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a208a-117">DisplayName (SOAP)</span></span>](displayname-soap.md) <br/> |<span data-ttu-id="a208a-118">Representa el nombre de la ubicación de uso compartido de documentos que se va a usar en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="a208a-118">Represents the name of the document sharing location to use in the UI.</span></span>  <br/> |
|[<span data-ttu-id="a208a-119">SupportedFileExtensions (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a208a-119">SupportedFileExtensions (SOAP)</span></span>](supportedfileextensions-soap.md) <br/> |<span data-ttu-id="a208a-120">Representa las extensiones de archivo que se pueden almacenar en la ubicación de uso compartido de documentos.</span><span class="sxs-lookup"><span data-stu-id="a208a-120">Represents the file extensions that can be stored in the document sharing location.</span></span>  <br/> |
|[<span data-ttu-id="a208a-121">ExternalAccessAllowed (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a208a-121">ExternalAccessAllowed (SOAP)</span></span>](externalaccessallowed-soap.md) <br/> |<span data-ttu-id="a208a-122">Indica si la ubicación de uso compartido de documentos está disponible para conexiones externas.</span><span class="sxs-lookup"><span data-stu-id="a208a-122">Indicates whether the document sharing location is available to outside connections.</span></span>  <br/> |
|[<span data-ttu-id="a208a-123">AnonymousAccessAllowed (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a208a-123">AnonymousAccessAllowed (SOAP)</span></span>](anonymousaccessallowed-soap.md) <br/> |<span data-ttu-id="a208a-124">Indica si el acceso a la ubicación compartida requiere un usuario autenticado.</span><span class="sxs-lookup"><span data-stu-id="a208a-124">Indicates whether access to the sharing location requires an authenticated user.</span></span>  <br/> |
|[<span data-ttu-id="a208a-125">CanModifyPermissions (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a208a-125">CanModifyPermissions (SOAP)</span></span>](canmodifypermissions-soap.md) <br/> |<span data-ttu-id="a208a-126">Indica si el usuario puede modificar los permisos de acceso a la ubicación de uso compartido de documentos.</span><span class="sxs-lookup"><span data-stu-id="a208a-126">Indicates whether the user can modify access permissions to the document sharing location.</span></span>  <br/> |
|[<span data-ttu-id="a208a-127">IsDefault (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a208a-127">IsDefault (SOAP)</span></span>](isdefault-soap.md) <br/> |<span data-ttu-id="a208a-128">Indica si la ubicación de uso compartido de documentos es la ubicación de uso compartido predeterminada del usuario.</span><span class="sxs-lookup"><span data-stu-id="a208a-128">Indicates whether the document sharing location is the user's default sharing location.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a208a-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a208a-129">Parent elements</span></span>

|<span data-ttu-id="a208a-130">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a208a-130">**Element**</span></span>|<span data-ttu-id="a208a-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a208a-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a208a-132">DocumentSharingLocations (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a208a-132">DocumentSharingLocations (SOAP)</span></span>](documentsharinglocations-soap.md) <br/> |<span data-ttu-id="a208a-133">Contiene una lista de los metadatos y las ubicaciones de uso compartido de documentos.</span><span class="sxs-lookup"><span data-stu-id="a208a-133">Contains a list of document sharing locations and metadata.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a208a-134">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="a208a-134">Text value</span></span>

<span data-ttu-id="a208a-135">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a208a-135">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a208a-136">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a208a-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a208a-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="a208a-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="a208a-138">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a208a-138">Schema Name</span></span>  <br/> |<span data-ttu-id="a208a-139">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="a208a-139">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="a208a-140">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a208a-140">Validation File</span></span>  <br/> |<span data-ttu-id="a208a-141">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a208a-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a208a-142">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a208a-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="a208a-143">Verdadero</span><span class="sxs-lookup"><span data-stu-id="a208a-143">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a208a-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="a208a-144">See also</span></span>

- [<span data-ttu-id="a208a-145">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="a208a-145">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="a208a-146">Referencia del servicio web de Detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="a208a-146">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="a208a-147">Elementos XML de detección automática de SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="a208a-147">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

