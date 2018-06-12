---
title: SyncFolderItemsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderItemsResponse
api_type:
- schema
ms.assetid: 82fe0644-1756-40b2-955c-20c01110660c
description: El elemento SyncFolderItemsResponse define una respuesta a una solicitud de SyncFolderItems.
ms.openlocfilehash: e6145a1757d67c1d4a2e50b74204e4a79bdb6df9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840615"
---
# <a name="syncfolderitemsresponse"></a><span data-ttu-id="7b7d8-103">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="7b7d8-103">SyncFolderItemsResponse</span></span>

<span data-ttu-id="7b7d8-104">El elemento **SyncFolderItemsResponse** define una respuesta a una solicitud de SyncFolderItems.</span><span class="sxs-lookup"><span data-stu-id="7b7d8-104">The **SyncFolderItemsResponse** element defines a response to a SyncFolderItems request.</span></span> 
  
```xml
<SyncFolderItemsResponse>
   <ResponseMessages/>
</SyncFolderItemsResponse>
```

 <span data-ttu-id="7b7d8-105">**SyncFolderItemsResponseType**</span><span class="sxs-lookup"><span data-stu-id="7b7d8-105">**SyncFolderItemsResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7b7d8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7b7d8-106">Attributes and elements</span></span>

<span data-ttu-id="7b7d8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7b7d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b7d8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7b7d8-108">Attributes</span></span>

<span data-ttu-id="7b7d8-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7b7d8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7b7d8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7b7d8-110">Child elements</span></span>

|<span data-ttu-id="7b7d8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7b7d8-111">**Element**</span></span>|<span data-ttu-id="7b7d8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7b7d8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b7d8-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7b7d8-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="7b7d8-114">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="7b7d8-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7b7d8-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7b7d8-115">Parent elements</span></span>

<span data-ttu-id="7b7d8-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7b7d8-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7b7d8-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b7d8-117">Remarks</span></span>

<span data-ttu-id="7b7d8-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="7b7d8-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7b7d8-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7b7d8-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b7d8-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7b7d8-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7b7d8-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7b7d8-121">Schema name</span></span>  <br/> |<span data-ttu-id="7b7d8-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="7b7d8-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7b7d8-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7b7d8-123">Validation file</span></span>  <br/> |<span data-ttu-id="7b7d8-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7b7d8-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7b7d8-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7b7d8-125">Can be empty</span></span>  <br/> |<span data-ttu-id="7b7d8-126">False</span><span class="sxs-lookup"><span data-stu-id="7b7d8-126">False</span></span>  <br/> |
   

