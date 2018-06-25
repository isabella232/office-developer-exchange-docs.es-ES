---
title: DisableApp
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 42d2a888-fa62-4970-8306-9ddde4eeb1f0
description: El elemento DisableApp especifica una solicitud para deshabilitar una aplicación.
ms.openlocfilehash: d6d895d98fb368a6912f9111a4b934ba9631268e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764170"
---
# <a name="disableapp"></a><span data-ttu-id="dc64e-103">DisableApp</span><span class="sxs-lookup"><span data-stu-id="dc64e-103">DisableApp</span></span>

<span data-ttu-id="dc64e-104">El elemento **DisableApp** especifica una solicitud para deshabilitar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="dc64e-104">The **DisableApp** element specifies a request to disable an app.</span></span> 
  
```XML
<DisableApp>
    <ID></ID>
    <DisableReason></DisableReason>
</DisableApp>
```

 <span data-ttu-id="dc64e-105">**DisableAppType**</span><span class="sxs-lookup"><span data-stu-id="dc64e-105">**DisableAppType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc64e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="dc64e-106">Attributes and elements</span></span>

<span data-ttu-id="dc64e-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="dc64e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc64e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="dc64e-108">Attributes</span></span>

<span data-ttu-id="dc64e-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dc64e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc64e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dc64e-110">Child elements</span></span>

|<span data-ttu-id="dc64e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="dc64e-111">**Element**</span></span>|<span data-ttu-id="dc64e-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="dc64e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc64e-113">Identificador (cadena)</span><span class="sxs-lookup"><span data-stu-id="dc64e-113">ID (String)</span></span>](id-string.md) <br/> |<span data-ttu-id="dc64e-114">Especifica el identificador de un elemento.</span><span class="sxs-lookup"><span data-stu-id="dc64e-114">Specifies the identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="dc64e-115">DisableReason</span><span class="sxs-lookup"><span data-stu-id="dc64e-115">DisableReason</span></span>](disablereason.md) <br/> |<span data-ttu-id="dc64e-116">Especifica la razón para deshabilitar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="dc64e-116">Specifies the reason for disabling an app.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dc64e-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="dc64e-117">Parent elements</span></span>

<span data-ttu-id="dc64e-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="dc64e-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc64e-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dc64e-119">Remarks</span></span>

<span data-ttu-id="dc64e-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dc64e-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dc64e-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="dc64e-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc64e-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="dc64e-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc64e-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dc64e-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dc64e-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="dc64e-124">Schema Name</span></span>  <br/> |<span data-ttu-id="dc64e-125">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="dc64e-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="dc64e-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="dc64e-126">Validation File</span></span>  <br/> |<span data-ttu-id="dc64e-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dc64e-127">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dc64e-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="dc64e-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="dc64e-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc64e-129">See also</span></span>

- [<span data-ttu-id="dc64e-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="dc64e-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

