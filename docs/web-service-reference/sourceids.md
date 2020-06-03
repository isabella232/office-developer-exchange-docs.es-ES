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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466111"
---
# <a name="sourceids"></a><span data-ttu-id="38831-103">SourceIds</span><span class="sxs-lookup"><span data-stu-id="38831-103">SourceIds</span></span>

<span data-ttu-id="38831-104">El elemento **SourceIds** contiene los identificadores de origen que se van a convertir.</span><span class="sxs-lookup"><span data-stu-id="38831-104">The **SourceIds** element contains the source identifiers to convert.</span></span> 
  
[<span data-ttu-id="38831-105">ConvertId</span><span class="sxs-lookup"><span data-stu-id="38831-105">ConvertId</span></span>](convertid.md)
  
[<span data-ttu-id="38831-106">SourceIds</span><span class="sxs-lookup"><span data-stu-id="38831-106">SourceIds</span></span>](sourceids.md)
  
```xml
<SourceIds>
   <AlternateId/>
   <AlternatePublicFolderId/>
   <AlternatePublicFolderItemId/>
</SourceIds>
```

 <span data-ttu-id="38831-107">**NonEmptyArrayOfAlternateIdsType**</span><span class="sxs-lookup"><span data-stu-id="38831-107">**NonEmptyArrayOfAlternateIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="38831-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="38831-108">Attributes and elements</span></span>

<span data-ttu-id="38831-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="38831-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38831-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="38831-110">Attributes</span></span>

<span data-ttu-id="38831-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="38831-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="38831-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="38831-112">Child elements</span></span>

|<span data-ttu-id="38831-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="38831-113">**Element**</span></span>|<span data-ttu-id="38831-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="38831-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38831-115">AlternateId</span><span class="sxs-lookup"><span data-stu-id="38831-115">AlternateId</span></span>](alternateid.md) <br/> |<span data-ttu-id="38831-116">Describe un identificador de elemento o carpeta que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="38831-116">Describes an item or folder identifier to convert.</span></span>  <br/> |
|[<span data-ttu-id="38831-117">AlternatePublicFolderId</span><span class="sxs-lookup"><span data-stu-id="38831-117">AlternatePublicFolderId</span></span>](alternatepublicfolderid.md) <br/> |<span data-ttu-id="38831-118">Describe un identificador de carpeta pública que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="38831-118">Describes a public folder identifier to convert.</span></span>  <br/> |
|[<span data-ttu-id="38831-119">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="38831-119">AlternatePublicFolderItemId</span></span>](alternatepublicfolderitemid.md) <br/> |<span data-ttu-id="38831-120">Describe un identificador de elemento de carpeta pública que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="38831-120">Describes a public folder item identifier to convert.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="38831-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="38831-121">Parent elements</span></span>

|<span data-ttu-id="38831-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="38831-122">**Element**</span></span>|<span data-ttu-id="38831-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="38831-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38831-124">ConvertId</span><span class="sxs-lookup"><span data-stu-id="38831-124">ConvertId</span></span>](convertid.md) <br/> |<span data-ttu-id="38831-125">Define una solicitud para convertir los identificadores de elemento y carpeta entre los formatos admitidos por Exchange.</span><span class="sxs-lookup"><span data-stu-id="38831-125">Defines a request to convert item and folder identifiers between Exchange supported formats.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38831-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="38831-126">Remarks</span></span>

<span data-ttu-id="38831-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="38831-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="38831-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="38831-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38831-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="38831-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="38831-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="38831-130">Schema Name</span></span>  <br/> |<span data-ttu-id="38831-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="38831-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="38831-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="38831-132">Validation File</span></span>  <br/> |<span data-ttu-id="38831-133">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="38831-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="38831-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="38831-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="38831-135">Falso</span><span class="sxs-lookup"><span data-stu-id="38831-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38831-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="38831-136">See also</span></span>



[<span data-ttu-id="38831-137">Operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="38831-137">ConvertId operation</span></span>](convertid-operation.md)


- [<span data-ttu-id="38831-138">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="38831-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="38831-139">Convertir identificadores</span><span class="sxs-lookup"><span data-stu-id="38831-139">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

