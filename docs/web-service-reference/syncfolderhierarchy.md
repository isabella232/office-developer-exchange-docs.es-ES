---
title: SyncFolderHierarchy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchy
api_type:
- schema
ms.assetid: 55df4d01-e48e-4263-a851-78a66ad1093a
description: El elemento SyncFolderHierarchy define una solicitud para sincronizar una jerarquía de carpetas en un cliente.
ms.openlocfilehash: 68b607dbf603e955f74dfaccadd3ce6c4c9fb6ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466650"
---
# <a name="syncfolderhierarchy"></a><span data-ttu-id="478cb-103">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="478cb-103">SyncFolderHierarchy</span></span>

<span data-ttu-id="478cb-104">El elemento **SyncFolderHierarchy** define una solicitud para sincronizar una jerarquía de carpetas en un cliente.</span><span class="sxs-lookup"><span data-stu-id="478cb-104">The **SyncFolderHierarchy** element defines a request to synchronize a folder hierarchy on a client.</span></span> 
  
```xml
<SyncFolderHierarchy>
   <FolderShape/>   <SyncFolderId/>
   <SyncState/>
</SyncFolderHierarchy>
```

 <span data-ttu-id="478cb-105">**SyncFolderHierarchyType**</span><span class="sxs-lookup"><span data-stu-id="478cb-105">**SyncFolderHierarchyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="478cb-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="478cb-106">Attributes and elements</span></span>

<span data-ttu-id="478cb-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="478cb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="478cb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="478cb-108">Attributes</span></span>

<span data-ttu-id="478cb-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="478cb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="478cb-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="478cb-110">Child elements</span></span>

|<span data-ttu-id="478cb-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="478cb-111">**Element**</span></span>|<span data-ttu-id="478cb-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="478cb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="478cb-113">FolderShape</span><span class="sxs-lookup"><span data-stu-id="478cb-113">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="478cb-114">Identifica las propiedades de carpeta que se deben incluir en una respuesta [SyncFolderHierarchy](syncfolderhierarchy.md) .</span><span class="sxs-lookup"><span data-stu-id="478cb-114">Identifies the folder properties to include in a [SyncFolderHierarchy](syncfolderhierarchy.md) response.</span></span>  <br/> |
|[<span data-ttu-id="478cb-115">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="478cb-115">SyncFolderId</span></span>](syncfolderid.md) <br/> |<span data-ttu-id="478cb-116">Representa la carpeta que contiene los elementos que se van a sincronizar.</span><span class="sxs-lookup"><span data-stu-id="478cb-116">Represents the folder that contains the items to synchronize.</span></span> <span data-ttu-id="478cb-117">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="478cb-117">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="478cb-118">SyncState</span><span class="sxs-lookup"><span data-stu-id="478cb-118">SyncState</span></span>](syncstate-ex15websvcsotherref.md) <br/> |<span data-ttu-id="478cb-119">Contiene una forma codificada en Base64 de los datos de sincronización que se actualizan después de cada solicitud correcta.</span><span class="sxs-lookup"><span data-stu-id="478cb-119">Contains a base64-encoded form of the synchronization data that is updated after each successful request.</span></span> <span data-ttu-id="478cb-120">Se usa para identificar el estado de sincronización.</span><span class="sxs-lookup"><span data-stu-id="478cb-120">This is used to identify the synchronization state.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="478cb-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="478cb-121">Parent elements</span></span>

<span data-ttu-id="478cb-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="478cb-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="478cb-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="478cb-123">Remarks</span></span>

<span data-ttu-id="478cb-124">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="478cb-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="478cb-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="478cb-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="478cb-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="478cb-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="478cb-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="478cb-127">Schema name</span></span>  <br/> |<span data-ttu-id="478cb-128">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="478cb-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="478cb-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="478cb-129">Validation file</span></span>  <br/> |<span data-ttu-id="478cb-130">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="478cb-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="478cb-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="478cb-131">Can be empty</span></span>  <br/> |<span data-ttu-id="478cb-132">Falso</span><span class="sxs-lookup"><span data-stu-id="478cb-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="478cb-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="478cb-133">See also</span></span>



[<span data-ttu-id="478cb-134">Operación SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="478cb-134">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


- [<span data-ttu-id="478cb-135">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="478cb-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

