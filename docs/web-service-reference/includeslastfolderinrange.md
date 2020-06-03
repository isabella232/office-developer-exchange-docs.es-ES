---
title: IncludesLastFolderInRange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IncludesLastFolderInRange
api_type:
- schema
ms.assetid: 95837904-17be-49b7-831c-de4fb20fccfb
description: El elemento IncludesLastFolderInRange indica si el último elemento que se va a sincronizar se ha incluido en la respuesta.
ms.openlocfilehash: 9ba401cf639ef7988fa7a1437a64d09ff54c5960
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466454"
---
# <a name="includeslastfolderinrange"></a><span data-ttu-id="89773-103">IncludesLastFolderInRange</span><span class="sxs-lookup"><span data-stu-id="89773-103">IncludesLastFolderInRange</span></span>

<span data-ttu-id="89773-104">El elemento **IncludesLastFolderInRange** indica si el último elemento que se va a sincronizar se ha incluido en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="89773-104">The **IncludesLastFolderInRange** element indicates whether the last item to synchronize has been included in the response.</span></span> 
  
[<span data-ttu-id="89773-105">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="89773-105">SyncFolderHierarchyResponse</span></span>](syncfolderhierarchyresponse.md)
  
[<span data-ttu-id="89773-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="89773-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="89773-107">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="89773-107">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md)
  
[<span data-ttu-id="89773-108">IncludesLastFolderInRange</span><span class="sxs-lookup"><span data-stu-id="89773-108">IncludesLastFolderInRange</span></span>](includeslastfolderinrange.md)
  
```xml
<IncludesLastFolderInRange/>
```

 <span data-ttu-id="89773-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="89773-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="89773-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="89773-110">Attributes and elements</span></span>

<span data-ttu-id="89773-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="89773-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="89773-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="89773-112">Attributes</span></span>

<span data-ttu-id="89773-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="89773-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="89773-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="89773-114">Child elements</span></span>

<span data-ttu-id="89773-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="89773-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="89773-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="89773-116">Parent elements</span></span>

|<span data-ttu-id="89773-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="89773-117">**Element**</span></span>|<span data-ttu-id="89773-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="89773-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="89773-119">SyncFolderHierarchyResponseMessage</span><span class="sxs-lookup"><span data-stu-id="89773-119">SyncFolderHierarchyResponseMessage</span></span>](syncfolderhierarchyresponsemessage.md) <br/> |<span data-ttu-id="89773-120">Contiene el estado y el resultado de una solicitud SyncFolderHierarchy.</span><span class="sxs-lookup"><span data-stu-id="89773-120">Contains the status and result of a SyncFolderHierarchy request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="89773-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="89773-121">Text value</span></span>

<span data-ttu-id="89773-122">Se requiere un valor de texto que representa un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="89773-122">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="89773-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="89773-123">Remarks</span></span>

<span data-ttu-id="89773-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="89773-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="89773-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="89773-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="89773-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="89773-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="89773-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="89773-127">Schema name</span></span>  <br/> |<span data-ttu-id="89773-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="89773-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="89773-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="89773-129">Validation file</span></span>  <br/> |<span data-ttu-id="89773-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="89773-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="89773-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="89773-131">Can be empty</span></span>  <br/> |<span data-ttu-id="89773-132">Falso</span><span class="sxs-lookup"><span data-stu-id="89773-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89773-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="89773-133">See also</span></span>



[<span data-ttu-id="89773-134">Operación SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="89773-134">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


[<span data-ttu-id="89773-135">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="89773-135">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
  
- [<span data-ttu-id="89773-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="89773-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

