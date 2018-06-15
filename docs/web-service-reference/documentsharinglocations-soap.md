---
title: DocumentSharingLocations (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 394f6015-721b-4800-9286-039d430f09b3
description: El elemento DocumentSharingLocations contiene una lista de ubicación y la información de metadatos de un documento de ubicación de uso compartido.
ms.openlocfilehash: 72d1ae9f01ad45441b4e255f2fb6353be2dc8d28
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19764260"
---
# <a name="documentsharinglocations-soap"></a><span data-ttu-id="4e1ff-103">DocumentSharingLocations (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4e1ff-103">DocumentSharingLocations (SOAP)</span></span>

<span data-ttu-id="4e1ff-104">El elemento **DocumentSharingLocations** contiene una lista de ubicación y la información de metadatos de un documento de ubicación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="4e1ff-104">The **DocumentSharingLocations** element contains a list of location and metadata information for a document sharing location.</span></span> 
  
```XML
<DocumentSharingLocations>
   <DocumentSharingLocation />
</DocumentSharingLocations>
```

 <span data-ttu-id="4e1ff-105">**DocumentSharingLocations**</span><span class="sxs-lookup"><span data-stu-id="4e1ff-105">**DocumentSharingLocations**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4e1ff-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4e1ff-106">Attributes and elements</span></span>

<span data-ttu-id="4e1ff-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4e1ff-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4e1ff-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4e1ff-108">Attributes</span></span>

<span data-ttu-id="4e1ff-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4e1ff-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4e1ff-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4e1ff-110">Child elements</span></span>

|<span data-ttu-id="4e1ff-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4e1ff-111">**Element**</span></span>|<span data-ttu-id="4e1ff-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4e1ff-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e1ff-113">DocumentSharingLocation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4e1ff-113">DocumentSharingLocation (SOAP)</span></span>](documentsharinglocation-soap.md) <br/> |<span data-ttu-id="4e1ff-114">Contiene la ubicación y los metadatos de un documento de ubicación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="4e1ff-114">Contains the location and metadata for a document sharing location.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4e1ff-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4e1ff-115">Parent elements</span></span>

|<span data-ttu-id="4e1ff-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="4e1ff-116">**Element**</span></span>|<span data-ttu-id="4e1ff-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4e1ff-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4e1ff-118">DocumentSharingLocationCollectionSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4e1ff-118">DocumentSharingLocationCollectionSetting (SOAP)</span></span>](documentsharinglocationcollectionsetting-soap.md) <br/> |<span data-ttu-id="4e1ff-119">Representa un usuario de configuración, es decir, una colección de documentación de uso compartido de las ubicaciones y los metadatos.</span><span class="sxs-lookup"><span data-stu-id="4e1ff-119">Represents a user setting that is a collection of documentation sharing locations and metadata.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="4e1ff-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4e1ff-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e1ff-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4e1ff-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="4e1ff-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4e1ff-122">Schema Name</span></span>  <br/> |<span data-ttu-id="4e1ff-123">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="4e1ff-123">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="4e1ff-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4e1ff-124">Validation File</span></span>  <br/> |<span data-ttu-id="4e1ff-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4e1ff-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4e1ff-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4e1ff-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="4e1ff-127">Verdadero</span><span class="sxs-lookup"><span data-stu-id="4e1ff-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e1ff-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="4e1ff-128">See also</span></span>

- [<span data-ttu-id="4e1ff-129">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="4e1ff-129">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="4e1ff-130">Referencia de servicio web de detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="4e1ff-130">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="4e1ff-131">Elementos de Autodiscover XML SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="4e1ff-131">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

