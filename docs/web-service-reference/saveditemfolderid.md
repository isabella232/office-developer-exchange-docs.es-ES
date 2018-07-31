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
description: El elemento SavedItemFolderId identifica la carpeta de destino para las operaciones que actualizar, enviar y crear elementos en un buzón de correo.
ms.openlocfilehash: 3f46070a538f5e03007925565a8888efe06b62b7
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354165"
---
# <a name="saveditemfolderid"></a><span data-ttu-id="b6251-103">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="b6251-103">SavedItemFolderId</span></span>

<span data-ttu-id="b6251-104">El elemento **SavedItemFolderId** identifica la carpeta de destino para las operaciones que actualizar, enviar y crear elementos en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="b6251-104">The **SavedItemFolderId** element identifies the target folder for operations that update, send, and create items in a mailbox.</span></span> 
  
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

<span data-ttu-id="b6251-105">**TargetFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="b6251-105">**TargetFolderIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b6251-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b6251-106">Attributes and elements</span></span>

<span data-ttu-id="b6251-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b6251-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b6251-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b6251-108">Attributes</span></span>

<span data-ttu-id="b6251-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b6251-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b6251-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b6251-110">Child elements</span></span>

|<span data-ttu-id="b6251-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b6251-111">**Element**</span></span>|<span data-ttu-id="b6251-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b6251-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6251-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="b6251-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="b6251-114">Contiene el identificador y cambiar la clave de una carpeta de destino para las operaciones que actualizar, enviar y crear elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b6251-114">Contains the identifier and change key of a target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b6251-115">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="b6251-115">DistinguishedFolderId</span></span>](distinguishedfolderid.md) <br/> |<span data-ttu-id="b6251-116">Una carpeta de destino se identifica mediante un identificador con nombre para las operaciones que actualizar, enviar y crear elementos en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b6251-116">Identifies a target folder by a named identifier for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b6251-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b6251-117">Parent elements</span></span>

|<span data-ttu-id="b6251-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="b6251-118">**Element**</span></span>|<span data-ttu-id="b6251-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b6251-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6251-120">CreateItem</span><span class="sxs-lookup"><span data-stu-id="b6251-120">CreateItem</span></span>](createitem.md) <br/> |<span data-ttu-id="b6251-121">Define una solicitud para crear un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b6251-121">Defines a request to create an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="b6251-122">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="b6251-122">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateItem` <br/> |
|[<span data-ttu-id="b6251-123">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="b6251-123">UpdateItem</span></span>](updateitem.md) <br/> |<span data-ttu-id="b6251-124">Define una solicitud para actualizar un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b6251-124">Defines a request to update an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="b6251-125">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="b6251-125">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem` <br/> |
|[<span data-ttu-id="b6251-126">SendItem</span><span class="sxs-lookup"><span data-stu-id="b6251-126">SendItem</span></span>](senditem.md) <br/> |<span data-ttu-id="b6251-127">Define una solicitud para enviar un elemento en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b6251-127">Defines a request to send an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="b6251-128">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="b6251-128">The following is the XPath expression to this element:</span></span>  <br/>  `/SendItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6251-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b6251-129">Remarks</span></span>

<span data-ttu-id="b6251-130">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="b6251-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b6251-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b6251-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6251-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b6251-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b6251-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b6251-133">Schema Name</span></span>  <br/> |<span data-ttu-id="b6251-134">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="b6251-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b6251-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b6251-135">Validation File</span></span>  <br/> |<span data-ttu-id="b6251-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b6251-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b6251-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b6251-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="b6251-138">False</span><span class="sxs-lookup"><span data-stu-id="b6251-138">False</span></span>  <br/> |
   

