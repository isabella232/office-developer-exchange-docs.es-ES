---
title: SearchParameters
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SearchParameters
api_type:
- schema
ms.assetid: 34602cb1-dc33-4552-a98c-3e77f614daa3
description: El elemento SearchParameters representa los parámetros que definen una carpeta de búsqueda.
ms.openlocfilehash: b534574a1292d78c8df99f5186990b114fc4e70a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837299"
---
# <a name="searchparameters"></a><span data-ttu-id="3498c-103">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="3498c-103">SearchParameters</span></span>

<span data-ttu-id="3498c-104">El elemento **SearchParameters** representa los parámetros que definen una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3498c-104">The **SearchParameters** element represents the parameters that define a search folder.</span></span> 
  
```xml
<SearchParameters Traversal="">
   <Restriction/>
   <BaseFolderIds/>
</SearchParameters>
```

 <span data-ttu-id="3498c-105">**SearchParametersType**</span><span class="sxs-lookup"><span data-stu-id="3498c-105">**SearchParametersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3498c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3498c-106">Attributes and elements</span></span>

<span data-ttu-id="3498c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="3498c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3498c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="3498c-108">Attributes</span></span>

|<span data-ttu-id="3498c-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="3498c-109">**Attribute**</span></span>|<span data-ttu-id="3498c-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3498c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3498c-111">**Cruce seguro del**</span><span class="sxs-lookup"><span data-stu-id="3498c-111">**Traversal**</span></span> <br/> |<span data-ttu-id="3498c-112">Describe cómo una carpeta de búsqueda recorre la jerarquía de carpetas.</span><span class="sxs-lookup"><span data-stu-id="3498c-112">Describes how a search folder traverses the folder hierarchy.</span></span> <span data-ttu-id="3498c-113">Las opciones son para un **profundo** o una búsqueda **no exhaustivos** .</span><span class="sxs-lookup"><span data-stu-id="3498c-113">The options are for either a **Deep** or a **Shallow** search.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3498c-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3498c-114">Child elements</span></span>

|<span data-ttu-id="3498c-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="3498c-115">**Element**</span></span>|<span data-ttu-id="3498c-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3498c-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3498c-117">Restriction</span><span class="sxs-lookup"><span data-stu-id="3498c-117">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="3498c-118">Representa la restricción o la consulta que se usa para filtrar los elementos o carpetas en las operaciones de carpeta FindItem/FindFolder y búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3498c-118">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="3498c-119">BaseFolderIds</span><span class="sxs-lookup"><span data-stu-id="3498c-119">BaseFolderIds</span></span>](basefolderids.md) <br/> |<span data-ttu-id="3498c-120">Representa la colección de carpetas que se extraídos para determinar el contenido de una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3498c-120">Represents the collection of folders that will be mined to determine the contents of a search folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3498c-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="3498c-121">Parent elements</span></span>

|<span data-ttu-id="3498c-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="3498c-122">**Element**</span></span>|<span data-ttu-id="3498c-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3498c-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3498c-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="3498c-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="3498c-125">Representa una carpeta de búsqueda que se encuentra en un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="3498c-125">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3498c-126">Notas</span><span class="sxs-lookup"><span data-stu-id="3498c-126">Remarks</span></span>

<span data-ttu-id="3498c-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="3498c-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3498c-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="3498c-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3498c-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3498c-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3498c-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="3498c-130">Schema Name</span></span>  <br/> |<span data-ttu-id="3498c-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="3498c-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="3498c-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="3498c-132">Validation File</span></span>  <br/> |<span data-ttu-id="3498c-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3498c-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3498c-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="3498c-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="3498c-135">False</span><span class="sxs-lookup"><span data-stu-id="3498c-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3498c-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="3498c-136">See also</span></span>



- [<span data-ttu-id="3498c-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="3498c-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

