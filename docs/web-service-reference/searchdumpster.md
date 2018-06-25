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
ms.openlocfilehash: 4a40ee2da7fdaa4eaa3f5349545a0bfd3e13ba73
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837283"
---
# <a name="searchdumpster"></a><span data-ttu-id="0640a-103">SearchDumpster</span><span class="sxs-lookup"><span data-stu-id="0640a-103">SearchDumpster</span></span>

<span data-ttu-id="0640a-104">El elemento **SearchDumpster** especifica si se debe buscar en el contenedor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0640a-104">The **SearchDumpster** element specifies whether to search in the Exchange Dumpster.</span></span> 
  
```XML
<SearchDumpster> true | false </SearchDumpster>
```

 ****
## <a name="attributes-and-elements"></a><span data-ttu-id="0640a-105">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0640a-105">Attributes and elements</span></span>

<span data-ttu-id="0640a-106">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0640a-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0640a-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="0640a-107">Attributes</span></span>

<span data-ttu-id="0640a-108">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0640a-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0640a-109">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0640a-109">Child elements</span></span>

<span data-ttu-id="0640a-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="0640a-110">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0640a-111">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0640a-111">Parent elements</span></span>

[<span data-ttu-id="0640a-112">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="0640a-112">FindMailboxStatisticsByKeywords</span></span>](findmailboxstatisticsbykeywords.md)
  
## <a name="text-value"></a><span data-ttu-id="0640a-113">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0640a-113">Text value</span></span>

<span data-ttu-id="0640a-114">Un valor de texto de **true** para el elemento **SearchDumpster** indica que la búsqueda de estadísticas de buzón incluye el contenedor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0640a-114">A text value of **true** for the **SearchDumpster** element indicates that the mailbox statistics search includes the Exchange Dumpster.</span></span> <span data-ttu-id="0640a-115">Un valor de **false** indica que no se busca en el contenedor de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0640a-115">A value of **false** indicates that the Exchange Dumpster is not searched.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0640a-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0640a-116">Remarks</span></span>

<span data-ttu-id="0640a-117">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="0640a-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0640a-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="0640a-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0640a-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0640a-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0640a-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0640a-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0640a-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0640a-121">Schema name</span></span>  <br/> |<span data-ttu-id="0640a-122">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="0640a-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="0640a-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0640a-123">Validation file</span></span>  <br/> |<span data-ttu-id="0640a-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0640a-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0640a-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0640a-125">Can be empty</span></span>  <br/> ||
   

