---
title: CopyFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyFolder
api_type:
- schema
ms.assetid: 7d5cd08a-fe81-4cb6-a5a0-6dec2d3c93d4
description: El elemento CopyFolder define una solicitud para copiar las carpetas de un buzón en el almacén de Exchange.
ms.openlocfilehash: 7bcfcc7f4212b3a3bd339fa5863df2990eb20d6d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763896"
---
# <a name="copyfolder"></a><span data-ttu-id="ba0d2-103">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="ba0d2-103">CopyFolder</span></span>

<span data-ttu-id="ba0d2-104">El elemento **CopyFolder** define una solicitud para copiar las carpetas de un buzón en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ba0d2-104">The **CopyFolder** element defines a request to copy folders in a mailbox in the Exchange store.</span></span> 
  
```xml
<CopyFolder>
   <ToFolderId/>
   <FolderIds/>
</CopyFolder>
```

 <span data-ttu-id="ba0d2-105">**CopyFolderType**</span><span class="sxs-lookup"><span data-stu-id="ba0d2-105">**CopyFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba0d2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ba0d2-106">Attributes and elements</span></span>

<span data-ttu-id="ba0d2-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ba0d2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba0d2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ba0d2-108">Attributes</span></span>

<span data-ttu-id="ba0d2-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ba0d2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba0d2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ba0d2-110">Child elements</span></span>

|<span data-ttu-id="ba0d2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ba0d2-111">**Element**</span></span>|<span data-ttu-id="ba0d2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ba0d2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba0d2-113">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="ba0d2-113">ToFolderId</span></span>](tofolderid.md) <br/> |<span data-ttu-id="ba0d2-114">Representa la carpeta de destino para una carpeta copiada.</span><span class="sxs-lookup"><span data-stu-id="ba0d2-114">Represents the destination folder for a copied folder.</span></span>  <br/> |
|[<span data-ttu-id="ba0d2-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="ba0d2-115">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="ba0d2-116">Contiene una matriz de carpetas que se copian a la carpeta identificada por el elemento [ToFolderId](tofolderid.md) .</span><span class="sxs-lookup"><span data-stu-id="ba0d2-116">Contains an array of folders to copy to the folder identified by the [ToFolderId](tofolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ba0d2-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ba0d2-117">Parent elements</span></span>

<span data-ttu-id="ba0d2-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ba0d2-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ba0d2-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba0d2-119">Remarks</span></span>

<span data-ttu-id="ba0d2-120">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="ba0d2-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba0d2-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ba0d2-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba0d2-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ba0d2-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ba0d2-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ba0d2-123">Schema Name</span></span>  <br/> |<span data-ttu-id="ba0d2-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ba0d2-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ba0d2-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ba0d2-125">Validation File</span></span>  <br/> |<span data-ttu-id="ba0d2-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ba0d2-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ba0d2-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ba0d2-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="ba0d2-128">False</span><span class="sxs-lookup"><span data-stu-id="ba0d2-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba0d2-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="ba0d2-129">See also</span></span>



[<span data-ttu-id="ba0d2-130">Operación CopyFolder</span><span class="sxs-lookup"><span data-stu-id="ba0d2-130">CopyFolder operation</span></span>](copyfolder-operation.md)

