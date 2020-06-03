---
title: IncludePersonalArchive
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b373bb1a-6b1d-4959-98a1-4c4ea62973bc
description: El elemento IncludePersonalArchive especifica si se incluye el archivo personal en la búsqueda.
ms.openlocfilehash: a25dd45bc0717af8f949d14b88793af3821ca69f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458253"
---
# <a name="includepersonalarchive"></a><span data-ttu-id="5359c-103">IncludePersonalArchive</span><span class="sxs-lookup"><span data-stu-id="5359c-103">IncludePersonalArchive</span></span>

<span data-ttu-id="5359c-104">El elemento **IncludePersonalArchive** especifica si se incluye el archivo personal en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5359c-104">The **IncludePersonalArchive** element specifies whether to include the personal archive in the search.</span></span> 
  
```XML
<IncludePersonalArchive>true | false</IncludePersonalArchive>
```

 <span data-ttu-id="5359c-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="5359c-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5359c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5359c-106">Attributes and elements</span></span>

<span data-ttu-id="5359c-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5359c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5359c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5359c-108">Attributes</span></span>

<span data-ttu-id="5359c-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5359c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5359c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5359c-110">Child elements</span></span>

<span data-ttu-id="5359c-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5359c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5359c-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5359c-112">Parent elements</span></span>

|<span data-ttu-id="5359c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5359c-113">**Element**</span></span>|<span data-ttu-id="5359c-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5359c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5359c-115">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="5359c-115">FindMailboxStatisticsByKeywords</span></span>](findmailboxstatisticsbykeywords.md) <br/> |<span data-ttu-id="5359c-116">Especifica una solicitud para buscar estadísticas de buzón por palabra clave.</span><span class="sxs-lookup"><span data-stu-id="5359c-116">Specifies a request to search for mailbox statistics by keyword.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5359c-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5359c-117">Text value</span></span>

<span data-ttu-id="5359c-118">Un valor de texto de **true** para el elemento **IncludePersonalArchive** indica que el archivo personal se incluye en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5359c-118">A text value of **true** for the **IncludePersonalArchive** element indicates that the personal archive is included in the search.</span></span> <span data-ttu-id="5359c-119">Un valor de **false** indica que el archivo personal no se incluye en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5359c-119">A value of **false** indicates that the personal archive is not included in the search.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5359c-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5359c-120">Remarks</span></span>

<span data-ttu-id="5359c-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5359c-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5359c-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5359c-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5359c-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="5359c-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5359c-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5359c-124">Schema Name</span></span>  <br/> |<span data-ttu-id="5359c-125">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="5359c-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="5359c-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5359c-126">Validation File</span></span>  <br/> |<span data-ttu-id="5359c-127">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="5359c-127">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5359c-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5359c-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="5359c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5359c-129">See also</span></span>



- [<span data-ttu-id="5359c-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5359c-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

