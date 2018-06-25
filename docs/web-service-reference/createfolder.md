---
title: CreateFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateFolder
api_type:
- schema
ms.assetid: 110bada1-517b-4bd6-870d-7086dc879e5d
description: El elemento CreateFolder define una solicitud para crear una carpeta en el almacén de Exchange.
ms.openlocfilehash: e30af23b8ed8669053b94be460d62fbf7abf24c9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763927"
---
# <a name="createfolder"></a><span data-ttu-id="57e82-103">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="57e82-103">CreateFolder</span></span>

<span data-ttu-id="57e82-104">El elemento **CreateFolder** define una solicitud para crear una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="57e82-104">The **CreateFolder** element defines a request to create a folder in the Exchange store.</span></span> 
  
```xml
<CreateFolder>
   <ParentFolderId/>
   <Folders/>
</CreateFolder>
```

 <span data-ttu-id="57e82-105">**CreateFolderType**</span><span class="sxs-lookup"><span data-stu-id="57e82-105">**CreateFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="57e82-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="57e82-106">Attributes and elements</span></span>

<span data-ttu-id="57e82-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="57e82-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="57e82-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="57e82-108">Attributes</span></span>

<span data-ttu-id="57e82-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="57e82-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="57e82-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="57e82-110">Child elements</span></span>

|<span data-ttu-id="57e82-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="57e82-111">**Element**</span></span>|<span data-ttu-id="57e82-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="57e82-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="57e82-113">ID (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="57e82-113">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="57e82-114">El elemento que identifica la ubicación donde se crea la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="57e82-114">The element that identifies the location where the new folder is created.</span></span>  <br/> |
|[<span data-ttu-id="57e82-115">Carpetas</span><span class="sxs-lookup"><span data-stu-id="57e82-115">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="57e82-116">El elemento que contiene todas las carpetas para crear.</span><span class="sxs-lookup"><span data-stu-id="57e82-116">The element that contains all the folders to create.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="57e82-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="57e82-117">Parent elements</span></span>

<span data-ttu-id="57e82-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="57e82-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="57e82-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="57e82-119">Remarks</span></span>

<span data-ttu-id="57e82-120">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="57e82-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="57e82-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="57e82-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="57e82-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="57e82-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="57e82-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="57e82-123">Schema Name</span></span>  <br/> |<span data-ttu-id="57e82-124">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="57e82-124">Message schema</span></span>  <br/> |
|<span data-ttu-id="57e82-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="57e82-125">Validation File</span></span>  <br/> |<span data-ttu-id="57e82-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="57e82-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="57e82-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="57e82-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="57e82-128">False</span><span class="sxs-lookup"><span data-stu-id="57e82-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="57e82-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="57e82-129">See also</span></span>



[<span data-ttu-id="57e82-130">Operación CreateFolder</span><span class="sxs-lookup"><span data-stu-id="57e82-130">CreateFolder operation</span></span>](createfolder-operation.md)


[<span data-ttu-id="57e82-131">Creación de carpetas (servicios Web de Exchange)</span><span class="sxs-lookup"><span data-stu-id="57e82-131">Creating Folders (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

