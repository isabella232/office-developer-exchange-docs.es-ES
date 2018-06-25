---
title: SourceIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SourceIds
api_type:
- schema
ms.assetid: 0043abd5-ba9c-4d67-8832-325f32bf7651
description: El elemento SourceIds contiene los identificadores de origen para convertir.
ms.openlocfilehash: c9ee9fd01367f714e1cb3770e2be5161cb45d98f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837522"
---
# <a name="sourceids"></a><span data-ttu-id="434c6-103">SourceIds</span><span class="sxs-lookup"><span data-stu-id="434c6-103">SourceIds</span></span>

<span data-ttu-id="434c6-104">El elemento **SourceIds** contiene los identificadores de origen para convertir.</span><span class="sxs-lookup"><span data-stu-id="434c6-104">The **SourceIds** element contains the source identifiers to convert.</span></span> 
  
[<span data-ttu-id="434c6-105">ConvertId</span><span class="sxs-lookup"><span data-stu-id="434c6-105">ConvertId</span></span>](convertid.md)
  
[<span data-ttu-id="434c6-106">SourceIds</span><span class="sxs-lookup"><span data-stu-id="434c6-106">SourceIds</span></span>](sourceids.md)
  
```xml
<SourceIds>
   <AlternateId/>
   <AlternatePublicFolderId/>
   <AlternatePublicFolderItemId/>
</SourceIds>
```

 <span data-ttu-id="434c6-107">**NonEmptyArrayOfAlternateIdsType**</span><span class="sxs-lookup"><span data-stu-id="434c6-107">**NonEmptyArrayOfAlternateIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="434c6-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="434c6-108">Attributes and elements</span></span>

<span data-ttu-id="434c6-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="434c6-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="434c6-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="434c6-110">Attributes</span></span>

<span data-ttu-id="434c6-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="434c6-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="434c6-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="434c6-112">Child elements</span></span>

|<span data-ttu-id="434c6-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="434c6-113">**Element**</span></span>|<span data-ttu-id="434c6-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="434c6-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="434c6-115">AlternateId</span><span class="sxs-lookup"><span data-stu-id="434c6-115">AlternateId</span></span>](alternateid.md) <br/> |<span data-ttu-id="434c6-116">Describe un identificador de elemento o carpeta para convertir.</span><span class="sxs-lookup"><span data-stu-id="434c6-116">Describes an item or folder identifier to convert.</span></span>  <br/> |
|[<span data-ttu-id="434c6-117">AlternatePublicFolderId</span><span class="sxs-lookup"><span data-stu-id="434c6-117">AlternatePublicFolderId</span></span>](alternatepublicfolderid.md) <br/> |<span data-ttu-id="434c6-118">Describe un identificador de carpeta pública para convertir.</span><span class="sxs-lookup"><span data-stu-id="434c6-118">Describes a public folder identifier to convert.</span></span>  <br/> |
|[<span data-ttu-id="434c6-119">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="434c6-119">AlternatePublicFolderItemId</span></span>](alternatepublicfolderitemid.md) <br/> |<span data-ttu-id="434c6-120">Se describe un identificador de elemento de la carpeta pública para convertir.</span><span class="sxs-lookup"><span data-stu-id="434c6-120">Describes a public folder item identifier to convert.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="434c6-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="434c6-121">Parent elements</span></span>

|<span data-ttu-id="434c6-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="434c6-122">**Element**</span></span>|<span data-ttu-id="434c6-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="434c6-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="434c6-124">ConvertId</span><span class="sxs-lookup"><span data-stu-id="434c6-124">ConvertId</span></span>](convertid.md) <br/> |<span data-ttu-id="434c6-125">Define una solicitud para convertir los identificadores de elemento y carpeta entre formatos compatibles de Exchange.</span><span class="sxs-lookup"><span data-stu-id="434c6-125">Defines a request to convert item and folder identifiers between Exchange supported formats.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="434c6-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="434c6-126">Remarks</span></span>

<span data-ttu-id="434c6-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server que tiene instalada la función del servidor acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="434c6-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="434c6-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="434c6-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="434c6-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="434c6-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="434c6-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="434c6-130">Schema Name</span></span>  <br/> |<span data-ttu-id="434c6-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="434c6-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="434c6-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="434c6-132">Validation File</span></span>  <br/> |<span data-ttu-id="434c6-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="434c6-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="434c6-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="434c6-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="434c6-135">False</span><span class="sxs-lookup"><span data-stu-id="434c6-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="434c6-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="434c6-136">See also</span></span>



[<span data-ttu-id="434c6-137">Operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="434c6-137">ConvertId operation</span></span>](convertid-operation.md)


- [<span data-ttu-id="434c6-138">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="434c6-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="434c6-139">Convertir identificadores</span><span class="sxs-lookup"><span data-stu-id="434c6-139">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

