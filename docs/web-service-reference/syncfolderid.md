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
description: El elemento SyncFolderId representa la carpeta que contiene los elementos que se van a sincronizar.
ms.openlocfilehash: 35b66579116a00d27df722629ff980471ca0272e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530299"
---
# <a name="syncfolderid"></a><span data-ttu-id="4cce9-103">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="4cce9-103">SyncFolderId</span></span>

<span data-ttu-id="4cce9-104">El elemento **SyncFolderId** representa la carpeta que contiene los elementos que se van a sincronizar.</span><span class="sxs-lookup"><span data-stu-id="4cce9-104">The **SyncFolderId** element represents the folder that contains the items to synchronize.</span></span> 
  
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

<span data-ttu-id="4cce9-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="4cce9-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4cce9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4cce9-106">Attributes and elements</span></span>

<span data-ttu-id="4cce9-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4cce9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4cce9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4cce9-108">Attributes</span></span>

<span data-ttu-id="4cce9-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="4cce9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4cce9-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4cce9-110">Child elements</span></span>

|<span data-ttu-id="4cce9-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4cce9-111">**Element**</span></span>|<span data-ttu-id="4cce9-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4cce9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4cce9-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="4cce9-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="4cce9-114">Contiene el identificador y la clave de cambio de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="4cce9-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="4cce9-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="4cce9-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="4cce9-116">Identifica las carpetas de MicrosoftExchange Server 2007 a las que se puede hacer referencia por su nombre.</span><span class="sxs-lookup"><span data-stu-id="4cce9-116">Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4cce9-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4cce9-117">Parent elements</span></span>

|<span data-ttu-id="4cce9-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4cce9-118">**Element**</span></span>|<span data-ttu-id="4cce9-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4cce9-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4cce9-120">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="4cce9-120">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md) <br/> |<span data-ttu-id="4cce9-121">Define una solicitud para sincronizar una jerarquía de carpetas en un almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4cce9-121">Defines a request to synchronize a folder hierarchy in an Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="4cce9-122">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="4cce9-122">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="4cce9-123">Define una solicitud para sincronizar elementos en una carpeta de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="4cce9-123">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cce9-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4cce9-124">Remarks</span></span>

<span data-ttu-id="4cce9-125">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="4cce9-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4cce9-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4cce9-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4cce9-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="4cce9-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4cce9-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4cce9-128">Schema name</span></span>  <br/> |<span data-ttu-id="4cce9-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="4cce9-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4cce9-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4cce9-130">Validation file</span></span>  <br/> |<span data-ttu-id="4cce9-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4cce9-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4cce9-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4cce9-132">Can be empty</span></span>  <br/> |<span data-ttu-id="4cce9-133">Falso</span><span class="sxs-lookup"><span data-stu-id="4cce9-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4cce9-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cce9-134">See also</span></span>

- [<span data-ttu-id="4cce9-135">Operación SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="4cce9-135">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)
- [<span data-ttu-id="4cce9-136">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4cce9-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

