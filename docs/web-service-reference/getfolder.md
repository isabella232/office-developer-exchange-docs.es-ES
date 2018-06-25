---
title: GetFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetFolder
api_type:
- schema
ms.assetid: 34e4c9ea-adcd-46bd-ae8f-7abb256c585a
description: El elemento GetFolder define una solicitud para obtener una carpeta de un buzón en el almacén de Exchange.
ms.openlocfilehash: 233da6ce57683350d4a13f6585593ac09438f0e6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764855"
---
# <a name="getfolder"></a><span data-ttu-id="55270-103">GetFolder</span><span class="sxs-lookup"><span data-stu-id="55270-103">GetFolder</span></span>

<span data-ttu-id="55270-104">El elemento **GetFolder** define una solicitud para obtener una carpeta de un buzón en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="55270-104">The **GetFolder** element defines a request to get a folder from a mailbox in the Exchange store.</span></span> 
  
```xml
<GetFolder>
   <FolderShape/>
   <FolderIds/>
</GetFolder>
```

 <span data-ttu-id="55270-105">**GetFolderType**</span><span class="sxs-lookup"><span data-stu-id="55270-105">**GetFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="55270-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="55270-106">Attributes and elements</span></span>

<span data-ttu-id="55270-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="55270-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="55270-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="55270-108">Attributes</span></span>

<span data-ttu-id="55270-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="55270-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="55270-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="55270-110">Child elements</span></span>

|<span data-ttu-id="55270-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="55270-111">**Element**</span></span>|<span data-ttu-id="55270-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="55270-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55270-113">FolderShape</span><span class="sxs-lookup"><span data-stu-id="55270-113">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="55270-114">Identifica las propiedades para obtener para cada carpeta identificada en el elemento [FolderIds](folderids.md) .</span><span class="sxs-lookup"><span data-stu-id="55270-114">Identifies the properties to get for each folder identified in the [FolderIds](folderids.md) element.</span></span>  <br/> |
|[<span data-ttu-id="55270-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="55270-115">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="55270-116">Contiene una matriz de identificadores de carpeta que se usa para identificar las carpetas para obtener de un buzón en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="55270-116">Contains an array of folder identifiers that are used to identify folders to get from a mailbox in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="55270-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="55270-117">Parent elements</span></span>

<span data-ttu-id="55270-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="55270-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="55270-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="55270-119">Remarks</span></span>

<span data-ttu-id="55270-120">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="55270-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="55270-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="55270-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55270-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="55270-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="55270-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="55270-123">Schema Name</span></span>  <br/> |<span data-ttu-id="55270-124">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="55270-124">Message schema</span></span>  <br/> |
|<span data-ttu-id="55270-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="55270-125">Validation File</span></span>  <br/> |<span data-ttu-id="55270-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="55270-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="55270-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="55270-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="55270-128">False</span><span class="sxs-lookup"><span data-stu-id="55270-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55270-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="55270-129">See also</span></span>



[<span data-ttu-id="55270-130">Operación GetFolder</span><span class="sxs-lookup"><span data-stu-id="55270-130">GetFolder operation</span></span>](getfolder-operation.md)

