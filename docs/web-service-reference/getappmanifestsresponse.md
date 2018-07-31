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
ms.openlocfilehash: ae9d1d853023a5b42db2e8fee2ed57f585433f69
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354151"
---
# <a name="getappmanifestsresponse"></a><span data-ttu-id="3091d-103">GetAppManifestsResponse</span><span class="sxs-lookup"><span data-stu-id="3091d-103">GetAppManifestsResponse</span></span>

<span data-ttu-id="3091d-104">El elemento **GetAppManifestsResponse** define la respuesta de una solicitud de operación **GetAppManifests** .</span><span class="sxs-lookup"><span data-stu-id="3091d-104">The **GetAppManifestsResponse** element defines the response for a **GetAppManifests** operation request.</span></span> 
  
```xml
<GetAppManifestsResponse>
    <ResponseCode/>
    <Manifests/>
</GetAppManifestsResponse>
```

```xml
<GetAppManifestsResponse>
    <ResponseCode/>
    <Apps/>
</GetAppManifestsResponse>
```

<span data-ttu-id="3091d-105">**GetAppManifestsResponseType**</span><span class="sxs-lookup"><span data-stu-id="3091d-105">**GetAppManifestsResponseType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3091d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3091d-106">Attributes and elements</span></span>

<span data-ttu-id="3091d-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3091d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3091d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3091d-108">Attributes</span></span>

<span data-ttu-id="3091d-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3091d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3091d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3091d-110">Child elements</span></span>

<span data-ttu-id="3091d-111">[ResponseCode](responsecode.md) | [manifiestos](manifests.md) | [aplicaciones](apps.md)</span><span class="sxs-lookup"><span data-stu-id="3091d-111">[ResponseCode](responsecode.md) | [Manifests](manifests.md) | [Apps](apps.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3091d-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3091d-112">Parent elements</span></span>

<span data-ttu-id="3091d-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3091d-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3091d-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3091d-114">Remarks</span></span>

<span data-ttu-id="3091d-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3091d-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3091d-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="3091d-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3091d-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3091d-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3091d-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3091d-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3091d-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3091d-119">Schema Name</span></span>  <br/> |<span data-ttu-id="3091d-120">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="3091d-120">Message schema</span></span>  <br/> |
|<span data-ttu-id="3091d-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3091d-121">Validation File</span></span>  <br/> |<span data-ttu-id="3091d-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3091d-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3091d-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3091d-123">Can Be Empty</span></span>  <br/> |<span data-ttu-id="3091d-124">False</span><span class="sxs-lookup"><span data-stu-id="3091d-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3091d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="3091d-125">See also</span></span>

- [<span data-ttu-id="3091d-126">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3091d-126">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

