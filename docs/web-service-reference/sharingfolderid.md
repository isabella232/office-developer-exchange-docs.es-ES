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
description: El elemento SharingFolderId representa el identificador de la carpeta local en una relación de uso compartido.
ms.openlocfilehash: 02780251639ee651ca65d8eadded43260852aaf8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526581"
---
# <a name="sharingfolderid"></a><span data-ttu-id="a3b7d-103">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="a3b7d-103">SharingFolderId</span></span>

<span data-ttu-id="a3b7d-104">El elemento **SharingFolderId** representa el identificador de la carpeta local en una relación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="a3b7d-104">The **SharingFolderId** element represents the identifier of the local folder in a sharing relationship.</span></span> 
  
```xml
<SharingFolderId Id="" ChangeKey="" />
```

 <span data-ttu-id="a3b7d-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="a3b7d-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a3b7d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a3b7d-106">Attributes and elements</span></span>

<span data-ttu-id="a3b7d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a3b7d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a3b7d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a3b7d-108">Attributes</span></span>

|<span data-ttu-id="a3b7d-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a3b7d-109">**Attribute**</span></span>|<span data-ttu-id="a3b7d-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a3b7d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a3b7d-111">Id</span><span class="sxs-lookup"><span data-stu-id="a3b7d-111">Id</span></span>  <br/> |<span data-ttu-id="a3b7d-112">Contiene una cadena que identifica una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a3b7d-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="a3b7d-113">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a3b7d-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="a3b7d-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="a3b7d-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="a3b7d-115">Contiene una cadena que identifica una versión de una carpeta identificada por el atributo id.</span><span class="sxs-lookup"><span data-stu-id="a3b7d-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="a3b7d-116">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="a3b7d-116">This attribute is optional.</span></span> <span data-ttu-id="a3b7d-117">Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="a3b7d-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a3b7d-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a3b7d-118">Child elements</span></span>

<span data-ttu-id="a3b7d-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="a3b7d-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a3b7d-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a3b7d-120">Parent elements</span></span>

|<span data-ttu-id="a3b7d-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a3b7d-121">**Element**</span></span>|<span data-ttu-id="a3b7d-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a3b7d-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3b7d-123">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="a3b7d-123">RefreshSharingFolder</span></span>](refreshsharingfolder.md) <br/> |<span data-ttu-id="a3b7d-124">Define una solicitud para actualizar la carpeta local especificada.</span><span class="sxs-lookup"><span data-stu-id="a3b7d-124">Defines a request to refresh the specified local folder.</span></span>  <br/> |
|[<span data-ttu-id="a3b7d-125">GetSharingFolderResponse</span><span class="sxs-lookup"><span data-stu-id="a3b7d-125">GetSharingFolderResponse</span></span>](getsharingfolderresponse.md) <br/> |<span data-ttu-id="a3b7d-126">Define una respuesta a una solicitud de [operación de GetSharingFolder](getsharingfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="a3b7d-126">Defines a response to a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="a3b7d-127">GetSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a3b7d-127">GetSharingFolderResponseMessage</span></span>](getsharingfolderresponsemessage.md) <br/> |<span data-ttu-id="a3b7d-128">Contiene el estado y el resultado de una sola solicitud de [operación GetSharingFolder](getsharingfolder-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="a3b7d-128">Contains the status and result of a single [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3b7d-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a3b7d-129">Remarks</span></span>

<span data-ttu-id="a3b7d-130">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="a3b7d-130">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a3b7d-131">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a3b7d-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a3b7d-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="a3b7d-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a3b7d-133">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a3b7d-133">Schema Name</span></span>  <br/> |<span data-ttu-id="a3b7d-134">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="a3b7d-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a3b7d-135">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a3b7d-135">Validation File</span></span>  <br/> |<span data-ttu-id="a3b7d-136">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a3b7d-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a3b7d-137">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a3b7d-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="a3b7d-138">Falso</span><span class="sxs-lookup"><span data-stu-id="a3b7d-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a3b7d-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3b7d-139">See also</span></span>



- [<span data-ttu-id="a3b7d-140">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a3b7d-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

