---
title: SupportedFileExtensions (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f73d18c-7bb1-4ab6-a23b-6d948e590b53
description: El elemento SupportedFileExtensions enumera las extensiones de archivo que se pueden almacenar en un documento de ubicación de uso compartido.
ms.openlocfilehash: 0f1dbbce2b836fe05e4bc612c607302783d5e05d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840605"
---
# <a name="supportedfileextensions-soap"></a><span data-ttu-id="82e0b-103">SupportedFileExtensions (SOAP)</span><span class="sxs-lookup"><span data-stu-id="82e0b-103">SupportedFileExtensions (SOAP)</span></span>

<span data-ttu-id="82e0b-104">El elemento **SupportedFileExtensions** enumera las extensiones de archivo que se pueden almacenar en un documento de ubicación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="82e0b-104">The **SupportedFileExtensions** element lists the file extensions that can be stored in a document sharing location.</span></span> 
  
```XML
<SupportedFileExtensions /> 
```

 <span data-ttu-id="82e0b-105">**ArrayOfFileExtension**</span><span class="sxs-lookup"><span data-stu-id="82e0b-105">**ArrayOfFileExtension**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="82e0b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="82e0b-106">Attributes and elements</span></span>

<span data-ttu-id="82e0b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="82e0b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82e0b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="82e0b-108">Attributes</span></span>

<span data-ttu-id="82e0b-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="82e0b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="82e0b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="82e0b-110">Child elements</span></span>

|<span data-ttu-id="82e0b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="82e0b-111">**Element**</span></span>|<span data-ttu-id="82e0b-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="82e0b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82e0b-113">FileExtension (SOAP)</span><span class="sxs-lookup"><span data-stu-id="82e0b-113">FileExtension (SOAP)</span></span>](fileextension-soap.md) <br/> |<span data-ttu-id="82e0b-114">Representa una extensión de archivo.</span><span class="sxs-lookup"><span data-stu-id="82e0b-114">Represents a file extension.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="82e0b-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="82e0b-115">Parent elements</span></span>

|<span data-ttu-id="82e0b-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="82e0b-116">**Element**</span></span>|<span data-ttu-id="82e0b-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="82e0b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82e0b-118">DocumentSharingLocation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="82e0b-118">DocumentSharingLocation (SOAP)</span></span>](documentsharinglocation-soap.md) <br/> |<span data-ttu-id="82e0b-119">Representa información de ubicación y los metadatos de un documento de ubicación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="82e0b-119">Represents location and metadata information for a document sharing location.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="82e0b-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="82e0b-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82e0b-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="82e0b-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="82e0b-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="82e0b-122">Schema Name</span></span>  <br/> |<span data-ttu-id="82e0b-123">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="82e0b-123">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="82e0b-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="82e0b-124">Validation File</span></span>  <br/> |<span data-ttu-id="82e0b-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="82e0b-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="82e0b-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="82e0b-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="82e0b-127">Verdadero</span><span class="sxs-lookup"><span data-stu-id="82e0b-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82e0b-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="82e0b-128">See also</span></span>



[<span data-ttu-id="82e0b-129">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="82e0b-129">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)


[<span data-ttu-id="82e0b-130">Referencia de servicio web de detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="82e0b-130">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="82e0b-131">Elementos de Autodiscover XML SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="82e0b-131">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

