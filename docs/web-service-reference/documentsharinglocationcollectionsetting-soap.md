---
title: DocumentSharingLocationCollectionSetting (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e3346f9-7a55-4e87-b121-9b1ee7f227f4
description: El elemento DocumentSharingLocationCollectionSetting representa un usuario de configuración, es decir, una colección de documentación de uso compartido de las ubicaciones y los metadatos.
ms.openlocfilehash: 9871e3fccdcce95fc275768d99159c70f57a07af
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764255"
---
# <a name="documentsharinglocationcollectionsetting-soap"></a><span data-ttu-id="dce1f-103">DocumentSharingLocationCollectionSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dce1f-103">DocumentSharingLocationCollectionSetting (SOAP)</span></span>

<span data-ttu-id="dce1f-104">El elemento **DocumentSharingLocationCollectionSetting** representa un usuario de configuración, es decir, una colección de documentación de uso compartido de las ubicaciones y los metadatos.</span><span class="sxs-lookup"><span data-stu-id="dce1f-104">The **DocumentSharingLocationCollectionSetting** element represents a user setting that is a collection of documentation sharing locations and metadata.</span></span> 
  
[<span data-ttu-id="dce1f-105">DocumentSharingLocationCollectionSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dce1f-105">DocumentSharingLocationCollectionSetting (SOAP)</span></span>](documentsharinglocationcollectionsetting-soap.md)
  
```XML
<DocumentSharingLocationCollectionSetting>
    <DocumentSharingLocations />
</DocumentSharingLocationCollectionSetting>
```

 <span data-ttu-id="dce1f-106">**DocumentSharingLocationCollectionSetting**</span><span class="sxs-lookup"><span data-stu-id="dce1f-106">**DocumentSharingLocationCollectionSetting**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dce1f-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dce1f-107">Attributes and elements</span></span>

<span data-ttu-id="dce1f-108">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dce1f-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dce1f-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="dce1f-109">Attributes</span></span>

<span data-ttu-id="dce1f-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dce1f-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dce1f-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dce1f-111">Child elements</span></span>

|<span data-ttu-id="dce1f-112">**Element**</span><span class="sxs-lookup"><span data-stu-id="dce1f-112">**Element**</span></span>|<span data-ttu-id="dce1f-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dce1f-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dce1f-114">DocumentSharingLocations (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dce1f-114">DocumentSharingLocations (SOAP)</span></span>](documentsharinglocations-soap.md) <br/> |<span data-ttu-id="dce1f-115">Representa la ubicación y los metadatos para una lista de ubicaciones de uso compartido de documentos.</span><span class="sxs-lookup"><span data-stu-id="dce1f-115">Represents the location and metadata for a list of document sharing locations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dce1f-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dce1f-116">Parent elements</span></span>

|<span data-ttu-id="dce1f-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="dce1f-117">**Element**</span></span>|<span data-ttu-id="dce1f-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dce1f-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dce1f-119">UserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dce1f-119">UserSettings (SOAP)</span></span>](usersettings-soap.md) <br/> |<span data-ttu-id="dce1f-120">Representa una colección de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="dce1f-120">Represents a collection of user settings.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="dce1f-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dce1f-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dce1f-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dce1f-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="dce1f-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dce1f-123">Schema Name</span></span>  <br/> |<span data-ttu-id="dce1f-124">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="dce1f-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="dce1f-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dce1f-125">Validation File</span></span>  <br/> |<span data-ttu-id="dce1f-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dce1f-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dce1f-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dce1f-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="dce1f-128">Verdadero</span><span class="sxs-lookup"><span data-stu-id="dce1f-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dce1f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="dce1f-129">See also</span></span>

- [<span data-ttu-id="dce1f-130">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="dce1f-130">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="dce1f-131">Referencia de servicio web de detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="dce1f-131">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="dce1f-132">Elementos de Autodiscover XML SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="dce1f-132">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

