---
title: InstallApp
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fc2ca69e-eea7-4334-b046-ec0b04d8f8c6
description: El elemento InstallApp especifica la solicitud para instalar una aplicación.
ms.openlocfilehash: d9b7412865c003b89eccbdd92aa6ff9968048191
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835949"
---
# <a name="installapp"></a><span data-ttu-id="aaed1-103">InstallApp</span><span class="sxs-lookup"><span data-stu-id="aaed1-103">InstallApp</span></span>

<span data-ttu-id="aaed1-104">El elemento **InstallApp** especifica la solicitud para instalar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="aaed1-104">The **InstallApp** element specifies the request to install an app.</span></span> 
  
```XML
<InstallApp>
    <Manifest/>
</InstallApp>
```

 <span data-ttu-id="aaed1-105">**InstallAppType**</span><span class="sxs-lookup"><span data-stu-id="aaed1-105">**InstallAppType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aaed1-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="aaed1-106">Attributes and elements</span></span>

<span data-ttu-id="aaed1-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="aaed1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aaed1-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="aaed1-108">Attributes</span></span>

<span data-ttu-id="aaed1-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aaed1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aaed1-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="aaed1-110">Child elements</span></span>

|<span data-ttu-id="aaed1-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="aaed1-111">**Element**</span></span>|<span data-ttu-id="aaed1-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aaed1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aaed1-113">Manifest</span><span class="sxs-lookup"><span data-stu-id="aaed1-113">Manifest</span></span>](manifest.md) <br/> |<span data-ttu-id="aaed1-114">Contiene el archivo de manifiesto de aplicación con codificación base64.</span><span class="sxs-lookup"><span data-stu-id="aaed1-114">Contains the base64-encoded app manifest file.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aaed1-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="aaed1-115">Parent elements</span></span>

<span data-ttu-id="aaed1-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="aaed1-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aaed1-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aaed1-117">Remarks</span></span>

<span data-ttu-id="aaed1-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="aaed1-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="aaed1-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="aaed1-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aaed1-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="aaed1-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aaed1-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aaed1-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="aaed1-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="aaed1-122">Schema Name</span></span>  <br/> |<span data-ttu-id="aaed1-123">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="aaed1-123">Message schema</span></span>  <br/> |
|<span data-ttu-id="aaed1-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="aaed1-124">Validation File</span></span>  <br/> |<span data-ttu-id="aaed1-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="aaed1-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="aaed1-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="aaed1-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="aaed1-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="aaed1-127">See also</span></span>



- [<span data-ttu-id="aaed1-128">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="aaed1-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

