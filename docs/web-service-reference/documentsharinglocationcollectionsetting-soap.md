---
title: DocumentSharingLocationCollectionSetting (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e3346f9-7a55-4e87-b121-9b1ee7f227f4
description: El elemento DocumentSharingLocationCollectionSetting representa una configuración de usuario que es una colección de ubicaciones y metadatos de uso compartido de documentación.
ms.openlocfilehash: 2a52f639a1f1bf638aacc78666c58aed1fae0fa0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457056"
---
# <a name="documentsharinglocationcollectionsetting-soap"></a><span data-ttu-id="ab9ef-103">DocumentSharingLocationCollectionSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ab9ef-103">DocumentSharingLocationCollectionSetting (SOAP)</span></span>

<span data-ttu-id="ab9ef-104">El elemento **DocumentSharingLocationCollectionSetting** representa una configuración de usuario que es una colección de ubicaciones y metadatos de uso compartido de documentación.</span><span class="sxs-lookup"><span data-stu-id="ab9ef-104">The **DocumentSharingLocationCollectionSetting** element represents a user setting that is a collection of documentation sharing locations and metadata.</span></span> 
  
[<span data-ttu-id="ab9ef-105">DocumentSharingLocationCollectionSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ab9ef-105">DocumentSharingLocationCollectionSetting (SOAP)</span></span>](documentsharinglocationcollectionsetting-soap.md)
  
```XML
<DocumentSharingLocationCollectionSetting>
    <DocumentSharingLocations />
</DocumentSharingLocationCollectionSetting>
```

 <span data-ttu-id="ab9ef-106">**DocumentSharingLocationCollectionSetting**</span><span class="sxs-lookup"><span data-stu-id="ab9ef-106">**DocumentSharingLocationCollectionSetting**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ab9ef-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ab9ef-107">Attributes and elements</span></span>

<span data-ttu-id="ab9ef-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ab9ef-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ab9ef-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="ab9ef-109">Attributes</span></span>

<span data-ttu-id="ab9ef-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ab9ef-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ab9ef-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ab9ef-111">Child elements</span></span>

|<span data-ttu-id="ab9ef-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ab9ef-112">**Element**</span></span>|<span data-ttu-id="ab9ef-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ab9ef-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab9ef-114">DocumentSharingLocations (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ab9ef-114">DocumentSharingLocations (SOAP)</span></span>](documentsharinglocations-soap.md) <br/> |<span data-ttu-id="ab9ef-115">Representa la ubicación y los metadatos de una lista de ubicaciones de uso compartido de documentos.</span><span class="sxs-lookup"><span data-stu-id="ab9ef-115">Represents the location and metadata for a list of document sharing locations.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ab9ef-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ab9ef-116">Parent elements</span></span>

|<span data-ttu-id="ab9ef-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ab9ef-117">**Element**</span></span>|<span data-ttu-id="ab9ef-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ab9ef-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab9ef-119">UserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ab9ef-119">UserSettings (SOAP)</span></span>](usersettings-soap.md) <br/> |<span data-ttu-id="ab9ef-120">Representa una colección de opciones de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="ab9ef-120">Represents a collection of user settings.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="ab9ef-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ab9ef-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab9ef-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab9ef-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="ab9ef-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ab9ef-123">Schema Name</span></span>  <br/> |<span data-ttu-id="ab9ef-124">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="ab9ef-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="ab9ef-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ab9ef-125">Validation File</span></span>  <br/> |<span data-ttu-id="ab9ef-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ab9ef-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ab9ef-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ab9ef-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="ab9ef-128">Verdadero</span><span class="sxs-lookup"><span data-stu-id="ab9ef-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab9ef-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab9ef-129">See also</span></span>

- [<span data-ttu-id="ab9ef-130">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="ab9ef-130">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
- [<span data-ttu-id="ab9ef-131">Referencia del servicio web de Detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="ab9ef-131">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="ab9ef-132">Elementos XML de detección automática de SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="ab9ef-132">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

