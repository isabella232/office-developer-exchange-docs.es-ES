---
title: SavedItemFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SavedItemFolderId
api_type:
- schema
ms.assetid: 4b8b475c-9ca5-48c9-acb0-8848b53be1ce
description: El elemento SavedItemFolderId identifica la carpeta de destino para las operaciones que actualizan, envían y crean elementos en un buzón.
ms.openlocfilehash: 8e18b8863a54aa4e9d6e65f7a54e20904f5a9599
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465278"
---
# <a name="saveditemfolderid"></a><span data-ttu-id="46635-103">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="46635-103">SavedItemFolderId</span></span>

<span data-ttu-id="46635-104">El elemento **SavedItemFolderId** identifica la carpeta de destino para las operaciones que actualizan, envían y crean elementos en un buzón.</span><span class="sxs-lookup"><span data-stu-id="46635-104">The **SavedItemFolderId** element identifies the target folder for operations that update, send, and create items in a mailbox.</span></span> 
  
```xml
<SavedItemFolderId>
   <FolderId/>
</SavedItemFolderId>
```

```xml
<SavedItemFolderId>
   <DistinguishedFolderId/>
</SavedItemFolderId>
```

<span data-ttu-id="46635-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="46635-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="46635-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="46635-106">Attributes and elements</span></span>

<span data-ttu-id="46635-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="46635-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="46635-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="46635-108">Attributes</span></span>

<span data-ttu-id="46635-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="46635-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="46635-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="46635-110">Child elements</span></span>

|<span data-ttu-id="46635-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="46635-111">**Element**</span></span>|<span data-ttu-id="46635-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="46635-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46635-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="46635-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="46635-114">Contiene el identificador y la clave de cambio de una carpeta de destino para las operaciones que actualizan, envían y crean elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="46635-114">Contains the identifier and change key of a target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="46635-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="46635-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="46635-116">Identifica una carpeta de destino mediante un identificador con nombre para las operaciones que actualizan, envían y crean elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="46635-116">Identifies a target folder by a named identifier for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="46635-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="46635-117">Parent elements</span></span>

|<span data-ttu-id="46635-118">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="46635-118">**Element**</span></span>|<span data-ttu-id="46635-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="46635-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46635-120">CreateItem</span><span class="sxs-lookup"><span data-stu-id="46635-120">CreateItem</span></span>](createitem.md) <br/> |<span data-ttu-id="46635-121">Define una solicitud para crear un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="46635-121">Defines a request to create an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="46635-122">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="46635-122">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateItem` <br/> |
|[<span data-ttu-id="46635-123">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="46635-123">UpdateItem</span></span>](updateitem.md) <br/> |<span data-ttu-id="46635-124">Define una solicitud para actualizar un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="46635-124">Defines a request to update an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="46635-125">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="46635-125">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem` <br/> |
|[<span data-ttu-id="46635-126">SendItem</span><span class="sxs-lookup"><span data-stu-id="46635-126">SendItem</span></span>](senditem.md) <br/> |<span data-ttu-id="46635-127">Define una solicitud para enviar un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="46635-127">Defines a request to send an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="46635-128">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="46635-128">The following is the XPath expression to this element:</span></span>  <br/>  `/SendItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46635-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="46635-129">Remarks</span></span>

<span data-ttu-id="46635-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="46635-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="46635-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="46635-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46635-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="46635-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="46635-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="46635-133">Schema Name</span></span>  <br/> |<span data-ttu-id="46635-134">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="46635-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="46635-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="46635-135">Validation File</span></span>  <br/> |<span data-ttu-id="46635-136">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="46635-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="46635-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="46635-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="46635-138">Falso</span><span class="sxs-lookup"><span data-stu-id="46635-138">False</span></span>  <br/> |
   

