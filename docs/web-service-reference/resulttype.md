---
title: ResultType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 488ee828-343f-4382-a5e8-eed1005f5dbc
description: El elemento ResultType contiene el tipo de búsqueda que se va a realizar. El tipo de búsqueda solo puede ser estadística o solo vista previa.
ms.openlocfilehash: 6617c8b4b64cd9b6728317d7247bcc5378e488f0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465285"
---
# <a name="resulttype"></a><span data-ttu-id="b0119-104">ResultType</span><span class="sxs-lookup"><span data-stu-id="b0119-104">ResultType</span></span>

<span data-ttu-id="b0119-105">El elemento **ResultType** contiene el tipo de búsqueda que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="b0119-105">The **ResultType** element contains the type of search to perform.</span></span> <span data-ttu-id="b0119-106">El tipo de búsqueda solo puede ser estadística o solo vista previa.</span><span class="sxs-lookup"><span data-stu-id="b0119-106">The type of search can be statistics only or preview only.</span></span> 
  
```XML
<ResultType>StatisticsOnly | PreviewOnly</ResultType>
```

 <span data-ttu-id="b0119-107">**SearchResultType**</span><span class="sxs-lookup"><span data-stu-id="b0119-107">**SearchResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b0119-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b0119-108">Attributes and elements</span></span>

<span data-ttu-id="b0119-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b0119-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b0119-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="b0119-110">Attributes</span></span>

<span data-ttu-id="b0119-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b0119-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b0119-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b0119-112">Child elements</span></span>

<span data-ttu-id="b0119-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b0119-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b0119-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b0119-114">Parent elements</span></span>

<span data-ttu-id="b0119-115">[SearchMailboxesResult](searchmailboxesresult.md)  |  [SearchMailboxes](searchmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="b0119-115">[SearchMailboxesResult](searchmailboxesresult.md) | [SearchMailboxes](searchmailboxes.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="b0119-116">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b0119-116">Text value</span></span>

<span data-ttu-id="b0119-117">El valor de texto del elemento **ResultType** es el tipo de resultado que se devuelve para una búsqueda de detección.</span><span class="sxs-lookup"><span data-stu-id="b0119-117">The text value of the **ResultType** element is the type of result that is returned for a discovery search.</span></span> <span data-ttu-id="b0119-118">Un valor de texto de **StatisticsOnly** devolverá las estadísticas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="b0119-118">A text value of **StatisticsOnly** will return the search statistics.</span></span> <span data-ttu-id="b0119-119">Un valor de texto de **PreviewOnly** devolverá información de la vista previa del elemento.</span><span class="sxs-lookup"><span data-stu-id="b0119-119">A text value of **PreviewOnly** will return item preview information.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b0119-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0119-120">Remarks</span></span>

<span data-ttu-id="b0119-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="b0119-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b0119-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b0119-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b0119-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b0119-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0119-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0119-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b0119-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b0119-125">Schema name</span></span>  <br/> |<span data-ttu-id="b0119-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b0119-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b0119-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b0119-127">Validation file</span></span>  <br/> |<span data-ttu-id="b0119-128">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b0119-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b0119-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b0119-129">Can be empty</span></span>  <br/> |<span data-ttu-id="b0119-130">false</span><span class="sxs-lookup"><span data-stu-id="b0119-130">false</span></span>  <br/> |
   

