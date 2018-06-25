---
title: GetAppManifestsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 86cf88f4-09c4-436a-a100-ac5cba0c4388
description: El elemento GetAppManifestsResponse define la respuesta de una solicitud de operación GetAppManifests.
ms.openlocfilehash: b5eac7c06c39c0ed80a362080db6b0cb37f8f4ca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764746"
---
# <a name="getappmanifestsresponse"></a><span data-ttu-id="6b0e6-103">GetAppManifestsResponse</span><span class="sxs-lookup"><span data-stu-id="6b0e6-103">GetAppManifestsResponse</span></span>

<span data-ttu-id="6b0e6-104">El elemento **GetAppManifestsResponse** define la respuesta de una solicitud de operación **GetAppManifests** .</span><span class="sxs-lookup"><span data-stu-id="6b0e6-104">The **GetAppManifestsResponse** element defines the response for a **GetAppManifests** operation request.</span></span> 
  
```XML
<GetAppManifestsResponse>
    <ResponseCode/>
    <Manifests/>
</GetAppManifestsResponse>
```

 <span data-ttu-id="6b0e6-105">**GetAppManifestsResponseType**</span><span class="sxs-lookup"><span data-stu-id="6b0e6-105">**GetAppManifestsResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6b0e6-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6b0e6-106">Attributes and elements</span></span>

<span data-ttu-id="6b0e6-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6b0e6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6b0e6-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6b0e6-108">Attributes</span></span>

<span data-ttu-id="6b0e6-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6b0e6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6b0e6-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6b0e6-110">Child elements</span></span>

<span data-ttu-id="6b0e6-111">[ResponseCode](responsecode.md) | [manifiestos](manifests.md) | [aplicaciones](apps.md)</span><span class="sxs-lookup"><span data-stu-id="6b0e6-111">[ResponseCode](responsecode.md) | [Manifests](manifests.md) | [Apps](apps.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6b0e6-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6b0e6-112">Parent elements</span></span>

<span data-ttu-id="6b0e6-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6b0e6-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6b0e6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b0e6-114">Remarks</span></span>

<span data-ttu-id="6b0e6-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6b0e6-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6b0e6-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6b0e6-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b0e6-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6b0e6-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b0e6-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6b0e6-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6b0e6-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6b0e6-119">Schema Name</span></span>  <br/> |<span data-ttu-id="6b0e6-120">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="6b0e6-120">Message schema</span></span>  <br/> |
|<span data-ttu-id="6b0e6-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6b0e6-121">Validation File</span></span>  <br/> |<span data-ttu-id="6b0e6-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6b0e6-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6b0e6-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6b0e6-123">Can Be Empty</span></span>  <br/> |<span data-ttu-id="6b0e6-124">False</span><span class="sxs-lookup"><span data-stu-id="6b0e6-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b0e6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b0e6-125">See also</span></span>



- [<span data-ttu-id="6b0e6-126">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="6b0e6-126">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

