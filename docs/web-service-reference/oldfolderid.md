---
title: OldFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OldFolderId
api_type:
- schema
ms.assetid: da554a97-ab87-4950-9fc4-26b1972381bb
description: El elemento OldFolderId contiene el identificador original de una carpeta que se movió o copió.
ms.openlocfilehash: a6713b9e0c47d68480724c3902086da6a8647dd7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458064"
---
# <a name="oldfolderid"></a><span data-ttu-id="b0f4a-103">OldFolderId</span><span class="sxs-lookup"><span data-stu-id="b0f4a-103">OldFolderId</span></span>

<span data-ttu-id="b0f4a-104">El elemento **OldFolderId** contiene el identificador original de una carpeta que se movió o copió.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-104">The **OldFolderId** element contains the original identifier of a folder that was moved or copied.</span></span> 
  
```xml
<OldFolderId Id="" ChangeKey=""/>
```

 <span data-ttu-id="b0f4a-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="b0f4a-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b0f4a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b0f4a-106">Attributes and elements</span></span>

<span data-ttu-id="b0f4a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b0f4a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b0f4a-108">Attributes</span></span>

|<span data-ttu-id="b0f4a-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="b0f4a-109">**Attribute**</span></span>|<span data-ttu-id="b0f4a-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b0f4a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b0f4a-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="b0f4a-111">**Id**</span></span> <br/> |<span data-ttu-id="b0f4a-112">Contiene una cadena que identifica una carpeta en el almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="b0f4a-113">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="b0f4a-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="b0f4a-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="b0f4a-115">Contiene una cadena que identifica una versión de una carpeta identificada por el atributo id.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="b0f4a-116">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-116">This attribute is optional.</span></span> <span data-ttu-id="b0f4a-117">Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b0f4a-118">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b0f4a-118">Child elements</span></span>

<span data-ttu-id="b0f4a-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b0f4a-120">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b0f4a-120">Parent elements</span></span>

|<span data-ttu-id="b0f4a-121">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b0f4a-121">**Element**</span></span>|<span data-ttu-id="b0f4a-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b0f4a-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0f4a-123">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="b0f4a-123">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="b0f4a-124">Representa un evento en el que se copia un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-124">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="b0f4a-125">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="b0f4a-125">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="b0f4a-126">Representa un evento en el que se mueve un elemento o una carpeta de una carpeta principal a otra carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-126">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0f4a-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0f4a-127">Remarks</span></span>

<span data-ttu-id="b0f4a-128">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b0f4a-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b0f4a-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0f4a-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0f4a-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b0f4a-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b0f4a-131">Schema Name</span></span>  <br/> |<span data-ttu-id="b0f4a-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b0f4a-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="b0f4a-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b0f4a-133">Validation File</span></span>  <br/> |<span data-ttu-id="b0f4a-134">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="b0f4a-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b0f4a-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b0f4a-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="b0f4a-136">Falso</span><span class="sxs-lookup"><span data-stu-id="b0f4a-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b0f4a-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0f4a-137">See also</span></span>



[<span data-ttu-id="b0f4a-138">Operación subscribe</span><span class="sxs-lookup"><span data-stu-id="b0f4a-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="b0f4a-139">Operación GetEvents</span><span class="sxs-lookup"><span data-stu-id="b0f4a-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="b0f4a-140">Operación unsubscribe</span><span class="sxs-lookup"><span data-stu-id="b0f4a-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="b0f4a-141">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="b0f4a-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

