---
title: SharingFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharingFolderId
api_type:
- schema
ms.assetid: 5ad37ceb-2922-4420-9051-c29d0d57c420
description: El elemento SharingFolderId representa el identificador de la carpeta local en una relación de uso compartida.
ms.openlocfilehash: e0eb1fbd7155040508daf253f5eb4b1352d7426d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837485"
---
# <a name="sharingfolderid"></a><span data-ttu-id="ae9ca-103">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="ae9ca-103">SharingFolderId</span></span>

<span data-ttu-id="ae9ca-104">El elemento **SharingFolderId** representa el identificador de la carpeta local en una relación de uso compartida.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-104">The **SharingFolderId** element represents the identifier of the local folder in a sharing relationship.</span></span> 
  
```xml
<SharingFolderId Id="" ChangeKey="" />
```

 <span data-ttu-id="ae9ca-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="ae9ca-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ae9ca-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ae9ca-106">Attributes and elements</span></span>

<span data-ttu-id="ae9ca-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae9ca-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ae9ca-108">Attributes</span></span>

|<span data-ttu-id="ae9ca-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ae9ca-109">**Attribute**</span></span>|<span data-ttu-id="ae9ca-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae9ca-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae9ca-111">Id</span><span class="sxs-lookup"><span data-stu-id="ae9ca-111">Id</span></span>  <br/> |<span data-ttu-id="ae9ca-112">Contiene una cadena que identifica una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="ae9ca-113">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="ae9ca-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="ae9ca-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="ae9ca-115">Contiene una cadena que identifica una versión de una carpeta que se identifica con el atributo Id.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="ae9ca-116">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-116">This attribute is optional.</span></span> <span data-ttu-id="ae9ca-117">Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ae9ca-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ae9ca-118">Child elements</span></span>

<span data-ttu-id="ae9ca-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ae9ca-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ae9ca-120">Parent elements</span></span>

|<span data-ttu-id="ae9ca-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="ae9ca-121">**Element**</span></span>|<span data-ttu-id="ae9ca-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae9ca-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae9ca-123">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="ae9ca-123">RefreshSharingFolder</span></span>](refreshsharingfolder.md) <br/> |<span data-ttu-id="ae9ca-124">Define una solicitud para actualizar la carpeta local especificada.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-124">Defines a request to refresh the specified local folder.</span></span>  <br/> |
|[<span data-ttu-id="ae9ca-125">GetSharingFolderResponse</span><span class="sxs-lookup"><span data-stu-id="ae9ca-125">GetSharingFolderResponse</span></span>](getsharingfolderresponse.md) <br/> |<span data-ttu-id="ae9ca-126">Define una respuesta a una solicitud de [operación GetSharingFolder](getsharingfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ae9ca-126">Defines a response to a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="ae9ca-127">GetSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ae9ca-127">GetSharingFolderResponseMessage</span></span>](getsharingfolderresponsemessage.md) <br/> |<span data-ttu-id="ae9ca-128">Contiene el estado y el resultado de una única solicitud de [operación GetSharingFolder](getsharingfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ae9ca-128">Contains the status and result of a single [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae9ca-129">Notas</span><span class="sxs-lookup"><span data-stu-id="ae9ca-129">Remarks</span></span>

<span data-ttu-id="ae9ca-130">El esquema que describe este elemento se encuentra en el directorio Virtual de IIS que hospeda los servicios Web Exchange del equipo que ejecuta a Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="ae9ca-130">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae9ca-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ae9ca-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae9ca-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ae9ca-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ae9ca-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ae9ca-133">Schema Name</span></span>  <br/> |<span data-ttu-id="ae9ca-134">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ae9ca-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ae9ca-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ae9ca-135">Validation File</span></span>  <br/> |<span data-ttu-id="ae9ca-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ae9ca-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ae9ca-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ae9ca-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="ae9ca-138">False</span><span class="sxs-lookup"><span data-stu-id="ae9ca-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae9ca-139">Ver también</span><span class="sxs-lookup"><span data-stu-id="ae9ca-139">See also</span></span>



- [<span data-ttu-id="ae9ca-140">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ae9ca-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

