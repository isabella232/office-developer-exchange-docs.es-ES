---
title: SyncFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderId
api_type:
- schema
ms.assetid: 3645fa03-236d-4e5f-b8b9-5d98f7f35fa2
description: El elemento SyncFolderId representa la carpeta que contiene los elementos para sincronizar.
ms.openlocfilehash: c90a20095ca4706f0c6edae3e98eaadd6024d817
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354403"
---
# <a name="syncfolderid"></a><span data-ttu-id="3793c-103">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="3793c-103">SyncFolderId</span></span>

<span data-ttu-id="3793c-104">El elemento **SyncFolderId** representa la carpeta que contiene los elementos para sincronizar.</span><span class="sxs-lookup"><span data-stu-id="3793c-104">The **SyncFolderId** element represents the folder that contains the items to synchronize.</span></span> 
  
```xml
<SyncFolderId>
   <FolderId/>
</SyncFolderId>
```

```xml
<SyncFolderId>
   <DistinguishedFolderId/> 
</SyncFolderId>
```

<span data-ttu-id="3793c-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="3793c-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3793c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3793c-106">Attributes and elements</span></span>

<span data-ttu-id="3793c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3793c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3793c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3793c-108">Attributes</span></span>

<span data-ttu-id="3793c-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3793c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3793c-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3793c-110">Child elements</span></span>

|<span data-ttu-id="3793c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3793c-111">**Element**</span></span>|<span data-ttu-id="3793c-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3793c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3793c-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="3793c-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="3793c-114">Contiene el identificador y cambiar la clave de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="3793c-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="3793c-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="3793c-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="3793c-116">Identifica las carpetas de MicrosoftExchange Server 2007 que se pueden hacer referencia por su nombre.</span><span class="sxs-lookup"><span data-stu-id="3793c-116">Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3793c-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3793c-117">Parent elements</span></span>

|<span data-ttu-id="3793c-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="3793c-118">**Element**</span></span>|<span data-ttu-id="3793c-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3793c-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3793c-120">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="3793c-120">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md) <br/> |<span data-ttu-id="3793c-121">Define una solicitud para sincronizar una jerarquía de carpetas en un almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3793c-121">Defines a request to synchronize a folder hierarchy in an Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3793c-122">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="3793c-122">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="3793c-123">Define una solicitud para sincronizar los elementos en una carpeta de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="3793c-123">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3793c-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3793c-124">Remarks</span></span>

<span data-ttu-id="3793c-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3793c-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3793c-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3793c-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3793c-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3793c-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3793c-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3793c-128">Schema name</span></span>  <br/> |<span data-ttu-id="3793c-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="3793c-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3793c-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3793c-130">Validation file</span></span>  <br/> |<span data-ttu-id="3793c-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3793c-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3793c-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3793c-132">Can be empty</span></span>  <br/> |<span data-ttu-id="3793c-133">False</span><span class="sxs-lookup"><span data-stu-id="3793c-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3793c-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3793c-134">See also</span></span>

- [<span data-ttu-id="3793c-135">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="3793c-135">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="3793c-136">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3793c-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

