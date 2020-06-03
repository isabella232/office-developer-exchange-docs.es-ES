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
description: El elemento RefreshSharingFolder define una solicitud para actualizar la carpeta local especificada. Es el elemento base para la operación RefreshSharingFolder.
ms.openlocfilehash: 4454607fa2c3114cc7279fd7c30f8aee74707baa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467931"
---
# <a name="refreshsharingfolder"></a><span data-ttu-id="65450-104">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="65450-104">RefreshSharingFolder</span></span>

<span data-ttu-id="65450-105">El elemento **RefreshSharingFolder** define una solicitud para actualizar la carpeta local especificada.</span><span class="sxs-lookup"><span data-stu-id="65450-105">The **RefreshSharingFolder** element defines a request to refresh the specified local folder.</span></span> <span data-ttu-id="65450-106">Es el elemento base para la [operación RefreshSharingFolder](refreshsharingfolder-operation.md).</span><span class="sxs-lookup"><span data-stu-id="65450-106">It is the base element for the [RefreshSharingFolder operation](refreshsharingfolder-operation.md).</span></span>
  
```xml
<RefreshSharingFolder>   <SharingFolderId/></RefreshSharingFolder>
```

 <span data-ttu-id="65450-107">**RefreshSharingFolderType**</span><span class="sxs-lookup"><span data-stu-id="65450-107">**RefreshSharingFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="65450-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="65450-108">Attributes and elements</span></span>

<span data-ttu-id="65450-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="65450-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65450-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="65450-110">Attributes</span></span>

<span data-ttu-id="65450-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="65450-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="65450-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="65450-112">Child elements</span></span>

|<span data-ttu-id="65450-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="65450-113">**Element**</span></span>|<span data-ttu-id="65450-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="65450-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65450-115">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="65450-115">SharingFolderId</span></span>](sharingfolderid.md) <br/> |<span data-ttu-id="65450-116">Representa el identificador de la carpeta local en una relación de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="65450-116">Represents the identifier of the local folder in a sharing relationship.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="65450-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="65450-117">Parent elements</span></span>

<span data-ttu-id="65450-118">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="65450-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="65450-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="65450-119">Remarks</span></span>

<span data-ttu-id="65450-120">El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="65450-120">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65450-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="65450-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65450-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="65450-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="65450-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="65450-123">Schema Name</span></span>  <br/> |<span data-ttu-id="65450-124">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="65450-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="65450-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="65450-125">Validation File</span></span>  <br/> |<span data-ttu-id="65450-126">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="65450-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="65450-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="65450-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="65450-128">Falso</span><span class="sxs-lookup"><span data-stu-id="65450-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65450-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="65450-129">See also</span></span>



- [<span data-ttu-id="65450-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="65450-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

