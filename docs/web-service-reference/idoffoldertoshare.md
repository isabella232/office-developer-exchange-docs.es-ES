---
title: IdOfFolderToShare
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IdOfFolderToShare
api_type:
- schema
ms.assetid: 199d1839-f061-4070-a977-874b0c08e5be
description: El elemento IdOfFolderToShare representa el identificador de la carpeta en el servidor que se van a compartir.
ms.openlocfilehash: 1e3e53819f23bbc5753ac21b9e3ea6593ac4826c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835853"
---
# <a name="idoffoldertoshare"></a><span data-ttu-id="1f2a9-103">IdOfFolderToShare</span><span class="sxs-lookup"><span data-stu-id="1f2a9-103">IdOfFolderToShare</span></span>

<span data-ttu-id="1f2a9-104">El elemento **IdOfFolderToShare** representa el identificador de la carpeta en el servidor que se van a compartir.</span><span class="sxs-lookup"><span data-stu-id="1f2a9-104">The **IdOfFolderToShare** element represents the identifier of the folder on the server that will be shared.</span></span> 
  
```
<IdOfFolderToShare Id="" ChangeKey="" />
```

 <span data-ttu-id="1f2a9-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="1f2a9-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1f2a9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1f2a9-106">Attributes and elements</span></span>

<span data-ttu-id="1f2a9-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="1f2a9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f2a9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="1f2a9-108">Attributes</span></span>

|<span data-ttu-id="1f2a9-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="1f2a9-109">**Attribute**</span></span>|<span data-ttu-id="1f2a9-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1f2a9-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f2a9-111">Id</span><span class="sxs-lookup"><span data-stu-id="1f2a9-111">Id</span></span>  <br/> |<span data-ttu-id="1f2a9-112">Contiene una cadena que identifica una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="1f2a9-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="1f2a9-113">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="1f2a9-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="1f2a9-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="1f2a9-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="1f2a9-115">Contiene una cadena que identifica una versión de una carpeta que se identifica con el atributo Id.</span><span class="sxs-lookup"><span data-stu-id="1f2a9-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="1f2a9-116">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="1f2a9-116">This attribute is optional.</span></span> <span data-ttu-id="1f2a9-117">Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="1f2a9-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1f2a9-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1f2a9-118">Child elements</span></span>

<span data-ttu-id="1f2a9-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1f2a9-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1f2a9-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="1f2a9-120">Parent elements</span></span>

|<span data-ttu-id="1f2a9-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="1f2a9-121">**Element**</span></span>|<span data-ttu-id="1f2a9-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1f2a9-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1f2a9-123">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="1f2a9-123">GetSharingMetadata</span></span>](getsharingmetadata.md) <br/> |<span data-ttu-id="1f2a9-124">Define una solicitud para obtener un token de autenticación opaco que identifica la invitación para compartir.</span><span class="sxs-lookup"><span data-stu-id="1f2a9-124">Defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f2a9-125">Notas</span><span class="sxs-lookup"><span data-stu-id="1f2a9-125">Remarks</span></span>

<span data-ttu-id="1f2a9-126">El esquema que describe este elemento se encuentra en el directorio Virtual de IIS que hospeda los servicios Web Exchange del equipo que ejecuta a Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="1f2a9-126">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1f2a9-127">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="1f2a9-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f2a9-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1f2a9-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1f2a9-129">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="1f2a9-129">Schema Name</span></span>  <br/> |<span data-ttu-id="1f2a9-130">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="1f2a9-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1f2a9-131">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="1f2a9-131">Validation File</span></span>  <br/> |<span data-ttu-id="1f2a9-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1f2a9-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1f2a9-133">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="1f2a9-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="1f2a9-134">False</span><span class="sxs-lookup"><span data-stu-id="1f2a9-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1f2a9-135">Ver también</span><span class="sxs-lookup"><span data-stu-id="1f2a9-135">See also</span></span>



[<span data-ttu-id="1f2a9-136">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="1f2a9-136">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="1f2a9-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="1f2a9-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

