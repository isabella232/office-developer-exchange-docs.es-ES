---
title: SupportedFileExtensions (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f73d18c-7bb1-4ab6-a23b-6d948e590b53
description: El elemento SupportedFileExtensions enumera las extensiones de archivo que se pueden almacenar en una ubicación de uso compartido de documentos.
ms.openlocfilehash: d783b147a25ebbe3bff59c2142012b50bd80004e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44433990"
---
# <a name="supportedfileextensions-soap"></a><span data-ttu-id="d9104-103">SupportedFileExtensions (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d9104-103">SupportedFileExtensions (SOAP)</span></span>

<span data-ttu-id="d9104-104">El elemento **SupportedFileExtensions** enumera las extensiones de archivo que se pueden almacenar en una ubicación de uso compartido de documentos.</span><span class="sxs-lookup"><span data-stu-id="d9104-104">The **SupportedFileExtensions** element lists the file extensions that can be stored in a document sharing location.</span></span> 
  
```XML
<SupportedFileExtensions /> 
```

 <span data-ttu-id="d9104-105">**ArrayOfFileExtension**</span><span class="sxs-lookup"><span data-stu-id="d9104-105">**ArrayOfFileExtension**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d9104-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d9104-106">Attributes and elements</span></span>

<span data-ttu-id="d9104-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d9104-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9104-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d9104-108">Attributes</span></span>

<span data-ttu-id="d9104-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d9104-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d9104-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d9104-110">Child elements</span></span>

|<span data-ttu-id="d9104-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d9104-111">**Element**</span></span>|<span data-ttu-id="d9104-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d9104-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9104-113">FileExtension (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d9104-113">FileExtension (SOAP)</span></span>](fileextension-soap.md) <br/> |<span data-ttu-id="d9104-114">Representa una extensión de archivo.</span><span class="sxs-lookup"><span data-stu-id="d9104-114">Represents a file extension.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d9104-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d9104-115">Parent elements</span></span>

|<span data-ttu-id="d9104-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d9104-116">**Element**</span></span>|<span data-ttu-id="d9104-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d9104-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9104-118">DocumentSharingLocation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d9104-118">DocumentSharingLocation (SOAP)</span></span>](documentsharinglocation-soap.md) <br/> |<span data-ttu-id="d9104-119">Representa la información de ubicación y metadatos de una ubicación de uso compartido de documentos.</span><span class="sxs-lookup"><span data-stu-id="d9104-119">Represents location and metadata information for a document sharing location.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="d9104-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d9104-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9104-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="d9104-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="d9104-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d9104-122">Schema Name</span></span>  <br/> |<span data-ttu-id="d9104-123">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="d9104-123">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="d9104-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d9104-124">Validation File</span></span>  <br/> |<span data-ttu-id="d9104-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d9104-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d9104-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d9104-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="d9104-127">Verdadero</span><span class="sxs-lookup"><span data-stu-id="d9104-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9104-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9104-128">See also</span></span>



[<span data-ttu-id="d9104-129">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d9104-129">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)


[<span data-ttu-id="d9104-130">Referencia del servicio web de Detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="d9104-130">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="d9104-131">Elementos XML de detección automática de SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="d9104-131">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

