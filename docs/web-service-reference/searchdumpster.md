---
title: SearchDumpster
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ddb62dce-c87a-4714-8023-a6b697a29699
description: El elemento SearchDumpster especifica si se debe buscar en el contenedor de Exchange.
ms.openlocfilehash: 067bf8ea3e589aa392c6b8ba6d4dc10b430c1f28
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460494"
---
# <a name="searchdumpster"></a><span data-ttu-id="0e38f-103">SearchDumpster</span><span class="sxs-lookup"><span data-stu-id="0e38f-103">SearchDumpster</span></span>

<span data-ttu-id="0e38f-104">El elemento **SearchDumpster** especifica si se debe buscar en el contenedor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0e38f-104">The **SearchDumpster** element specifies whether to search in the Exchange Dumpster.</span></span> 
  
```XML
<SearchDumpster> true | false </SearchDumpster>
```

 ****
## <a name="attributes-and-elements"></a><span data-ttu-id="0e38f-105">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0e38f-105">Attributes and elements</span></span>

<span data-ttu-id="0e38f-106">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0e38f-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0e38f-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="0e38f-107">Attributes</span></span>

<span data-ttu-id="0e38f-108">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0e38f-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0e38f-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0e38f-109">Child elements</span></span>

<span data-ttu-id="0e38f-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0e38f-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0e38f-111">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0e38f-111">Parent elements</span></span>

[<span data-ttu-id="0e38f-112">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="0e38f-112">FindMailboxStatisticsByKeywords</span></span>](findmailboxstatisticsbykeywords.md)
  
## <a name="text-value"></a><span data-ttu-id="0e38f-113">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0e38f-113">Text value</span></span>

<span data-ttu-id="0e38f-114">Un valor de texto de **true** para el elemento **SearchDumpster** indica que la búsqueda de estadísticas de buzón incluye el contenedor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0e38f-114">A text value of **true** for the **SearchDumpster** element indicates that the mailbox statistics search includes the Exchange Dumpster.</span></span> <span data-ttu-id="0e38f-115">Un valor de **false** indica que no se busca en el contenedor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0e38f-115">A value of **false** indicates that the Exchange Dumpster is not searched.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0e38f-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0e38f-116">Remarks</span></span>

<span data-ttu-id="0e38f-117">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0e38f-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0e38f-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0e38f-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0e38f-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0e38f-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e38f-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="0e38f-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0e38f-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0e38f-121">Schema name</span></span>  <br/> |<span data-ttu-id="0e38f-122">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0e38f-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="0e38f-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0e38f-123">Validation file</span></span>  <br/> |<span data-ttu-id="0e38f-124">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="0e38f-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0e38f-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0e38f-125">Can be empty</span></span>  <br/> ||
   

