---
title: IncludePersonalArchive
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b373bb1a-6b1d-4959-98a1-4c4ea62973bc
description: El elemento IncludePersonalArchive especifica si se debe incluir el archivo personal en la búsqueda.
ms.openlocfilehash: ba2dcaae3befd3595815c7281858e4fa8a738e0a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835905"
---
# <a name="includepersonalarchive"></a><span data-ttu-id="bcb78-103">IncludePersonalArchive</span><span class="sxs-lookup"><span data-stu-id="bcb78-103">IncludePersonalArchive</span></span>

<span data-ttu-id="bcb78-104">El elemento **IncludePersonalArchive** especifica si se debe incluir el archivo personal en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="bcb78-104">The **IncludePersonalArchive** element specifies whether to include the personal archive in the search.</span></span> 
  
```XML
<IncludePersonalArchive>true | false</IncludePersonalArchive>
```

 <span data-ttu-id="bcb78-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="bcb78-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bcb78-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="bcb78-106">Attributes and elements</span></span>

<span data-ttu-id="bcb78-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="bcb78-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bcb78-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="bcb78-108">Attributes</span></span>

<span data-ttu-id="bcb78-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bcb78-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bcb78-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bcb78-110">Child elements</span></span>

<span data-ttu-id="bcb78-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="bcb78-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bcb78-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="bcb78-112">Parent elements</span></span>

|<span data-ttu-id="bcb78-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="bcb78-113">**Element**</span></span>|<span data-ttu-id="bcb78-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bcb78-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bcb78-115">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="bcb78-115">FindMailboxStatisticsByKeywords</span></span>](findmailboxstatisticsbykeywords.md) <br/> |<span data-ttu-id="bcb78-116">Especifica una solicitud para buscar las estadísticas de buzón de correo por palabra clave.</span><span class="sxs-lookup"><span data-stu-id="bcb78-116">Specifies a request to search for mailbox statistics by keyword.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bcb78-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="bcb78-117">Text value</span></span>

<span data-ttu-id="bcb78-118">Un valor de texto de **true** para el elemento **IncludePersonalArchive** indica que el archivo personal está incluido en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="bcb78-118">A text value of **true** for the **IncludePersonalArchive** element indicates that the personal archive is included in the search.</span></span> <span data-ttu-id="bcb78-119">Un valor de **false** indica que el archivo personal no se incluye en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="bcb78-119">A value of **false** indicates that the personal archive is not included in the search.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bcb78-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bcb78-120">Remarks</span></span>

<span data-ttu-id="bcb78-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="bcb78-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bcb78-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="bcb78-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bcb78-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bcb78-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bcb78-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="bcb78-124">Schema Name</span></span>  <br/> |<span data-ttu-id="bcb78-125">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="bcb78-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="bcb78-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="bcb78-126">Validation File</span></span>  <br/> |<span data-ttu-id="bcb78-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bcb78-127">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bcb78-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="bcb78-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="bcb78-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcb78-129">See also</span></span>



- [<span data-ttu-id="bcb78-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="bcb78-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

