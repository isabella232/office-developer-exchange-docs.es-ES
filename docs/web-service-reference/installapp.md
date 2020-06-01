---
title: InstallApp
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fc2ca69e-eea7-4334-b046-ec0b04d8f8c6
description: El elemento InstallApp especifica la solicitud de instalar una aplicación.
ms.openlocfilehash: 003a72507813677484b2d6ee75f8ff577df169e3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468008"
---
# <a name="installapp"></a><span data-ttu-id="0970d-103">InstallApp</span><span class="sxs-lookup"><span data-stu-id="0970d-103">InstallApp</span></span>

<span data-ttu-id="0970d-104">El elemento **InstallApp** especifica la solicitud de instalar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="0970d-104">The **InstallApp** element specifies the request to install an app.</span></span> 
  
```XML
<InstallApp>
    <Manifest/>
</InstallApp>
```

 <span data-ttu-id="0970d-105">**InstallAppType**</span><span class="sxs-lookup"><span data-stu-id="0970d-105">**InstallAppType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0970d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0970d-106">Attributes and elements</span></span>

<span data-ttu-id="0970d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0970d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0970d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0970d-108">Attributes</span></span>

<span data-ttu-id="0970d-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0970d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0970d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0970d-110">Child elements</span></span>

|<span data-ttu-id="0970d-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0970d-111">**Element**</span></span>|<span data-ttu-id="0970d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0970d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0970d-113">Manifiesto</span><span class="sxs-lookup"><span data-stu-id="0970d-113">Manifest</span></span>](manifest.md) <br/> |<span data-ttu-id="0970d-114">Contiene el archivo de manifiesto de la aplicación con codificación Base64.</span><span class="sxs-lookup"><span data-stu-id="0970d-114">Contains the base64-encoded app manifest file.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0970d-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0970d-115">Parent elements</span></span>

<span data-ttu-id="0970d-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0970d-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0970d-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0970d-117">Remarks</span></span>

<span data-ttu-id="0970d-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0970d-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0970d-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0970d-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0970d-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0970d-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0970d-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="0970d-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0970d-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0970d-122">Schema Name</span></span>  <br/> |<span data-ttu-id="0970d-123">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="0970d-123">Message schema</span></span>  <br/> |
|<span data-ttu-id="0970d-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0970d-124">Validation File</span></span>  <br/> |<span data-ttu-id="0970d-125">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0970d-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0970d-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0970d-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="0970d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0970d-127">See also</span></span>



- [<span data-ttu-id="0970d-128">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="0970d-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

