---
title: IsDefault (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7358bb88-c441-4f2c-9647-c030e7303e8a
description: El elemento IsDefault indica si una ubicación de uso compartido de documentos es la ubicación de uso compartido predeterminada del usuario.
ms.openlocfilehash: dbf419d591bc0d693204df51d8259c2a9fe13c50
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466076"
---
# <a name="isdefault-soap"></a><span data-ttu-id="6a191-103">IsDefault (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6a191-103">IsDefault (SOAP)</span></span>

<span data-ttu-id="6a191-104">El elemento **IsDefault** indica si una ubicación de uso compartido de documentos es la ubicación de uso compartido predeterminada del usuario.</span><span class="sxs-lookup"><span data-stu-id="6a191-104">The **IsDefault** element indicates whether a document sharing location is the user's default sharing location.</span></span> 
  
```XML
<IsDefault /> 
```

 <span data-ttu-id="6a191-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6a191-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6a191-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6a191-106">Attributes and elements</span></span>

<span data-ttu-id="6a191-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6a191-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6a191-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6a191-108">Attributes</span></span>

<span data-ttu-id="6a191-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6a191-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6a191-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6a191-110">Child elements</span></span>

<span data-ttu-id="6a191-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6a191-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6a191-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6a191-112">Parent elements</span></span>

|<span data-ttu-id="6a191-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6a191-113">**Element**</span></span>|<span data-ttu-id="6a191-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6a191-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6a191-115">DocumentSharingLocation (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6a191-115">DocumentSharingLocation (SOAP)</span></span>](documentsharinglocation-soap.md) <br/> |<span data-ttu-id="6a191-116">Representa la información de ubicación y metadatos de una ubicación de uso compartido de documentos.</span><span class="sxs-lookup"><span data-stu-id="6a191-116">Represents location and metadata information for a document sharing location.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6a191-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6a191-117">Text value</span></span>

<span data-ttu-id="6a191-118">El valor booleano del elemento **IsDefault** indica si la ubicación de uso compartido es la ubicación de uso compartido predeterminada del usuario.</span><span class="sxs-lookup"><span data-stu-id="6a191-118">The Boolean value of the **IsDefault** element indicates whether the sharing location is the user's default sharing location.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="6a191-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6a191-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6a191-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a191-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="6a191-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6a191-121">Schema Name</span></span>  <br/> |<span data-ttu-id="6a191-122">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="6a191-122">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="6a191-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6a191-123">Validation File</span></span>  <br/> |<span data-ttu-id="6a191-124">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6a191-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6a191-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6a191-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="6a191-126">Verdadero</span><span class="sxs-lookup"><span data-stu-id="6a191-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6a191-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a191-127">See also</span></span>



[<span data-ttu-id="6a191-128">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="6a191-128">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)


[<span data-ttu-id="6a191-129">Referencia del servicio web de Detección automática para Exchange</span><span class="sxs-lookup"><span data-stu-id="6a191-129">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
  
[<span data-ttu-id="6a191-130">Elementos XML de detección automática de SOAP para Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="6a191-130">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

