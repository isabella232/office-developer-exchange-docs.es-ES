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
ms.openlocfilehash: cd9f255621b17d01113392e67a0301b01b70f326
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466671"
---
# <a name="searchparameters"></a><span data-ttu-id="a471a-103">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="a471a-103">SearchParameters</span></span>

<span data-ttu-id="a471a-104">El elemento **SearchParameters** representa los parámetros que definen una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a471a-104">The **SearchParameters** element represents the parameters that define a search folder.</span></span> 
  
```xml
<SearchParameters Traversal="">
   <Restriction/>
   <BaseFolderIds/>
</SearchParameters>
```

 <span data-ttu-id="a471a-105">**SearchParametersType**</span><span class="sxs-lookup"><span data-stu-id="a471a-105">**SearchParametersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a471a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a471a-106">Attributes and elements</span></span>

<span data-ttu-id="a471a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="a471a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a471a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="a471a-108">Attributes</span></span>

|<span data-ttu-id="a471a-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="a471a-109">**Attribute**</span></span>|<span data-ttu-id="a471a-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a471a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a471a-111">**Transversal**</span><span class="sxs-lookup"><span data-stu-id="a471a-111">**Traversal**</span></span> <br/> |<span data-ttu-id="a471a-112">Describe cómo una carpeta de búsqueda atraviesa la jerarquía de carpetas.</span><span class="sxs-lookup"><span data-stu-id="a471a-112">Describes how a search folder traverses the folder hierarchy.</span></span> <span data-ttu-id="a471a-113">Las opciones son para una búsqueda en **profundidad** o **superficial** .</span><span class="sxs-lookup"><span data-stu-id="a471a-113">The options are for either a **Deep** or a **Shallow** search.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a471a-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a471a-114">Child elements</span></span>

|<span data-ttu-id="a471a-115">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a471a-115">**Element**</span></span>|<span data-ttu-id="a471a-116">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a471a-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a471a-117">Restriction</span><span class="sxs-lookup"><span data-stu-id="a471a-117">Restriction</span></span>](restriction.md) <br/> |<span data-ttu-id="a471a-118">Representa la restricción o consulta que se usa para filtrar elementos o carpetas en las operaciones de carpeta de búsqueda FindItem/FindFolder.</span><span class="sxs-lookup"><span data-stu-id="a471a-118">Represents the restriction or query that is used to filter items or folders in FindItem/FindFolder and search folder operations.</span></span>  <br/> |
|[<span data-ttu-id="a471a-119">BaseFolderIds</span><span class="sxs-lookup"><span data-stu-id="a471a-119">BaseFolderIds</span></span>](basefolderids.md) <br/> |<span data-ttu-id="a471a-120">Representa la colección de carpetas que se extendrán para determinar el contenido de una carpeta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a471a-120">Represents the collection of folders that will be mined to determine the contents of a search folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a471a-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="a471a-121">Parent elements</span></span>

|<span data-ttu-id="a471a-122">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="a471a-122">**Element**</span></span>|<span data-ttu-id="a471a-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a471a-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a471a-124">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="a471a-124">SearchFolder</span></span>](searchfolder.md) <br/> |<span data-ttu-id="a471a-125">Representa una carpeta de búsqueda contenida en un buzón.</span><span class="sxs-lookup"><span data-stu-id="a471a-125">Represents a search folder that is contained in a mailbox.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a471a-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a471a-126">Remarks</span></span>

<span data-ttu-id="a471a-127">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="a471a-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a471a-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="a471a-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a471a-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="a471a-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a471a-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="a471a-130">Schema Name</span></span>  <br/> |<span data-ttu-id="a471a-131">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="a471a-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="a471a-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="a471a-132">Validation File</span></span>  <br/> |<span data-ttu-id="a471a-133">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="a471a-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a471a-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="a471a-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="a471a-135">Falso</span><span class="sxs-lookup"><span data-stu-id="a471a-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a471a-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a471a-136">See also</span></span>



- [<span data-ttu-id="a471a-137">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="a471a-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

