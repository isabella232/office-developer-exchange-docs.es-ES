---
title: GetAppManifestsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 86cf88f4-09c4-436a-a100-ac5cba0c4388
description: El elemento GetAppManifestsResponse define la respuesta para una solicitud de operación GetAppManifests.
ms.openlocfilehash: a01f6265d6d534e2f7868b17acf19f0f5d52a01f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462967"
---
# <a name="getappmanifestsresponse"></a><span data-ttu-id="04d06-103">GetAppManifestsResponse</span><span class="sxs-lookup"><span data-stu-id="04d06-103">GetAppManifestsResponse</span></span>

<span data-ttu-id="04d06-104">El elemento **GetAppManifestsResponse** define la respuesta para una solicitud de operación **GetAppManifests** .</span><span class="sxs-lookup"><span data-stu-id="04d06-104">The **GetAppManifestsResponse** element defines the response for a **GetAppManifests** operation request.</span></span> 
  
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

<span data-ttu-id="04d06-105">**GetAppManifestsResponseType**</span><span class="sxs-lookup"><span data-stu-id="04d06-105">**GetAppManifestsResponseType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="04d06-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="04d06-106">Attributes and elements</span></span>

<span data-ttu-id="04d06-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="04d06-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04d06-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="04d06-108">Attributes</span></span>

<span data-ttu-id="04d06-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="04d06-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="04d06-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="04d06-110">Child elements</span></span>

<span data-ttu-id="04d06-111">[ResponseCode](responsecode.md)  |  [Manifiestos](manifests.md)  |  [Aplicaciones](apps.md)</span><span class="sxs-lookup"><span data-stu-id="04d06-111">[ResponseCode](responsecode.md) | [Manifests](manifests.md) | [Apps](apps.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="04d06-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="04d06-112">Parent elements</span></span>

<span data-ttu-id="04d06-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="04d06-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="04d06-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="04d06-114">Remarks</span></span>

<span data-ttu-id="04d06-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="04d06-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="04d06-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="04d06-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="04d06-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="04d06-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04d06-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="04d06-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="04d06-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="04d06-119">Schema Name</span></span>  <br/> |<span data-ttu-id="04d06-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="04d06-120">Message schema</span></span>  <br/> |
|<span data-ttu-id="04d06-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="04d06-121">Validation File</span></span>  <br/> |<span data-ttu-id="04d06-122">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="04d06-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="04d06-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="04d06-123">Can Be Empty</span></span>  <br/> |<span data-ttu-id="04d06-124">Falso</span><span class="sxs-lookup"><span data-stu-id="04d06-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="04d06-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="04d06-125">See also</span></span>

- [<span data-ttu-id="04d06-126">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="04d06-126">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

