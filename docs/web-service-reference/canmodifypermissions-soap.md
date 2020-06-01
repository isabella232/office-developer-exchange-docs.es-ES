---
title: CanModifyPermissions (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9693de1a-0c76-4898-8f4d-a8693fb005b3
description: El elemento CanModifyPermissions indica si un usuario puede modificar los permisos de acceso a una ubicación de uso compartido de documentos.
ms.openlocfilehash: bf21b80a738498176bac41feea001ff859a54c2b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461586"
---
# <a name="canmodifypermissions-soap"></a><span data-ttu-id="d7237-103">CanModifyPermissions (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d7237-103">CanModifyPermissions (SOAP)</span></span>

<span data-ttu-id="d7237-104">El elemento **CanModifyPermissions** indica si un usuario puede modificar los permisos de acceso a una ubicación de uso compartido de documentos.</span><span class="sxs-lookup"><span data-stu-id="d7237-104">The **CanModifyPermissions** element indicates whether a user can modify access permissions to a document sharing location.</span></span> 
  
```XML
<CanModifyPermissions /> 
```

 <span data-ttu-id="d7237-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d7237-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d7237-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d7237-106">Attributes and elements</span></span>

<span data-ttu-id="d7237-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="d7237-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d7237-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="d7237-108">Attributes</span></span>

<span data-ttu-id="d7237-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d7237-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d7237-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d7237-110">Child elements</span></span>

<span data-ttu-id="d7237-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="d7237-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d7237-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="d7237-112">Parent elements</span></span>

|<span data-ttu-id="d7237-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d7237-113">**Element**</span></span>|<span data-ttu-id="d7237-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d7237-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7237-115">DocumentSharingLocation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d7237-115">DocumentSharingLocation (SOAP)</span></span>](documentsharinglocation-soap.md) <br/> |<span data-ttu-id="d7237-116">Representa la información de ubicación y metadatos de una ubicación de uso compartido de documentos.</span><span class="sxs-lookup"><span data-stu-id="d7237-116">Represents location and metadata information for a document sharing location.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d7237-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="d7237-117">Text value</span></span>

<span data-ttu-id="d7237-118">El valor booleano del elemento **CanModifyPermissions** indica si los usuarios pueden modificar los permisos de acceso a la ubicación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="d7237-118">The Boolean value of the **CanModifyPermissions** element indicates whether users can modify access permissions to the sharing location.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d7237-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="d7237-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7237-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="d7237-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="d7237-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="d7237-121">Schema Name</span></span>  <br/> |<span data-ttu-id="d7237-122">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="d7237-122">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="d7237-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="d7237-123">Validation File</span></span>  <br/> |<span data-ttu-id="d7237-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="d7237-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d7237-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="d7237-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="d7237-126">Verdadero</span><span class="sxs-lookup"><span data-stu-id="d7237-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d7237-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7237-127">See also</span></span>



[<span data-ttu-id="d7237-128">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d7237-128">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)


[<span data-ttu-id="d7237-129">Referencia del servicio web de Detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="d7237-129">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="d7237-130">Elementos XML de detección automática de SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="d7237-130">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

