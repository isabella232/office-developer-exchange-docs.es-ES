---
title: RefreshSharingFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RefreshSharingFolder
api_type:
- schema
ms.assetid: 14571c28-effa-430a-802e-82fb99bafa7f
description: El elemento RefreshSharingFolder define una solicitud para actualizar la carpeta local especificada. Éste es el elemento base para la operación RefreshSharingFolder.
ms.openlocfilehash: b09e311d0ba38b0cdcc9fe0864ed3e2b0151b0fd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837043"
---
# <a name="refreshsharingfolder"></a><span data-ttu-id="46a78-104">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="46a78-104">RefreshSharingFolder</span></span>

<span data-ttu-id="46a78-105">El elemento **RefreshSharingFolder** define una solicitud para actualizar la carpeta local especificada.</span><span class="sxs-lookup"><span data-stu-id="46a78-105">The **RefreshSharingFolder** element defines a request to refresh the specified local folder.</span></span> <span data-ttu-id="46a78-106">Éste es el elemento base para la [operación de RefreshSharingFolder](refreshsharingfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="46a78-106">It is the base element for the [RefreshSharingFolder operation](refreshsharingfolder-operation.md).</span></span>
  
```xml
<RefreshSharingFolder>   <SharingFolderId/></RefreshSharingFolder>
```

 <span data-ttu-id="46a78-107">**RefreshSharingFolderType**</span><span class="sxs-lookup"><span data-stu-id="46a78-107">**RefreshSharingFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="46a78-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="46a78-108">Attributes and elements</span></span>

<span data-ttu-id="46a78-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="46a78-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="46a78-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="46a78-110">Attributes</span></span>

<span data-ttu-id="46a78-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="46a78-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="46a78-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="46a78-112">Child elements</span></span>

|<span data-ttu-id="46a78-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="46a78-113">**Element**</span></span>|<span data-ttu-id="46a78-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="46a78-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46a78-115">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="46a78-115">SharingFolderId</span></span>](sharingfolderid.md) <br/> |<span data-ttu-id="46a78-116">Representa el identificador de la carpeta local en una relación de uso compartida.</span><span class="sxs-lookup"><span data-stu-id="46a78-116">Represents the identifier of the local folder in a sharing relationship.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="46a78-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="46a78-117">Parent elements</span></span>

<span data-ttu-id="46a78-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="46a78-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="46a78-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46a78-119">Remarks</span></span>

<span data-ttu-id="46a78-120">El esquema que describe este elemento se encuentra en el directorio Virtual de IIS que hospeda los servicios Web Exchange del equipo que ejecuta a Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="46a78-120">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="46a78-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="46a78-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46a78-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="46a78-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="46a78-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="46a78-123">Schema Name</span></span>  <br/> |<span data-ttu-id="46a78-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="46a78-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="46a78-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="46a78-125">Validation File</span></span>  <br/> |<span data-ttu-id="46a78-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="46a78-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="46a78-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="46a78-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="46a78-128">False</span><span class="sxs-lookup"><span data-stu-id="46a78-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="46a78-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="46a78-129">See also</span></span>



- [<span data-ttu-id="46a78-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="46a78-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

