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
ms.openlocfilehash: 42a990ced18cc13c7694042df786d33c018f346c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836485"
---
# <a name="movefolder"></a><span data-ttu-id="1ef4b-103">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="1ef4b-103">MoveFolder</span></span>

<span data-ttu-id="1ef4b-104">El elemento **MoveFolder** define una solicitud para mover una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1ef4b-104">The **MoveFolder** element defines a request to move a folder in the Exchange store.</span></span> 
  
```xml
<MoveFolder>
   <ToFolderId/>
   <FolderIds/>
</MoveFolder>
```

 <span data-ttu-id="1ef4b-105">**MoveFolderType**</span><span class="sxs-lookup"><span data-stu-id="1ef4b-105">**MoveFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1ef4b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1ef4b-106">Attributes and elements</span></span>

<span data-ttu-id="1ef4b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1ef4b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ef4b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1ef4b-108">Attributes</span></span>

<span data-ttu-id="1ef4b-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1ef4b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1ef4b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1ef4b-110">Child elements</span></span>

|<span data-ttu-id="1ef4b-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ef4b-111">**Element**</span></span>|<span data-ttu-id="1ef4b-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1ef4b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ef4b-113">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="1ef4b-113">ToFolderId</span></span>](tofolderid.md) <br/> |<span data-ttu-id="1ef4b-114">Representa la carpeta de destino para una carpeta que se ha movido.</span><span class="sxs-lookup"><span data-stu-id="1ef4b-114">Represents the destination folder for a moved folder.</span></span>  <br/> |
|[<span data-ttu-id="1ef4b-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="1ef4b-115">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="1ef4b-116">Contiene una matriz de las carpetas para mover a la carpeta identificada por el elemento [ToFolderId](tofolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="1ef4b-116">Contains an array of folders to move to the folder identified by the [ToFolderId](tofolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1ef4b-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1ef4b-117">Parent elements</span></span>

<span data-ttu-id="1ef4b-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1ef4b-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1ef4b-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ef4b-119">Remarks</span></span>

<span data-ttu-id="1ef4b-120">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="1ef4b-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1ef4b-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1ef4b-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ef4b-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1ef4b-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1ef4b-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1ef4b-123">Schema Name</span></span>  <br/> |<span data-ttu-id="1ef4b-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1ef4b-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1ef4b-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1ef4b-125">Validation File</span></span>  <br/> |<span data-ttu-id="1ef4b-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1ef4b-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1ef4b-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1ef4b-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="1ef4b-128">False</span><span class="sxs-lookup"><span data-stu-id="1ef4b-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ef4b-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="1ef4b-129">See also</span></span>



[<span data-ttu-id="1ef4b-130">Operación MoveFolder</span><span class="sxs-lookup"><span data-stu-id="1ef4b-130">MoveFolder operation</span></span>](movefolder-operation.md)

