---
title: CanModifyPermissions (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9693de1a-0c76-4898-8f4d-a8693fb005b3
description: El elemento CanModifyPermissions indica si un usuario puede modificar los permisos de acceso a un documento de ubicación de uso compartido.
ms.openlocfilehash: 16526cb79eeca591af6e009e67959a1c3b58a5d7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763724"
---
# <a name="canmodifypermissions-soap"></a><span data-ttu-id="9703d-103">CanModifyPermissions (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9703d-103">CanModifyPermissions (SOAP)</span></span>

<span data-ttu-id="9703d-104">El elemento **CanModifyPermissions** indica si un usuario puede modificar los permisos de acceso a un documento de ubicación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="9703d-104">The **CanModifyPermissions** element indicates whether a user can modify access permissions to a document sharing location.</span></span> 
  
```XML
<CanModifyPermissions /> 
```

 <span data-ttu-id="9703d-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9703d-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9703d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9703d-106">Attributes and elements</span></span>

<span data-ttu-id="9703d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9703d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9703d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9703d-108">Attributes</span></span>

<span data-ttu-id="9703d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9703d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9703d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9703d-110">Child elements</span></span>

<span data-ttu-id="9703d-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9703d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9703d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9703d-112">Parent elements</span></span>

|<span data-ttu-id="9703d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9703d-113">**Element**</span></span>|<span data-ttu-id="9703d-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9703d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9703d-115">DocumentSharingLocation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9703d-115">DocumentSharingLocation (SOAP)</span></span>](documentsharinglocation-soap.md) <br/> |<span data-ttu-id="9703d-116">Representa información de ubicación y los metadatos de un documento de ubicación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="9703d-116">Represents location and metadata information for a document sharing location.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9703d-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9703d-117">Text value</span></span>

<span data-ttu-id="9703d-118">El valor de tipo Boolean del elemento **CanModifyPermissions** indica si los usuarios pueden modificar los permisos de acceso a la ubicación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="9703d-118">The Boolean value of the **CanModifyPermissions** element indicates whether users can modify access permissions to the sharing location.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="9703d-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9703d-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9703d-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9703d-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="9703d-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9703d-121">Schema Name</span></span>  <br/> |<span data-ttu-id="9703d-122">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="9703d-122">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="9703d-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9703d-123">Validation File</span></span>  <br/> |<span data-ttu-id="9703d-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9703d-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9703d-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9703d-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="9703d-126">Verdadero</span><span class="sxs-lookup"><span data-stu-id="9703d-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9703d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9703d-127">See also</span></span>



[<span data-ttu-id="9703d-128">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="9703d-128">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)


[<span data-ttu-id="9703d-129">Referencia de servicio web de detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="9703d-129">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="9703d-130">Elementos de Autodiscover XML SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9703d-130">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

