---
title: ResultType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 488ee828-343f-4382-a5e8-eed1005f5dbc
description: El elemento ResultType contiene el tipo de búsqueda para llevar a cabo. El tipo de búsqueda puede ser sólo estadísticas o sólo vista previa.
ms.openlocfilehash: 750f53ae05a7ad9f5aefc9396911a23ef32cdfc2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837211"
---
# <a name="resulttype"></a><span data-ttu-id="6f487-104">ResultType</span><span class="sxs-lookup"><span data-stu-id="6f487-104">ResultType</span></span>

<span data-ttu-id="6f487-105">El elemento **ResultType** contiene el tipo de búsqueda para llevar a cabo.</span><span class="sxs-lookup"><span data-stu-id="6f487-105">The **ResultType** element contains the type of search to perform.</span></span> <span data-ttu-id="6f487-106">El tipo de búsqueda puede ser sólo estadísticas o sólo vista previa.</span><span class="sxs-lookup"><span data-stu-id="6f487-106">The type of search can be statistics only or preview only.</span></span> 
  
```XML
<ResultType>StatisticsOnly | PreviewOnly</ResultType>
```

 <span data-ttu-id="6f487-107">**SearchResultType**</span><span class="sxs-lookup"><span data-stu-id="6f487-107">**SearchResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f487-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6f487-108">Attributes and elements</span></span>

<span data-ttu-id="6f487-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6f487-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f487-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="6f487-110">Attributes</span></span>

<span data-ttu-id="6f487-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6f487-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f487-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6f487-112">Child elements</span></span>

<span data-ttu-id="6f487-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6f487-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6f487-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6f487-114">Parent elements</span></span>

<span data-ttu-id="6f487-115">[SearchMailboxesResult](searchmailboxesresult.md) | [SearchMailboxes](searchmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="6f487-115">[SearchMailboxesResult](searchmailboxesresult.md) | [SearchMailboxes](searchmailboxes.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="6f487-116">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6f487-116">Text value</span></span>

<span data-ttu-id="6f487-117">El valor de texto del elemento **ResultType** es el tipo de resultado que se devuelve para una búsqueda de detección.</span><span class="sxs-lookup"><span data-stu-id="6f487-117">The text value of the **ResultType** element is the type of result that is returned for a discovery search.</span></span> <span data-ttu-id="6f487-118">Un valor de texto de **StatisticsOnly** devolverá las estadísticas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6f487-118">A text value of **StatisticsOnly** will return the search statistics.</span></span> <span data-ttu-id="6f487-119">Un valor de texto de **PreviewOnly** devolverá información de vista previa del elemento.</span><span class="sxs-lookup"><span data-stu-id="6f487-119">A text value of **PreviewOnly** will return item preview information.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6f487-120">Notas</span><span class="sxs-lookup"><span data-stu-id="6f487-120">Remarks</span></span>

<span data-ttu-id="6f487-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6f487-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6f487-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6f487-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f487-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6f487-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f487-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6f487-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6f487-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6f487-125">Schema name</span></span>  <br/> |<span data-ttu-id="6f487-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="6f487-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6f487-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6f487-127">Validation file</span></span>  <br/> |<span data-ttu-id="6f487-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6f487-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6f487-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6f487-129">Can be empty</span></span>  <br/> |<span data-ttu-id="6f487-130">falso</span><span class="sxs-lookup"><span data-stu-id="6f487-130">false</span></span>  <br/> |
   

