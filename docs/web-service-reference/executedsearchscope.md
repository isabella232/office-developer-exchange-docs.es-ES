---
title: ExecutedSearchScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExecutedSearchScope
api_type:
- schema
ms.assetid: 2de5f0ad-43f2-4d38-b520-06540066564e
description: El elemento ExecutedSearchScope contiene el ámbito de la búsqueda que se llevó a cabo para obtener los resultados de búsqueda.
ms.openlocfilehash: ece9fdfc156cedad2a9fa181897145ae4eea20a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764483"
---
# <a name="executedsearchscope"></a><span data-ttu-id="eb381-103">ExecutedSearchScope</span><span class="sxs-lookup"><span data-stu-id="eb381-103">ExecutedSearchScope</span></span>

<span data-ttu-id="eb381-104">El elemento **ExecutedSearchScope** contiene el ámbito de la búsqueda que se llevó a cabo para obtener los resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="eb381-104">The **ExecutedSearchScope** element contains the scope of the search that was performed to get the search results.</span></span> 
  
```xml
<ExecutedSearchScope/>
```

 <span data-ttu-id="eb381-105">**String**</span><span class="sxs-lookup"><span data-stu-id="eb381-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb381-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="eb381-106">Attributes and elements</span></span>

<span data-ttu-id="eb381-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="eb381-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb381-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="eb381-108">Attributes</span></span>

<span data-ttu-id="eb381-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eb381-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eb381-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="eb381-110">Child elements</span></span>

<span data-ttu-id="eb381-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="eb381-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eb381-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="eb381-112">Parent elements</span></span>

|<span data-ttu-id="eb381-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="eb381-113">**Element**</span></span>|<span data-ttu-id="eb381-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eb381-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eb381-115">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="eb381-115">FindMessageTrackingReportResponse</span></span>](findmessagetrackingreportresponse.md) <br/> |<span data-ttu-id="eb381-116">Contiene el estado y el resultado de una única solicitud de [operación FindMessageTrackingReport](findmessagetrackingreport-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="eb381-116">Contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="eb381-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="eb381-117">Text value</span></span>

<span data-ttu-id="eb381-118">El valor de texto es opcional.</span><span class="sxs-lookup"><span data-stu-id="eb381-118">The text value is optional.</span></span> <span data-ttu-id="eb381-119">Esta información se usa en la aplicación cliente para almacenar en caché los resultados de la forma más eficaz.</span><span class="sxs-lookup"><span data-stu-id="eb381-119">This information is used by the client application to cache the results more effectively.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb381-120">Notas</span><span class="sxs-lookup"><span data-stu-id="eb381-120">Remarks</span></span>

<span data-ttu-id="eb381-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda Exchange Web Services.This elemento fue introdujo en Exchange Server 2010 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="eb381-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb381-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="eb381-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb381-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eb381-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="eb381-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="eb381-124">Schema Name</span></span>  <br/> |<span data-ttu-id="eb381-125">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="eb381-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="eb381-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="eb381-126">Validation File</span></span>  <br/> |<span data-ttu-id="eb381-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="eb381-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="eb381-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="eb381-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="eb381-129">False</span><span class="sxs-lookup"><span data-stu-id="eb381-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb381-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="eb381-130">See also</span></span>



[<span data-ttu-id="eb381-131">Operación FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="eb381-131">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="eb381-132">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="eb381-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

