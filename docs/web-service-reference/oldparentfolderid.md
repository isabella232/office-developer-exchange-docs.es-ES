---
title: OldParentFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OldParentFolderId
api_type:
- schema
ms.assetid: da1b8c88-c650-455d-b749-0cd160b012d8
description: El elemento OldParentFolderId contiene el identificador de la carpeta principal de un elemento o carpeta que se ha copiado o movido.
ms.openlocfilehash: 1c4a51755c4194939dd797efa31cf5410b02bf85
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836644"
---
# <a name="oldparentfolderid"></a><span data-ttu-id="234fb-103">OldParentFolderId</span><span class="sxs-lookup"><span data-stu-id="234fb-103">OldParentFolderId</span></span>

<span data-ttu-id="234fb-104">El elemento **OldParentFolderId** contiene el identificador de la carpeta principal de un elemento o carpeta que se ha copiado o movido.</span><span class="sxs-lookup"><span data-stu-id="234fb-104">The **OldParentFolderId** element contains the identifier of the parent folder of an item or folder that was copied or moved.</span></span> 
  
```xml
<OldParentFolderId Id="" ChangeKey=""/>
```

 <span data-ttu-id="234fb-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="234fb-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="234fb-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="234fb-106">Attributes and elements</span></span>

<span data-ttu-id="234fb-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="234fb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="234fb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="234fb-108">Attributes</span></span>

|<span data-ttu-id="234fb-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="234fb-109">**Attribute**</span></span>|<span data-ttu-id="234fb-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="234fb-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="234fb-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="234fb-111">**Id**</span></span> <br/> |<span data-ttu-id="234fb-112">Contiene una cadena que identifica una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="234fb-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="234fb-113">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="234fb-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="234fb-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="234fb-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="234fb-115">Contiene una cadena que identifica una versión de una carpeta que se identifica con el atributo Id.</span><span class="sxs-lookup"><span data-stu-id="234fb-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="234fb-116">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="234fb-116">This attribute is optional.</span></span> <span data-ttu-id="234fb-117">Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="234fb-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="234fb-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="234fb-118">Child elements</span></span>

<span data-ttu-id="234fb-119">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="234fb-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="234fb-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="234fb-120">Parent elements</span></span>

|<span data-ttu-id="234fb-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="234fb-121">**Element**</span></span>|<span data-ttu-id="234fb-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="234fb-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="234fb-123">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="234fb-123">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="234fb-124">Representa un evento en el que se copia un elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="234fb-124">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="234fb-125">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="234fb-125">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="234fb-126">Representa un evento en el que una carpeta o elemento se mueve de una carpeta principal a otra carpeta primaria.</span><span class="sxs-lookup"><span data-stu-id="234fb-126">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="234fb-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="234fb-127">Remarks</span></span>

<span data-ttu-id="234fb-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="234fb-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="234fb-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="234fb-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="234fb-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="234fb-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="234fb-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="234fb-131">Schema Name</span></span>  <br/> |<span data-ttu-id="234fb-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="234fb-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="234fb-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="234fb-133">Validation File</span></span>  <br/> |<span data-ttu-id="234fb-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="234fb-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="234fb-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="234fb-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="234fb-136">False</span><span class="sxs-lookup"><span data-stu-id="234fb-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="234fb-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="234fb-137">See also</span></span>



[<span data-ttu-id="234fb-138">Operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="234fb-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="234fb-139">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="234fb-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="234fb-140">Cancelar la operación de suscripción</span><span class="sxs-lookup"><span data-stu-id="234fb-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="234fb-141">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="234fb-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

