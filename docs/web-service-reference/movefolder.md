---
title: MoveFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveFolder
api_type:
- schema
ms.assetid: f2bb0a73-94d7-4bc7-8902-bd9c69120221
description: El elemento MoveFolder define una solicitud para mover una carpeta en el almacén de Exchange.
ms.openlocfilehash: d2fe33a6d7893d45fa116a1516fcc6ab2dea3bcf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457294"
---
# <a name="movefolder"></a><span data-ttu-id="f1862-103">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="f1862-103">MoveFolder</span></span>

<span data-ttu-id="f1862-104">El elemento **MoveFolder** define una solicitud para mover una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f1862-104">The **MoveFolder** element defines a request to move a folder in the Exchange store.</span></span> 
  
```xml
<MoveFolder>
   <ToFolderId/>
   <FolderIds/>
</MoveFolder>
```

 <span data-ttu-id="f1862-105">**MoveFolderType**</span><span class="sxs-lookup"><span data-stu-id="f1862-105">**MoveFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f1862-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f1862-106">Attributes and elements</span></span>

<span data-ttu-id="f1862-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f1862-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1862-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f1862-108">Attributes</span></span>

<span data-ttu-id="f1862-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="f1862-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f1862-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f1862-110">Child elements</span></span>

|<span data-ttu-id="f1862-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f1862-111">**Element**</span></span>|<span data-ttu-id="f1862-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f1862-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f1862-113">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="f1862-113">ToFolderId</span></span>](tofolderid.md) <br/> |<span data-ttu-id="f1862-114">Representa la carpeta de destino de una carpeta que se ha movido.</span><span class="sxs-lookup"><span data-stu-id="f1862-114">Represents the destination folder for a moved folder.</span></span>  <br/> |
|[<span data-ttu-id="f1862-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="f1862-115">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="f1862-116">Contiene una matriz de carpetas para desplazarse a la carpeta identificada por el elemento [ToFolderId](tofolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="f1862-116">Contains an array of folders to move to the folder identified by the [ToFolderId](tofolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f1862-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f1862-117">Parent elements</span></span>

<span data-ttu-id="f1862-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f1862-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f1862-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1862-119">Remarks</span></span>

<span data-ttu-id="f1862-120">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="f1862-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f1862-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="f1862-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1862-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1862-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f1862-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="f1862-123">Schema Name</span></span>  <br/> |<span data-ttu-id="f1862-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="f1862-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f1862-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="f1862-125">Validation File</span></span>  <br/> |<span data-ttu-id="f1862-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="f1862-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f1862-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="f1862-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="f1862-128">Falso</span><span class="sxs-lookup"><span data-stu-id="f1862-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f1862-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1862-129">See also</span></span>



[<span data-ttu-id="f1862-130">Operación MoveFolder</span><span class="sxs-lookup"><span data-stu-id="f1862-130">MoveFolder operation</span></span>](movefolder-operation.md)

