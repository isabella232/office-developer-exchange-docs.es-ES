---
title: SyncFolderHierarchyResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchyResponse
api_type:
- schema
ms.assetid: 7e6061d2-bbce-4864-a7bb-a6457628cb7c
description: El elemento SyncFolderHierarchyResponse define una respuesta a una solicitud de SyncFolderHierarchy.
ms.openlocfilehash: aee70603b84dfdf5f7f580fd2566f7ebfbbce383
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19840612"
---
# <a name="syncfolderhierarchyresponse"></a><span data-ttu-id="3b31f-103">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="3b31f-103">SyncFolderHierarchyResponse</span></span>

<span data-ttu-id="3b31f-104">El elemento **SyncFolderHierarchyResponse** define una respuesta a una solicitud de SyncFolderHierarchy.</span><span class="sxs-lookup"><span data-stu-id="3b31f-104">The **SyncFolderHierarchyResponse** element defines a response to a SyncFolderHierarchy request.</span></span> 
  
```xml
<SyncFolderHierarchyResponse>
   <ResponseMessages/>
</SyncFolderHierarchyResponse>
```

 <span data-ttu-id="3b31f-105">**SyncFolderHierarchyResponseType**</span><span class="sxs-lookup"><span data-stu-id="3b31f-105">**SyncFolderHierarchyResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3b31f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3b31f-106">Attributes and elements</span></span>

<span data-ttu-id="3b31f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3b31f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b31f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3b31f-108">Attributes</span></span>

<span data-ttu-id="3b31f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3b31f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3b31f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3b31f-110">Child elements</span></span>

|<span data-ttu-id="3b31f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3b31f-111">**Element**</span></span>|<span data-ttu-id="3b31f-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3b31f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b31f-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3b31f-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="3b31f-114">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3b31f-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3b31f-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3b31f-115">Parent elements</span></span>

<span data-ttu-id="3b31f-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3b31f-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3b31f-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3b31f-117">Remarks</span></span>

<span data-ttu-id="3b31f-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3b31f-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3b31f-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3b31f-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b31f-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3b31f-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3b31f-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3b31f-121">Schema name</span></span>  <br/> |<span data-ttu-id="3b31f-122">esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3b31f-122">messages schema</span></span>  <br/> |
|<span data-ttu-id="3b31f-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3b31f-123">Validation file</span></span>  <br/> |<span data-ttu-id="3b31f-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3b31f-124">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3b31f-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3b31f-125">Can be empty</span></span>  <br/> |<span data-ttu-id="3b31f-126">False</span><span class="sxs-lookup"><span data-stu-id="3b31f-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b31f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b31f-127">See also</span></span>



[<span data-ttu-id="3b31f-128">Operación SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="3b31f-128">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


- [<span data-ttu-id="3b31f-129">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3b31f-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

