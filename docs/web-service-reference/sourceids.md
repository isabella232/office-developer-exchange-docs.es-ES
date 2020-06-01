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
description: El elemento SourceIds contiene los identificadores de origen que se van a convertir.
ms.openlocfilehash: 1c4990f2185788c5cfaab5483cb6a54a0d850596
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466111"
---
# <a name="sourceids"></a><span data-ttu-id="641c8-103">SourceIds</span><span class="sxs-lookup"><span data-stu-id="641c8-103">SourceIds</span></span>

<span data-ttu-id="641c8-104">El elemento **SourceIds** contiene los identificadores de origen que se van a convertir.</span><span class="sxs-lookup"><span data-stu-id="641c8-104">The **SourceIds** element contains the source identifiers to convert.</span></span> 
  
[<span data-ttu-id="641c8-105">ConvertId</span><span class="sxs-lookup"><span data-stu-id="641c8-105">ConvertId</span></span>](convertid.md)
  
[<span data-ttu-id="641c8-106">SourceIds</span><span class="sxs-lookup"><span data-stu-id="641c8-106">SourceIds</span></span>](sourceids.md)
  
```xml
<SourceIds>
   <AlternateId/>
   <AlternatePublicFolderId/>
   <AlternatePublicFolderItemId/>
</SourceIds>
```

 <span data-ttu-id="641c8-107">**NonEmptyArrayOfAlternateIdsType**</span><span class="sxs-lookup"><span data-stu-id="641c8-107">**NonEmptyArrayOfAlternateIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="641c8-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="641c8-108">Attributes and elements</span></span>

<span data-ttu-id="641c8-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="641c8-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="641c8-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="641c8-110">Attributes</span></span>

<span data-ttu-id="641c8-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="641c8-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="641c8-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="641c8-112">Child elements</span></span>

|<span data-ttu-id="641c8-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="641c8-113">**Element**</span></span>|<span data-ttu-id="641c8-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="641c8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="641c8-115">AlternateId</span><span class="sxs-lookup"><span data-stu-id="641c8-115">AlternateId</span></span>](alternateid.md) <br/> |<span data-ttu-id="641c8-116">Describe un identificador de elemento o carpeta que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="641c8-116">Describes an item or folder identifier to convert.</span></span>  <br/> |
|[<span data-ttu-id="641c8-117">AlternatePublicFolderId</span><span class="sxs-lookup"><span data-stu-id="641c8-117">AlternatePublicFolderId</span></span>](alternatepublicfolderid.md) <br/> |<span data-ttu-id="641c8-118">Describe un identificador de carpeta pública que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="641c8-118">Describes a public folder identifier to convert.</span></span>  <br/> |
|[<span data-ttu-id="641c8-119">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="641c8-119">AlternatePublicFolderItemId</span></span>](alternatepublicfolderitemid.md) <br/> |<span data-ttu-id="641c8-120">Describe un identificador de elemento de carpeta pública que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="641c8-120">Describes a public folder item identifier to convert.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="641c8-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="641c8-121">Parent elements</span></span>

|<span data-ttu-id="641c8-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="641c8-122">**Element**</span></span>|<span data-ttu-id="641c8-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="641c8-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="641c8-124">ConvertId</span><span class="sxs-lookup"><span data-stu-id="641c8-124">ConvertId</span></span>](convertid.md) <br/> |<span data-ttu-id="641c8-125">Define una solicitud para convertir los identificadores de elemento y carpeta entre los formatos admitidos por Exchange.</span><span class="sxs-lookup"><span data-stu-id="641c8-125">Defines a request to convert item and folder identifiers between Exchange supported formats.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="641c8-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="641c8-126">Remarks</span></span>

<span data-ttu-id="641c8-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="641c8-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="641c8-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="641c8-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="641c8-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="641c8-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="641c8-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="641c8-130">Schema Name</span></span>  <br/> |<span data-ttu-id="641c8-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="641c8-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="641c8-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="641c8-132">Validation File</span></span>  <br/> |<span data-ttu-id="641c8-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="641c8-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="641c8-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="641c8-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="641c8-135">Falso</span><span class="sxs-lookup"><span data-stu-id="641c8-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="641c8-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="641c8-136">See also</span></span>



[<span data-ttu-id="641c8-137">Operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="641c8-137">ConvertId operation</span></span>](convertid-operation.md)


- [<span data-ttu-id="641c8-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="641c8-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="641c8-139">Convertir identificadores</span><span class="sxs-lookup"><span data-stu-id="641c8-139">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

