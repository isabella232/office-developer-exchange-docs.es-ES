---
title: Manifiestos
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 650d9fc0-1504-4db4-95d6-d3ba86df66ca
description: El elemento Manifests contiene una colección de manifiestos de aplicaciones codificadas en Base64 que se instalan para la cuenta de correo electrónico.
ms.openlocfilehash: 91239e2337f7a1886d8947f558a86110755a93df
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44450819"
---
# <a name="manifests"></a><span data-ttu-id="eb63f-103">Manifiestos</span><span class="sxs-lookup"><span data-stu-id="eb63f-103">Manifests</span></span>

<span data-ttu-id="eb63f-104">El elemento **Manifests** contiene una colección de manifiestos de aplicaciones codificadas en Base64 que se instalan para la cuenta de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="eb63f-104">The **Manifests** element contains a collection of base64-encoded app manifests that are installed for the email account.</span></span> 
  
```XML
<Manifests>
   <Manifest/>
</Manifests>
```

 <span data-ttu-id="eb63f-105">**ArrayOfAppManifestsType**</span><span class="sxs-lookup"><span data-stu-id="eb63f-105">**ArrayOfAppManifestsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb63f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="eb63f-106">Attributes and elements</span></span>

<span data-ttu-id="eb63f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="eb63f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb63f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="eb63f-108">Attributes</span></span>

<span data-ttu-id="eb63f-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="eb63f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eb63f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eb63f-110">Child elements</span></span>

[<span data-ttu-id="eb63f-111">Manifiesto</span><span class="sxs-lookup"><span data-stu-id="eb63f-111">Manifest</span></span>](manifest.md)
  
### <a name="parent-elements"></a><span data-ttu-id="eb63f-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="eb63f-112">Parent elements</span></span>

[<span data-ttu-id="eb63f-113">GetAppManifestsResponse</span><span class="sxs-lookup"><span data-stu-id="eb63f-113">GetAppManifestsResponse</span></span>](getappmanifestsresponse.md)
  
## <a name="remarks"></a><span data-ttu-id="eb63f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eb63f-114">Remarks</span></span>

<span data-ttu-id="eb63f-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="eb63f-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="eb63f-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="eb63f-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb63f-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="eb63f-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb63f-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb63f-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="eb63f-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="eb63f-119">Schema name</span></span>  <br/> |<span data-ttu-id="eb63f-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="eb63f-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="eb63f-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="eb63f-121">Validation file</span></span>  <br/> |<span data-ttu-id="eb63f-122">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="eb63f-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eb63f-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="eb63f-123">Can be empty</span></span>  <br/> ||
   

